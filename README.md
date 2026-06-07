<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,30:0a192f,60:112240,100:0d1117&height=280&section=header&text=Enterprise%20Security%20Assessment%20Lab&fontSize=36&fontColor=64ffda&animation=fadeIn&fontAlignY=40&desc=Web%20%7C%20API%20%7C%20Network%20%7C%20Active%20Directory%20%7C%20AWS%20Cloud%20%7C%20Azure&descAlignY=58&descSize=15&descColor=8892b0" width="100%"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=15&duration=3500&pause=1200&color=64FFDA&center=true&vCenter=true&multiline=true&repeat=true&width=780&height=55&lines=Hands-on+Penetration+Testing+%7C+Active+Directory+%7C+Cloud+Security;Impacket+%7C+BloodHound+%7C+Responder+%7C+Pacu+%7C+ScoutSuite+%7C+CloudGoat)](https://git.io/typing-svg)

<br/>

<!-- Status & Type -->
![Status](https://img.shields.io/badge/Status-Active_Portfolio_Project-64ffda?style=for-the-badge&logo=statuspage&logoColor=0d1117)
![Type](https://img.shields.io/badge/Type-Hands--on_Security_Lab-0a192f?style=for-the-badge&logo=hackthebox&logoColor=64ffda)
![Level](https://img.shields.io/badge/Level-Beginner_%E2%86%92_Intermediate_Practical-112240?style=for-the-badge&logo=levelsdotfyi&logoColor=ccd6f6)
![Ethics](https://img.shields.io/badge/Ethics-Authorized_Lab_Only-ff6b6b?style=for-the-badge&logo=opensourceinitiative&logoColor=white)

<br/>

<!-- Platform badges -->
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server_2019-0078D6?style=flat-square&logo=windows&logoColor=white)
![Windows 10](https://img.shields.io/badge/Windows_10_Enterprise-0078D6?style=flat-square&logo=windows&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active_Directory-003366?style=flat-square&logo=microsoft&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Python](https://img.shields.io/badge/Python_3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

<!-- Tool badges -->
<br/>
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=portswigger&logoColor=white)
![BloodHound](https://img.shields.io/badge/BloodHound-DC143C?style=flat-square&logo=github&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-008CC1?style=flat-square&logo=neo4j&logoColor=white)
![Impacket](https://img.shields.io/badge/Impacket-2E4057?style=flat-square&logo=python&logoColor=white)
![Responder](https://img.shields.io/badge/Responder-8B0000?style=flat-square)
![Hashcat](https://img.shields.io/badge/Hashcat-374151?style=flat-square)
![NetExec](https://img.shields.io/badge/NetExec-1a1a2e?style=flat-square)
![AWS CLI](https://img.shields.io/badge/AWS_CLI-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![CloudGoat](https://img.shields.io/badge/CloudGoat-FF4500?style=flat-square)
![Pacu](https://img.shields.io/badge/Pacu-CC4400?style=flat-square)
![ScoutSuite](https://img.shields.io/badge/ScoutSuite-1E90FF?style=flat-square)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Azure CLI](https://img.shields.io/badge/Azure_CLI-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

</div>

---

## 🔎 Project Overview

This is a **multi-domain, hands-on security assessment lab** built from scratch to develop, practise, and document real-world penetration testing techniques across enterprise attack surfaces.

Every completed phase includes:
- Step-by-step methodology notes
- Evidence screenshots (sensitive values redacted)
- Tool commands and outputs
- Attack path analysis
- Responsible cleanup verification

> **All activity is performed exclusively on self-owned, intentionally vulnerable, isolated lab environments. No production systems or external infrastructure are involved.**

---

## 📊 Project Status

| Sub-Project | Status | Evidence | Notes |
|-------------|--------|----------|-------|
| 🏢 AD & Internal Network | ✅ **Completed** | 10 screenshots | Full attack chain documented |
| ☁️ AWS Cloud Security | ✅ **Completed** | 8 screenshots | CloudGoat + ScoutSuite + Pacu |
| 🔷 Azure Security | ⚠️ **Attempted — Quota Blocked** | 3 screenshots | Documented & cleaned up |
| 🌐 Web Application VAPT | 🔄 **In Progress** | — | Lab prepared, testing ongoing |
| 🔌 API Security | 🔄 **In Progress** | — | Structure & methodology prepared |
| 🟡 GCP Security | 📅 **Deferred** | — | Scheduled after AWS/Azure complete |
| 📜 Certification Roadmap | ✅ **Documented** | — | Path defined in `/06-roadmap/` |

---

## 🗺️ Lab Architecture

```
┌──────────────────────────────────────────────────────────────────────┐
│                   ENTERPRISE SECURITY LAB — TOPOLOGY                  │
├────────────────────────┬─────────────────────────┬───────────────────┤
│   INTERNAL AD NETWORK  │    WEB / API LAB         │   CLOUD TARGETS   │
│   192.168.X.X / 24     │   Docker / Local         │   AWS  |  Azure   │
│                        │                          │                   │
│  ┌──────────────────┐  │  ┌────────────────────┐  │  ┌─────────────┐  │
│  │  Kali Linux      │  │  │  DVWA              │  │  │ CloudGoat   │  │
│  │  Attacker Box    │  │  │  WebGoat           │  │  │ IAM / S3    │  │
│  └────────┬─────────┘  │  │  Juice Shop        │  │  │ EC2 / IMDS  │  │
│           │            │  │  crAPI (planned)   │  │  └─────────────┘  │
│  ┌────────▼─────────┐  │  └────────────────────┘  │  ┌─────────────┐  │
│  │  DC01            │  │                          │  │ AzureGoat   │  │
│  │  Windows Server  │  │                          │  │ (attempted, │  │
│  │  corp.local      │  │                          │  │ quota block)│  │
│  ├──────────────────┤  │                          │  └─────────────┘  │
│  │  WS01            │  │                          │                   │
│  │  Windows 10 Ent  │  │                          │                   │
│  │  Domain Member   │  │                          │                   │
│  └──────────────────┘  │                          │                   │
└────────────────────────┴─────────────────────────┴───────────────────┘
```

---

## 📁 Repository Structure

```
enterprise-security-assessment-lab/
│
├── README.md
├── .gitignore
│
├── 01-web-vapt/                  🔄 In Progress
│   ├── README.md
│   ├── screenshots/
│   ├── tool-outputs/
│   └── scripts/
│
├── 02-api-security/              🔄 In Progress
│   ├── README.md
│   ├── screenshots/
│   ├── postman-collections/
│   └── tools/
│       └── api_security_tester.py
│
├── 03-ad-network/                ✅ Completed
│   ├── README.md
│   ├── screenshots/              ← 10 evidence screenshots
│   ├── reports/
│   └── notes/
│
├── 04-cloud-security/            ✅ Completed (AWS)
│   ├── README.md
│   ├── screenshots/              ← 8 evidence screenshots
│   ├── reports/
│   └── scripts/
│
├── 05-azure-security/            ⚠️ Attempted / Cleaned Up
│   ├── README.md
│   ├── screenshots/              ← 3 evidence screenshots
│   └── reports/
│
└── 06-roadmap/
    └── certification-roadmap.md
```

---

## 🏢 Sub-Project 3 — Active Directory & Internal Network Pentest

> **Status: ✅ Completed** | Platform: Kali Linux → Windows Server 2019 + Windows 10 (corp.local)

### Lab Environment

| Component | Details |
|-----------|---------|
| Domain | `corp.local` |
| Domain Controller | Windows Server 2019 — DC01 |
| Workstation | Windows 10 Enterprise — WS01 |
| Attacker | Kali Linux |
| Network | Isolated host-only — private lab |
| Config | Intentionally misconfigured users & privileges for training |

### Attack Chain — Phase by Phase

```
Phase 1: Discovery          Phase 2: Credential Capture    Phase 3: AD Exploitation
────────────────────        ───────────────────────────    ────────────────────────
Nmap host discovery   →     Responder LLMNR poisoning  →   Kerberoasting (Impacket)
SMB enumeration       →     NTLMv2 hash capture         →   Kerberoast hash cracking
Domain enumeration    →     Hashcat offline crack        →   BloodHound collection
enum4linux-ng         →     Credential validation (SMB) →   Attack path analysis

Phase 4: Privilege & Impact
────────────────────────────────
Pass-the-Hash → SYSTEM shell
DCSync → domain hash extraction (lab only, values redacted)
BloodHound domain overview graph
```

### Evidence — Screenshots

> All sensitive values (hashes, passwords, tokens) are **redacted** before publication.

**Responder — NTLMv2 Hash Capture**
```
Technique:  LLMNR/NBT-NS poisoning via Responder
MITRE:      T1557.001 — Adversary-in-the-Middle
Result:     NTLMv2 hash intercepted from domain workstation
```
![Responder NTLMv2 Hash Captured](./03-ad-network/screenshots/10-responder-ntlmv2-hash-captured.png)

---

**Hashcat — Offline NTLMv2 Crack**
```
Technique:  Offline password cracking (no lockout triggered)
Tool:       Hashcat -m 5600
Result:     Domain credential recovered from captured hash
```
![Hashcat NTLMv2 Cracked](./03-ad-network/screenshots/11-hashcat-ntlmv2-cracked.png)

---

**NetExec — SMB Enumeration & Credential Validation**
```
Technique:  SMB credential validation and share enumeration
Tool:       NetExec (CrackMapExec successor)
Result:     Credentials confirmed valid against domain services
```
![SMB Enumeration Credential Validation](./03-ad-network/screenshots/12-smb-enumeration-credential-validation.png)

---

**Kerberoasting — SPN Ticket Request**
```
Technique:  Kerberoasting — offline service ticket cracking
MITRE:      T1558.003 — Steal or Forge Kerberos Tickets
Tool:       Impacket GetUserSPNs.py
Result:     Kerberos service ticket (TGS) extracted for offline cracking
```
![Kerberoasting SPN Ticket Requested](./03-ad-network/screenshots/13-kerberoasting-spn-ticket-requested.png)

---

**Hashcat — Kerberoast Hash Cracked**
```
Tool:       Hashcat -m 13100
Result:     Service account credential recovered offline
```
![Kerberoast Hash Cracked](./03-ad-network/screenshots/14-kerberoast-hash-cracked.png)

---

**BloodHound — Attack Path to Domain Admin**
```
Technique:  AD attack path analysis and graph visualisation
Tool:       BloodHound + Neo4j + BloodHound.py collection
Result:     Shortest path to Domain Admin identified and visualised
```
![BloodHound Attack Path Domain Admin](./03-ad-network/screenshots/15-bloodhound-attack-path-domain-admin.png)

---

**BloodHound — Domain Overview Graph**
```
Result:  Full domain object graph: users, groups, computers, relationships
```
![BloodHound Domain Overview Graph](./03-ad-network/screenshots/16-bloodhound-domain-overview-graph.png)

---

**Pass-the-Hash — SYSTEM Shell Obtained**
```
Technique:  Pass-the-Hash lateral movement
MITRE:      T1550.002 — Use Alternate Authentication Material
Tool:       Impacket psexec.py
Result:     SYSTEM-level shell obtained on target using NTLM hash
```
![Pass the Hash SYSTEM Shell Obtained](./03-ad-network/screenshots/17-pass-the-hash-system-shell-obtained.png)

---

**DCSync — Domain Hash Extraction (Lab Only)**
```
Technique:  DCSync — simulate DC replication to extract hashes
MITRE:      T1003.006 — DCSync
Tool:       Impacket secretsdump.py
Scope:      Private lab only. All hash values redacted before publication.
```
![DCSync Domain Hashes Dumped](./03-ad-network/screenshots/18-dcsync-domain-hashes-dumped.png)
![DCSync All Domain Hashes Dumped](./03-ad-network/screenshots/18b-dcsync-all-domain-hashes-dumped.png)

---

### AD Findings Summary

| Technique | MITRE ID | Outcome |
|-----------|----------|---------|
| LLMNR/NBT-NS Poisoning | T1557.001 | NTLMv2 hash captured |
| Offline Hash Cracking | T1110.002 | Domain credential recovered |
| Kerberoasting | T1558.003 | Service account credential recovered |
| BloodHound Recon | T1069.002 | Domain Admin attack path identified |
| Pass-the-Hash | T1550.002 | SYSTEM shell on target |
| DCSync (lab) | T1003.006 | Domain hashes extracted (redacted) |

---

## ☁️ Sub-Project 4 — AWS Cloud Security Assessment

> **Status: ✅ Completed** | Platform: AWS Free Tier — CloudGoat, Pacu, ScoutSuite

### Lab Setup & Safety

- Personal AWS account — isolated lab environment
- Root MFA enabled before any lab deployment
- Budget and free-tier usage monitoring configured
- CloudGoat deployed and destroyed responsibly
- Billing and cleanup verified after completion

### Attack Chain Summary

```
Phase 1: Authentication & Enumeration
───────────────────────────────────────
AWS CLI configured → Identity verified (aws sts get-caller-identity)
IAM permissions enumerated → Policy documents reviewed
Available services and resources mapped

Phase 2: Exploitation Scenarios
────────────────────────────────────────────────────────────────────
CloudGoat scenario deployed → IAM privilege escalation via PassRole + EC2
Pacu IAM privesc scan → viable escalation paths identified
IAM instance profile assumed on target EC2 (CloudGoat scenario objective met)

Phase 3: Misconfiguration Testing
──────────────────────────────────────────────────────────────────────────────
S3 unauthenticated access tested (--no-sign-request) → public bucket accessed
EC2 IMDS endpoint accessed in lab → temporary credentials retrieved (redacted)
ScoutSuite full AWS audit run → HTML report generated

Phase 4: Cleanup & Verification
───────────────────────────────────────────────
CloudGoat scenarios destroyed → resources verified removed
EC2 instances terminated → confirmed
S3 buckets removed → no buckets remaining confirmed
Free-tier / billing dashboard reviewed
```

### Evidence — Screenshots

> Account IDs, access keys, secret keys, tokens, and IPs are **fully redacted** in all screenshots.

**IAM Permissions Enumeration**
```
Tool:    AWS CLI — aws iam list-attached-user-policies / get-policy-version
Result:  Current user's IAM permissions mapped before exploitation
```
![IAM Permissions Enumeration](./04-cloud-security/screenshots/iam-permissions-enumeration.png)

---

**Pacu — IAM Privilege Escalation Scan**
```
Tool:    Pacu — iam__privesc_scan module
Result:  Viable IAM privilege escalation paths identified for CloudGoat user
```
![Pacu Privesc Scan Results](./04-cloud-security/screenshots/pacu-privesc-scan-results.png)

---

**S3 — Unauthenticated Public Access**
```
Command: aws s3 ls s3://[bucket] --no-sign-request
Result:  CloudGoat S3 bucket accessible without credentials
         (intentionally misconfigured lab target)
```
![S3 Public Bucket Unauthenticated Access](./04-cloud-security/screenshots/s3-public-bucket-unauthenticated-access.png)

---

**ScoutSuite — AWS Audit Report Overview**
```
Tool:    ScoutSuite — multi-service AWS security audit
Result:  HTML dashboard showing findings across IAM, S3, EC2, and other services
```
![ScoutSuite HTML Report Overview](./04-cloud-security/screenshots/scoutsuite-html-report-overview.png)

---

**ScoutSuite — High Severity Finding Detail**
```
Result:  Specific high-severity misconfiguration finding drilled down in ScoutSuite
```
![ScoutSuite High Severity Finding](./04-cloud-security/screenshots/scoutsuite-specific-high-severity-finding.png)

---

**EC2 IMDS — Metadata Credential Exposure**
```
Technique:  EC2 Instance Metadata Service (IMDSv1) credential retrieval
Context:    Accessed via vulnerable proxy path in CloudGoat lab scenario
Result:     Temporary IAM role credentials retrieved from metadata endpoint
Note:       All credential values fully redacted before publication
```
![IMDS EC2 Metadata Credentials](./04-cloud-security/screenshots/imds-ec2-metadata-credentials-stolen.png)

---

**CloudGoat Cleanup — EC2 Terminated & Verified**
```
Verification:  Target EC2 instance terminated and removed
Tool:          AWS Console + CLI
```
![CloudGoat EC2 Cleanup Verified](./04-cloud-security/screenshots/13-cloudgoat-ec2-cleanup-verified.png)

---

**AWS Billing / Free-Tier Cleanup Check**
```
Verification:  No unexpected charges. Free-tier usage within limits.
               All CloudGoat resources destroyed.
```
![AWS Free Tier Cleanup Check](./04-cloud-security/screenshots/14-aws-free-tier-cleanup-check.png)

---

### AWS Findings Summary

| Finding Area | Category | Context |
|---|---|---|
| IAM misconfigured permissions | Privilege Escalation | CloudGoat scenario |
| PassRole + EC2 RunInstances path | IAM Privesc | Identified by Pacu |
| S3 public unauthenticated access | Misconfiguration | CloudGoat scenario |
| IMDSv1 metadata credential exposure | Credential Access | CloudGoat proxy scenario |
| IAM instance profile assumption | Privilege Escalation | CloudGoat objective met |
| ScoutSuite high-severity findings | Audit/Misconfiguration | Full AWS service audit |

---

## 🔷 Sub-Project 5 — Azure Security Lab

> **Status: ⚠️ Attempted — Blocked by Subscription Quota — Documented & Cleaned Up**

### What Happened

| Step | Outcome |
|------|---------|
| Azure account login | ✅ Successful |
| Azure budget alert configured | ✅ Configured |
| Azure Cloud Shell authenticated | ✅ Successful (Kali CLI had issues; switched to Cloud Shell) |
| AzureGoat repository cloned | ✅ Cloned |
| Terraform deployment initiated | ⚠️ Blocked — Azure subscription quota restrictions |
| Quota errors encountered | App Service Plan limit + Basic Public IP limit exceeded |
| Decision | Did not force deployment — documented as real-world quota constraint |
| Terraform destroy executed | ✅ 14 resources destroyed |
| Resource group `azuregoat_app` | ✅ Deleted and confirmed removed |
| Azure Portal — AzureGoat resources | ✅ Nothing to display — clean |

> This was a deliberate, responsible decision. Forcing a deployment past subscription limits risks unexpected charges and unclean environments. Recognising quota boundaries, documenting the constraint, and performing clean teardown is itself a cloud security and lab management skill.

### Evidence — Screenshots

**Azure CLI — Authenticated in Cloud Shell**
```
Result:  Azure Cloud Shell authenticated successfully after local CLI issues
```
![Azure CLI Authenticated](./05-azure-security/screenshots/01-azure-cli-authenticated.png)

---

**AzureGoat — Deployment Blocked by Subscription Quota**
```
Error:   App Service Plan quota + Basic Public IP quota restrictions
Action:  Deployment halted — Terraform destroy executed immediately
```
![AzureGoat Deployment Blocked](./05-azure-security/screenshots/azuregoat-deployment-blocked-by-subscription-quota.png)

---

**AzureGoat — Cleanup Confirmed**
```
Command:   az group exists --name azuregoat_app → false
Result:    Resource group deleted, no AzureGoat resources in portal
```
![AzureGoat Cleanup Confirmed](./05-azure-security/screenshots/06-azuregoat-cleanup-confirmed.png)

### Skills Demonstrated in Azure Phase

- Azure Portal and Cloud Shell navigation
- Azure CLI authentication and troubleshooting
- Terraform plan, apply, and destroy lifecycle
- Azure subscription quota awareness
- Azure Cost Management and budget alerts
- Responsible resource teardown and cleanup verification

---

## 🌐 Sub-Project 1 — Web Application VAPT

> **Status: 🔄 In Progress** — Lab environment prepared, testing under way

### Planned Targets

| Target | Type | Purpose |
|--------|------|---------|
| DVWA | Docker | OWASP Top 10 fundamentals |
| WebGoat | Docker | Guided vulnerability exercises |
| OWASP Juice Shop | Docker | Full-stack CTF-style VAPT |
| crAPI | Docker | Combined web + API practice |

### Tools Prepared

`Burp Suite` `Nmap` `Gobuster` `ffuf` `Nikto` `SQLMap` `Python`

> Findings, screenshots, and report will be added to `01-web-vapt/` as testing is completed and evidence captured. No findings are pre-claimed.

---

## 🔌 Sub-Project 2 — API Security Testing

> **Status: 🔄 In Progress** — Methodology and tooling structure prepared

### Testing Areas Planned

- REST API authentication and authorisation testing
- JWT token analysis and manipulation
- OWASP API Security Top 10 coverage
- GraphQL introspection and injection testing
- OAuth flow testing
- crAPI vulnerable API lab (in progress)
- PortSwigger Web Security Academy API labs

### Tools Prepared

`Postman` `Burp Suite` `Python requests` `curl` `jq` `JWT analysis tools`

> Findings and screenshots will be added to `02-api-security/` as evidence is captured.

---

## 🟡 GCP Security — Deferred

> **Status: 📅 Deferred — Intentional Decision**

After completing the AWS CloudGoat lab and encountering the Azure subscription quota issue, I made a deliberate decision to defer GCPGoat.

**Reasons:**
- AWS CloudGoat objective was fully completed
- Azure lab exposed real-world quota and billing constraints
- Running a third simultaneous cloud lab increases cost and cleanup risk
- Billing hygiene and cleanup workflow should be validated before adding another cloud

**Planned GCP path (when ready):**
- Create isolated GCP project with billing alerts
- Authenticate via `gcloud` CLI
- IAM and service account enumeration
- Cloud Storage permission review
- Attempt GCPGoat after billing and cleanup workflow is stable

---

## 🛡️ Tools Arsenal

<table>
<tr><th>Category</th><th>Tools Used / Relevant</th></tr>
<tr>
<td>🔴 AD & Network</td>
<td>

`Nmap` `enum4linux-ng` `Responder` `Hashcat` `Impacket` `NetExec` `BloodHound` `Neo4j`

</td>
</tr>
<tr>
<td>☁️ AWS Cloud</td>
<td>

`AWS CLI` `CloudGoat` `Pacu` `ScoutSuite` `Terraform` `curl` `jq`

</td>
</tr>
<tr>
<td>🔷 Azure</td>
<td>

`Azure Portal` `Azure Cloud Shell` `Azure CLI` `Terraform` `Azure Cost Management`

</td>
</tr>
<tr>
<td>🌐 Web (In Progress)</td>
<td>

`Burp Suite` `Nmap` `Gobuster` `ffuf` `Nikto` `SQLMap` `Python`

</td>
</tr>
<tr>
<td>🔌 API (In Progress)</td>
<td>

`Postman` `Burp Suite` `Python requests` `curl` `jq`

</td>
</tr>
</table>

---

## 📋 Methodology & Standards

| Standard / Framework | Application |
|---------------------|-------------|
| OWASP Top 10 (2021) | Web vulnerability testing guidance |
| OWASP API Security Top 10 | API testing methodology |
| MITRE ATT&CK Enterprise | AD and network technique mapping |
| PTES | Overall engagement structure |
| CIS Benchmarks (AWS) | Cloud configuration assessment baseline |
| CVSSv3.1 | Vulnerability severity scoring (when findings confirmed) |

---

## 📸 Evidence Matrix

| Sub-Project | Evidence Type | Count | Redaction Applied |
|-------------|--------------|-------|-------------------|
| AD & Network | Screenshots | 10 | Hashes, passwords, usernames |
| AWS Cloud | Screenshots | 8 | Account IDs, keys, tokens, IPs |
| Azure | Screenshots | 3 | Subscription IDs, tenant info |
| Web VAPT | — | — | In progress |
| API Security | — | — | In progress |

---

## 🔒 Redaction & Secret Handling

All published screenshots and output files follow these rules:

- **Hashes** (NTLMv2, Kerberoast, NTLM) — redacted or blurred before publication
- **AWS account IDs, access keys, secret keys, session tokens** — fully redacted
- **Azure subscription IDs, tenant IDs** — redacted
- **Plaintext passwords** — never shown in published evidence
- **Public IPs, internal IPs** — redacted where identifiable
- **SAM / secretsdump output** — hash fields blurred; structure shown only
- Tool used for redaction: Flameshot (annotate → blur) on Kali Linux

---

## ✅ Cleanup Verification

| Lab | Cleanup Action | Verified |
|-----|---------------|---------|
| AD Lab | Host-only VMs, isolated network — no external exposure | ✅ |
| AWS CloudGoat | `cloudgoat.py destroy` — EC2 terminated, S3 removed | ✅ |
| AWS Pacu / ScoutSuite | No persistent resources created | ✅ |
| AWS Billing | Free-tier usage checked, no unexpected charges | ✅ |
| Azure AzureGoat | `terraform destroy` — 14 resources destroyed | ✅ |
| Azure Resource Group | `az group exists` returned `false` | ✅ |
| Azure Portal | No AzureGoat resources visible | ✅ |

---

## 🎯 Skills Demonstrated

```
Active Directory Security
  ├── Domain lab build from scratch (Windows Server + Win10 + Kali)
  ├── LLMNR/NBT-NS poisoning and NTLMv2 hash capture
  ├── Offline credential cracking (Hashcat)
  ├── SMB enumeration and credential validation
  ├── Kerberoasting using Impacket
  ├── BloodHound attack path analysis and graph visualisation
  ├── Pass-the-Hash lateral movement
  └── DCSync domain hash extraction (private lab)

AWS Cloud Security
  ├── IAM identity and permissions enumeration
  ├── IAM privilege escalation via PassRole + EC2 (CloudGoat)
  ├── Pacu automated privilege escalation scanning
  ├── S3 misconfiguration and public access testing
  ├── EC2 IMDS credential exposure (IMDSv1)
  ├── ScoutSuite full-account security audit
  └── Responsible cleanup and billing verification

Azure / Cloud General
  ├── Azure CLI and Cloud Shell operation
  ├── Terraform lifecycle management (plan → apply → destroy)
  ├── Azure subscription quota awareness
  ├── Azure Cost Management and budget alerts
  └── Safe cloud lab teardown and cleanup verification

General
  ├── Pentest methodology and documentation
  ├── Evidence screenshot capture with redaction
  ├── MITRE ATT&CK technique mapping
  ├── Professional report writing structure
  └── Responsible lab management and ethics
```

---

## 📜 Certification Roadmap

> Full path: [`06-roadmap/certification-roadmap.md`](./06-roadmap/certification-roadmap.md)

| Stage | Certification | Provider | Focus |
|-------|--------------|----------|-------|
| Foundation | Security+ or equivalent | CompTIA | Broad security fundamentals |
| Entry practical | eJPT | eLearnSecurity | Beginner hands-on pentesting |
| Intermediate | PNPT or PenTest+ | TCM Security / CompTIA | Practical pentest methodology |
| Cloud | AWS Security Specialty or AZ-500 | AWS / Microsoft | Cloud security professional |
| Advanced | OSCP | Offensive Security | Gold standard — 24hr practical exam |

---

## 🔮 Future Improvements

- [ ] Complete Web VAPT phase — DVWA + WebGoat + Juice Shop findings
- [ ] Complete API Security phase — crAPI + PortSwigger API labs
- [ ] Resolve Azure quota issue (upgrade tier or request quota increase) and retry AzureGoat
- [ ] Add GCP security lab once billing and cleanup workflow validated
- [ ] Produce formal pentest report (PDF) per sub-project
- [ ] Add Python automation scripts for AD enumeration and cloud IAM review
- [ ] Map all completed findings to MITRE ATT&CK Navigator layer

---

## ⚖️ Legal & Ethical Disclaimer

```
╔══════════════════════════════════════════════════════════════════════╗
║                        IMPORTANT NOTICE                               ║
║                                                                        ║
║  All penetration testing, exploitation, and security testing           ║
║  activities documented in this repository were performed              ║
║  EXCLUSIVELY on:                                                       ║
║                                                                        ║
║  • Self-owned, isolated virtual lab environments                       ║
║  • Intentionally vulnerable software (DVWA, WebGoat, CloudGoat,       ║
║    AzureGoat, Metasploitable) designed for security education          ║
║  • Private AWS and Azure accounts under personal control               ║
║                                                                        ║
║  No real-world systems, third-party infrastructure, or external        ║
║  networks were targeted or accessed without authorisation.             ║
║                                                                        ║
║  Performing these techniques against systems without explicit written  ║
║  permission is illegal under the Computer Misuse Act, CFAA, and       ║
║  equivalent laws worldwide.                                            ║
║                                                                        ║
║  This project exists for EDUCATIONAL PURPOSES ONLY.                   ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

## 📬 Contact

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_PROFILE)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-212C42?style=for-the-badge&logo=tryhackme&logoColor=red)](https://tryhackme.com/p/YOUR_USERNAME)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/YOUR_USERNAME)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0a192f,100:112240&height=120&section=footer&text=&fontColor=64ffda" width="100%"/>

*Built with methodology. Documented with evidence. Conducted with integrity.*

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=YOUR_USERNAME.enterprise-security-assessment-lab&color=64ffda)
&nbsp;
![GitHub Stars](https://img.shields.io/github/stars/YOUR_USERNAME/enterprise-security-assessment-lab?style=social)

</div>
