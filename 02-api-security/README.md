<div align="center">

# 🔌 Sub-Project 2 — API Security Testing Lab

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,50:112240,100:233554&height=220&section=header&text=API%20Security%20Testing%20Lab&fontSize=38&fontColor=64ffda&animation=fadeIn&fontAlignY=38&desc=crAPI%20%7C%20JWT%20%7C%20BOLA%20%7C%20GraphQL%20%7C%20OAuth%20%7C%20Postman%20%7C%20Burp%20Suite&descAlignY=60&descSize=14&descColor=ccd6f6" width="100%"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono\&size=15\&duration=3000\&pause=900\&color=64FFDA\&center=true\&vCenter=true\&multiline=true\&repeat=true\&width=900\&height=70\&lines=API+Security+Testing+Lab;crAPI+%7C+JWT+Analysis+%7C+BOLA+Testing+%7C+GraphQL+Introspection;Evidence-based+testing+%7C+Rejected+attacks+documented+%7C+Secrets+redacted)](https://git.io/typing-svg)

<br/>

[![OWASP API](https://img.shields.io/badge/OWASP_API_Top_10-2023-3E4D6C?style=for-the-badge\&logo=owasp\&logoColor=white)](https://owasp.org/API-Security/)
[![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge\&logo=postman\&logoColor=white)](https://postman.com)
[![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge\&logo=portswigger\&logoColor=white)](https://portswigger.net/burp)
[![GraphQL](https://img.shields.io/badge/GraphQL-Testing-E10098?style=for-the-badge\&logo=graphql\&logoColor=white)](https://graphql.org/)
[![Status](https://img.shields.io/badge/Status-Completed-00d4aa?style=for-the-badge)](.)

<br/>

![crAPI](https://img.shields.io/badge/crAPI-API%20Lab-233554?style=flat-square)
![JWT](https://img.shields.io/badge/JWT-Analysis-000000?style=flat-square\&logo=jsonwebtokens\&logoColor=white)
![ffuf](https://img.shields.io/badge/ffuf-Rate%20Limit%20Testing-005571?style=flat-square)
![Kiterunner](https://img.shields.io/badge/Kiterunner-Endpoint%20Discovery-6e40c9?style=flat-square)
![DVGA](https://img.shields.io/badge/DVGA-GraphQL%20Lab-E10098?style=flat-square)
![OAuth](https://img.shields.io/badge/OAuth-Request%20Analysis-2b6cb0?style=flat-square)

<br/>

*Practical API security assessment covering authentication, authorization, JWT analysis, object-level access control, excessive data exposure, rate-limit behaviour, hidden endpoint discovery, GraphQL introspection, and OAuth request analysis.*

[← Back to Main Project](../README.md)

</div>

---

## 📚 Table of Contents

* [📋 Engagement Summary](#-engagement-summary)
* [🎯 Assessment Scope](#-assessment-scope)
* [🧭 OWASP API Security Top 10 Coverage](#-owasp-api-security-top-10--coverage)
* [🧪 Evidence-Based Testing Summary](#-evidence-based-testing-summary)
* [🔬 Attack Methodology](#-attack-methodology)

  * [Phase 1 — API Lab Deployment](#phase-1--api-lab-deployment)
  * [Phase 2 — API Discovery and Mapping](#phase-2--api-discovery-and-mapping)
  * [Phase 3 — Authentication and JWT Analysis](#phase-3--authentication-and-jwt-analysis)
  * [Phase 4 — Authorization Testing](#phase-4--authorization-testing)
  * [Phase 5 — Data Exposure Testing](#phase-5--data-exposure-testing)
  * [Phase 6 — Rate-Limit Behaviour Testing](#phase-6--rate-limit-behaviour-testing)
  * [Phase 7 — Mass Assignment Testing](#phase-7--mass-assignment-testing)
  * [Phase 8 — Hidden Endpoint Discovery](#phase-8--hidden-endpoint-discovery)
  * [Phase 9 — GraphQL Testing](#phase-9--graphql-testing)
  * [Phase 10 — OAuth Request Analysis](#phase-10--oauth-request-analysis)
* [📸 Evidence Screenshots](#-evidence-screenshots)
* [🖼️ Screenshot Gallery](#️-screenshot-gallery)
* [🧠 Key Security Lessons](#-key-security-lessons)
* [🔐 Redaction and Safety Notes](#-redaction-and-safety-notes)
* [✅ Completion Status](#-completion-status)

---

## 📋 Engagement Summary

| Field                     | Details                                                               |
| ------------------------- | --------------------------------------------------------------------- |
| **Project Area**          | API Security Testing                                                  |
| **Primary API Lab**       | crAPI                                                                 |
| **Additional API Labs**   | DVGA / GraphQL lab, OAuth-focused lab testing                         |
| **API Types Tested**      | REST, JSON, JWT-authenticated APIs, GraphQL                           |
| **Authentication Tested** | JWT Bearer token flow                                                 |
| **Testing Style**         | Authorized lab testing                                                |
| **Attack Machine**        | Kali Linux                                                            |
| **Main Tools**            | Postman, Burp Suite, JWT.io, ffuf, Kiterunner, DVGA, browser DevTools |
| **Methodology Reference** | OWASP API Security Top 10                                             |
| **Evidence Style**        | Screenshot-based, redacted, GitHub portfolio documentation            |
| **Assessment Status**     | Completed Practical Assessment                                        |

> This API assessment was performed only against intentionally vulnerable or controlled lab environments. Some tests confirmed vulnerable behaviour, while other tests confirmed that the API rejected malicious input. Both outcomes are documented because professional security testing must validate weaknesses and controls.

---

## 🎯 Assessment Scope

The API Security Lab focused on the following areas:

```text
API Lab Deployment
→ Authentication Flow Testing
→ JWT Token Inspection
→ Authorization / BOLA Testing
→ Excessive Data Exposure Review
→ Rate-Limit Behaviour Testing
→ Mass Assignment Testing
→ Hidden Endpoint Discovery
→ GraphQL Introspection Testing
→ OAuth Request Analysis
→ Evidence Capture and Redaction
```

### In Scope

| Area                                       |      Status |
| ------------------------------------------ | ----------: |
| crAPI Docker lab                           | ✅ Completed |
| Postman login and JWT workflow             | ✅ Completed |
| JWT decoding and claim review              | ✅ Completed |
| BOLA / IDOR-style access test              | ✅ Completed |
| Excessive data exposure review             | ✅ Completed |
| ffuf-based rate-limit behaviour test       | ✅ Completed |
| Mass assignment test                       | ✅ Completed |
| Kiterunner hidden endpoint discovery       | ✅ Completed |
| DVGA GraphQL lab                           | ✅ Completed |
| GraphQL endpoint and introspection testing | ✅ Completed |
| OAuth request analysis in Burp             | ✅ Completed |

### Out of Scope

| Area                  | Reason                                 |
| --------------------- | -------------------------------------- |
| Production APIs       | Not authorized                         |
| Real OAuth providers  | Testing restricted to lab environments |
| Real user accounts    | Only lab accounts used                 |
| Destructive testing   | Not required for portfolio evidence    |
| Token/secret exposure | All sensitive values must be redacted  |

---

## 🧭 OWASP API Security Top 10 — Coverage

This table reflects **what was tested and evidenced**, not exaggerated vulnerability counts.

| ID    | OWASP API Category                              | Tested | Evidence / Result                                    | Outcome                              |
| ----- | ----------------------------------------------- | :----: | ---------------------------------------------------- | ------------------------------------ |
| API1  | Broken Object Level Authorization               |    ✅   | BOLA/IDOR-style object access test                   | Vulnerable behaviour observed in lab |
| API2  | Broken Authentication                           |    ✅   | JWT login, decoding, manipulation attempt            | Token manipulation rejected          |
| API3  | Broken Object Property Level Authorization      |    ✅   | Excessive data exposure / hidden fields review       | Data exposure reviewed               |
| API4  | Unrestricted Resource Consumption               |    ✅   | ffuf rate-limit behaviour testing                    | Behaviour tested and documented      |
| API5  | Broken Function Level Authorization             |    ✅   | Hidden endpoint discovery and endpoint access review | Tested with Kiterunner / API mapping |
| API6  | Unrestricted Access to Sensitive Business Flows |    ✅   | Business-flow style API access reviewed              | Tested in lab context                |
| API7  | Server Side Request Forgery                     |    ⚪   | Not a primary tested finding in current evidence     | Not claimed                          |
| API8  | Security Misconfiguration                       |    ✅   | Tools/version checks and exposed lab behaviour       | Reviewed                             |
| API9  | Improper Inventory Management                   |    ✅   | Hidden / undocumented endpoint discovery             | Endpoints discovered                 |
| API10 | Unsafe Consumption of APIs                      |    ⚪   | Not deeply tested in this phase                      | Not claimed                          |


---

## 🧪 Evidence-Based Testing Summary

| Test Area | Evidence File | Result Type |
|---|---|---|
| crAPI containers running | [Open Report](./reports/evidence/00-crapi-docker-containers-running-evidence-report.pdf) | Lab deployment proof |
| crAPI homepage accessible | [Open Report](./reports/evidence/01-crapi-homepage-browser-evidence-report.pdf) | Target availability proof |
| Postman login + JWT | [Open Report](./reports/evidence/02-postman-login-jwt-token-evidence-report.pdf) | Auth workflow captured |
| JWT decoded in jwt.io | [Open Report](./reports/evidence/03-jwtio-decoded-token-evidence-report.pdf) | Token analysis |
| Postman collection structure | [Open Report](./reports/evidence/04-postman-collection-structure-evidence-report.pdf) | Testing workflow |
| API tools version check | [Open Report](./reports/evidence/05-api-tools-version-check-evidence-report.pdf) | Tool readiness |
| BOLA / IDOR test | [Open Report](./reports/evidence/06-bola-idor-accessing-another-user-data-evidence-report.pdf) | Vulnerable behaviour observed |
| JWT claim review | [Open Report](./reports/evidence/07-jwt-decodetoken-analysis-evidence-report.pdf) | Token claim analysis |
| JWT attack attempt | [Open Report](./reports/evidence/08-jwt-attack-attempt-token-rejected-evidence-report.pdf) | Attack rejected / control validated |
| Excessive data exposure | [Open Report](./reports/evidence/09-excessive-data-exposure-hidden-fields-evidence-report.pdf) | Data exposure review |
| Rate-limit behaviour | [Open Report](./reports/evidence/10-no-rate-limiting-ffuf-running-p1-evidence-report.pdf) | ffuf testing evidence |
| Rate-limit behaviour continued | [Open Report](./reports/evidence/11-no-rate-limiting-ffuf-running-p2-evidence-report.pdf) | ffuf testing evidence |
| Mass assignment | [Open Report](./reports/evidence/12-mass-assignment-extra-fields-rejected-evidence-report.pdf) | Attack rejected / control validated |
| Hidden endpoints | [Open Report](./reports/evidence/13-kiterunner-hidden-endpoints-discovered-evidence-report.pdf) | Endpoint discovery |
| DVGA GraphQL lab | [Open Report](./reports/evidence/14-dvga-graphql-lab-running-evidence-report.pdf) | GraphQL lab proof |
| GraphQL endpoint alive | [Open Report](./reports/evidence/15-graphql-endpoint-alive-evidence-report.pdf) | Endpoint availability |
| GraphQL introspection | [Open Report](./reports/evidence/16-graphql-introspection-schema-discovery-evidence-report.pdf) | Schema discovery |
| GraphQL data query | [Open Report](./reports/evidence/17-graphql-user-data-query-test-evidence-report.pdf) | Query testing |
| OAuth request analysis | [Open Report](./reports/evidence/18-oauth-lab-burp-request-analysis-evidence-report.pdf) | OAuth request review |

---

## 🔬 Attack Methodology

---

### Phase 1 — API Lab Deployment

**Objective:** Confirm that the API lab environment is running and reachable before testing.

```bash
# Check running Docker containers
docker ps

# Confirm crAPI is reachable in browser
http://127.0.0.1:8888
```

**Evidence captured:**

```text
00-crapi-docker-containers-running.png
01-crapi-homepage-browser.png
```

**Result:**

```text
crAPI lab environment was deployed successfully and accessed through the browser.
```

---

### Phase 2 — API Discovery and Mapping

**Objective:** Identify API endpoints and build a structured request collection.

```bash
# API-aware discovery using Kiterunner
kr scan http://127.0.0.1:8888

# Additional endpoint behaviour testing with ffuf
ffuf -u http://127.0.0.1:8888/FUZZ \
  -w /usr/share/wordlists/seclists/Discovery/Web-Content/api/api-endpoints.txt
```

Postman was used to organize discovered requests and maintain a repeatable testing workflow.

**Evidence captured:**

```text
04-postman-collection-structure.png
10-kiterunner-hidden-endpoints-discovered.png
```

**Result:**

```text
API requests were organized in Postman, and hidden or undocumented endpoints were discovered using Kiterunner.
```

---

### Phase 3 — Authentication and JWT Analysis

**Objective:** Understand the login process, capture JWT tokens, and inspect token claims.

```http
POST /identity/api/auth/login
Content-Type: application/json

{
  "email": "lab-user@example.com",
  "password": "REDACTED"
}
```

Successful authentication returned a JWT-style bearer token, which was then decoded for claim analysis.

```text
Authorization: Bearer <REDACTED_TOKEN>
```

JWT inspection was performed using JWT.io and local decoding methods.

**Evidence captured:**

```text
02-postman-login-jwt-token.png
03-jwtio-decoded-token.png
06-JWT-decodetoken-analysis.png
```

**Result:**

```text
JWT authentication flow was captured and analyzed. Token values were redacted before publication.
```

---

### Phase 4 — Authorization Testing

#### Test Case 1 — BOLA / IDOR-Style Object Access

**Objective:** Check whether an authenticated user can access another user's object by changing an object identifier.

```http
GET /api/resource/{object_id}
Authorization: Bearer <REDACTED_TOKEN>
```

The object identifier was modified to test whether the server enforced ownership checks.

```text
Original object ID → owned resource
Modified object ID → another user's resource
```

**Evidence captured:**

```text
05-bola-accessing-another-user-data.png
```

**Observed behaviour:**

```text
BOLA/IDOR-style access behaviour was observed in the lab environment.
```

**Risk:**

```text
If present in production, this issue could allow authenticated users to access other users' private objects or sensitive data.
```

**Recommended remediation:**

```text
Implement server-side object ownership checks for every object access request.
Never trust client-supplied IDs without validating ownership against the authenticated user.
```

---

### Phase 5 — Data Exposure Testing

#### Test Case 2 — Excessive Data Exposure / Hidden Fields Review

**Objective:** Review API responses for unnecessary fields returned to the client.

```http
GET /api/user/profile
Authorization: Bearer <REDACTED_TOKEN>
```

Responses were reviewed for fields such as:

```text
internal IDs
roles
email fields
hidden attributes
debug fields
sensitive metadata
```

**Evidence captured:**

```text
07-excessive-data-exposure-hidden-fields.png
```

**Observed behaviour:**

```text
API responses were inspected for hidden or excessive fields.
```

**Risk:**

```text
APIs that return more data than required can expose internal application logic, user metadata, or sensitive fields to attackers.
```

**Recommended remediation:**

```text
Return only fields required by the frontend.
Use response DTOs or serializers to prevent accidental exposure of internal model fields.
```

---

### Phase 6 — Rate-Limit Behaviour Testing

#### Test Case 3 — Rate-Limit Behaviour with ffuf

**Objective:** Test whether the API responds with throttling behaviour under repeated requests.

```bash
ffuf \
  -u http://127.0.0.1:8888/FUZZ \
  -w /usr/share/wordlists/seclists/Discovery/Web-Content/api/api-endpoints.txt \
  -t 20
```

**Evidence captured:**

```text
08-no-rate-limiting-ffuf-running-p1.png
08-no-rate-limiting-ffuf-running-p2.png
```

**Observed behaviour:**

```text
Rate-limit behaviour was tested using ffuf. The evidence shows repeated request testing against the lab target.
```

**Important note:**

```text
This should be described as rate-limit behaviour testing unless the screenshot clearly proves no throttling or 429 response was absent over a meaningful request volume.
```

**Recommended remediation:**

```text
Implement rate limiting, account lockout controls, IP throttling, and monitoring for repeated failed requests.
```

---

### Phase 7 — Mass Assignment Testing

#### Test Case 4 — Extra Fields Rejected

**Objective:** Check whether the API accepts unexpected sensitive fields in JSON requests.

```http
POST /identity/api/auth/signup
Content-Type: application/json

{
  "name": "Lab User",
  "email": "lab-user@example.com",
  "password": "REDACTED",
  "role": "admin",
  "isAdmin": true
}
```

**Evidence captured:**

```text
09-mass-assignment-extra-fields-rejected.png
```

**Observed behaviour:**

```text
Mass assignment-style extra fields were rejected by the API.
```

**Result type:**

```text
Control validation — the malicious input was not accepted.
```

**Recommended remediation:**

```text
Use explicit allowlists for accepted request fields.
Never bind client JSON directly to sensitive server-side model attributes.
```

---

### Phase 8 — Hidden Endpoint Discovery

#### Test Case 5 — Kiterunner Endpoint Discovery

**Objective:** Identify hidden or undocumented API routes.

```bash
kr scan http://127.0.0.1:8888 \
  -w /usr/share/wordlists/kiterunner/routes-small.kite
```

**Evidence captured:**

```text
10-kiterunner-hidden-endpoints-discovered.png
```

**Observed behaviour:**

```text
Kiterunner discovered API endpoints for further testing and mapping.
```

**Risk:**

```text
Undocumented endpoints may expose old functionality, admin functions, or insecure legacy routes.
```

**Recommended remediation:**

```text
Maintain a complete API inventory.
Remove deprecated endpoints.
Require authentication and authorization checks on every endpoint.
```

---

### Phase 9 — GraphQL Testing

#### Test Case 6 — DVGA GraphQL Lab and Endpoint Check

**Objective:** Validate GraphQL endpoint availability and test introspection behaviour.

```http
GET /graphql
```

**Evidence captured:**

```text
11-dvga-graphql-lab-running.png
11-graphql-endpoint-alive.png
```

---

#### Test Case 7 — GraphQL Introspection

**Objective:** Check whether the GraphQL schema is exposed through introspection.

```json
{
  "__schema": {
    "types": {
      "name": "..."
    }
  }
}
```

**Evidence captured:**

```text
12-graphql-introspection-schema-discovery.png
```

**Observed behaviour:**

```text
GraphQL schema discovery was performed through introspection in the lab.
```

**Risk:**

```text
Exposed introspection can help attackers map available types, queries, mutations, and sensitive objects.
```

**Recommended remediation:**

```text
Disable introspection in production unless explicitly required.
Apply authorization at resolver level.
Monitor unusual GraphQL queries.
```

---

#### Test Case 8 — GraphQL User Data Query

**Objective:** Query discovered GraphQL fields and review returned user data.

```graphql
query {
  users {
    id
    email
    role
  }
}
```

**Evidence captured:**

```text
13-graphql-user-data-query-test.png
```

**Observed behaviour:**

```text
GraphQL user-data query testing was performed using the lab endpoint.
```

**Recommended remediation:**

```text
Apply resolver-level authorization.
Return only necessary fields.
Avoid exposing sensitive user fields through broad GraphQL queries.
```

---

### Phase 10 — OAuth Request Analysis

#### Test Case 9 — OAuth Request Review in Burp Suite

**Objective:** Analyze OAuth request parameters and understand the authorization flow.

OAuth request fields reviewed included:

```text
client_id
redirect_uri
response_type
scope
state
code
callback URL
```

**Evidence captured:**

```text
14-oauth-lab-burp-request-analysis.png
```

**Observed behaviour:**

```text
OAuth request analysis was performed in Burp Suite using a lab environment.
```

**Security checks performed:**

```text
redirect_uri review
state parameter review
scope review
authorization code flow observation
request/response inspection
```

**Recommended remediation:**

```text
Strictly validate redirect_uri.
Use and verify unpredictable state values.
Limit OAuth scopes.
Never expose client secrets in frontend code.
Protect authorization codes and tokens.
```

---

## 📸 Evidence Screenshots

| #  | Screenshot                                      | Description                            |
| -- | ----------------------------------------------- | -------------------------------------- |
| 00 | `00-crapi-docker-containers-running.png`        | crAPI containers running               |
| 01 | `01-crapi-homepage-browser.png`                 | crAPI homepage accessible              |
| 02 | `02-postman-login-jwt-token.png`                | Login request and JWT workflow         |
| 03 | `03-jwtio-decoded-token.png`                    | JWT decoded and inspected              |
| 04 | `04-postman-collection-structure.png`           | Postman collection structure           |
| 05 | `05-api-tools-version-check.png`                | API tools version check                |
| 06 | `05-bola-accessing-another-user-data.png`       | BOLA/IDOR-style object access test     |
| 07 | `06-JWT-decodetoken-analysis.png`               | JWT decoded token analysis             |
| 08 | `06-jwt-attack-attempt-token-rejected.png`      | JWT manipulation attempt rejected      |
| 09 | `07-excessive-data-exposure-hidden-fields.png`  | Excessive data exposure review         |
| 10 | `08-no-rate-limiting-ffuf-running-p1.png`       | Rate-limit behaviour testing           |
| 11 | `08-no-rate-limiting-ffuf-running-p2.png`       | Continued ffuf testing evidence        |
| 12 | `09-mass-assignment-extra-fields-rejected.png`  | Mass assignment extra fields rejected  |
| 13 | `10-kiterunner-hidden-endpoints-discovered.png` | Hidden endpoint discovery              |
| 14 | `11-dvga-graphql-lab-running.png`               | DVGA GraphQL lab running               |
| 15 | `11-graphql-endpoint-alive.png`                 | GraphQL endpoint alive                 |
| 16 | `12-graphql-introspection-schema-discovery.png` | GraphQL introspection schema discovery |
| 17 | `13-graphql-user-data-query-test.png`           | GraphQL user data query test           |
| 18 | `14-oauth-lab-burp-request-analysis.png`        | OAuth request analysis in Burp         |

---

## 🖼️ Screenshot Gallery

> All sensitive values must be redacted before public upload. This includes JWTs, bearer tokens, cookies, emails, user IDs, OAuth codes, client secrets, access tokens, and refresh tokens.

![crAPI Docker Containers Running](./screenshots/00-crapi-docker-containers-running.png)

![crAPI Homepage Browser](./screenshots/01-crapi-homepage-browser.png)

![Postman Login JWT Token](./screenshots/02-postman-login-jwt-token.png)

![JWT.io Decoded Token](./screenshots/03-jwtio-decoded-token.png)

![Postman Collection Structure](./screenshots/04-postman-collection-structure.png)

![API Tools Version Check](./screenshots/05-api-tools-version-check.png)

![BOLA Accessing Another User Data](./screenshots/05-bola-accessing-another-user-data.png)

![JWT Decode Token Analysis](./screenshots/06-JWT-decodetoken-analysis.png)

![JWT Attack Attempt Token Rejected](./screenshots/06-jwt-attack-attempt-token-rejected.png)

![Excessive Data Exposure Hidden Fields](./screenshots/07-excessive-data-exposure-hidden-fields.png)

![No Rate Limiting ffuf Running Part 1](./screenshots/08-no-rate-limiting-ffuf-running-p1.png)

![No Rate Limiting ffuf Running Part 2](./screenshots/08-no-rate-limiting-ffuf-running-p2.png)

![Mass Assignment Extra Fields Rejected](./screenshots/09-mass-assignment-extra-fields-rejected.png)

![Kiterunner Hidden Endpoints Discovered](./screenshots/10-kiterunner-hidden-endpoints-discovered.png)

![DVGA GraphQL Lab Running](./screenshots/11-dvga-graphql-lab-running.png)

![GraphQL Endpoint Alive](./screenshots/11-graphql-endpoint-alive.png)

![GraphQL Introspection Schema Discovery](./screenshots/12-graphql-introspection-schema-discovery.png)

![GraphQL User Data Query Test](./screenshots/13-graphql-user-data-query-test.png)

![OAuth Lab Burp Request Analysis](./screenshots/14-oauth-lab-burp-request-analysis.png)

---

## 🧠 Key Security Lessons

| Area               | Lesson                                                                             |
| ------------------ | ---------------------------------------------------------------------------------- |
| Authentication     | JWTs must be protected, validated, and never exposed publicly                      |
| Authorization      | Object-level access must be checked server-side for every request                  |
| JWT Testing        | A rejected JWT attack attempt is useful evidence of control validation             |
| Data Exposure      | APIs should return only the minimum fields required                                |
| Rate Limiting      | Repeated request behaviour should be monitored and throttled                       |
| Mass Assignment    | APIs should reject unexpected sensitive fields                                     |
| Endpoint Discovery | Hidden endpoints should be inventoried, protected, and removed if unused           |
| GraphQL            | Introspection and broad queries can expose schema and data paths                   |
| OAuth              | Redirect URIs, state values, scopes, and token handling must be reviewed carefully |
| Reporting          | Screenshots must be redacted before public GitHub upload                           |

---

## 🔐 Redaction and Safety Notes

Before publishing this folder publicly, redact:

```text
JWT tokens
Bearer tokens
Authorization headers
Session cookies
Emails
User IDs if private
OAuth authorization codes
OAuth access tokens
OAuth refresh tokens
Client secrets
Passwords
Internal IPs if sensitive
```

Do not commit:

```text
real API tokens
Postman environments containing secrets
raw bearer tokens
client secrets
refresh tokens
cookies
private credentials
```

If a Postman collection is uploaded, ensure that token values are removed or replaced with placeholders such as:

```text
{{token}}
{{base_url}}
{{user_id}}
```

---

## ✅ Completion Status

| Section                         |      Status |
| ------------------------------- | ----------: |
| crAPI deployment evidence       | ✅ Completed |
| API authentication testing      | ✅ Completed |
| JWT decoding and claim analysis | ✅ Completed |
| BOLA / IDOR-style testing       | ✅ Completed |
| Excessive data exposure review  | ✅ Completed |
| Rate-limit behaviour testing    | ✅ Completed |
| Mass assignment testing         | ✅ Completed |
| Hidden endpoint discovery       | ✅ Completed |
| GraphQL introspection testing   | ✅ Completed |
| OAuth request analysis          | ✅ Completed |
| Evidence redaction reminder     |  ✅ Included |
| GitHub documentation            | ✅ Completed |

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:233554,100:0d1117&height=110&section=footer&text=&fontColor=64ffda" width="100%"/>

### API security is not only about finding vulnerabilities — it is about proving what is vulnerable, what is protected, and why it matters.

[← Back to Main Project](../README.md)

</div>
