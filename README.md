# Enterprise-Security-Assessment-Lab
Enterprise-style cybersecurity lab covering Web VAPT, API Security, Active Directory attacks, Network Pentesting, AWS CloudGoat, AzureGoat, and security reporting.
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,50:1a1a2e,100:16213e&height=300&section=header&text=Enterprise%20Security%20Assessment%20Lab&fontSize=38&fontColor=00d4aa&animation=fadeIn&fontAlignY=38&desc=Web%20%7C%20API%20%7C%20Network%20%7C%20Active%20Directory%20%7C%20Cloud%20Security&descAlignY=58&descSize=16&descColor=8892b0" width="100%"/>

</div>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono\&size=16\&duration=3000\&pause=1000\&color=00D4AA\&center=true\&vCenter=true\&multiline=true\&repeat=true\&width=850\&height=70\&lines=Enterprise+Security+Assessment+Lab;Web+VAPT+%7C+API+Security+%7C+Active+Directory+%7C+Cloud+Security;Practical+Pentesting+%7C+Evidence-Based+Reporting+%7C+Responsible+Cleanup)](https://git.io/typing-svg)

</div>

---

<div align="center">

![Status](https://img.shields.io/badge/Status-Active%20Portfolio%20Project-00d4aa?style=for-the-badge)
![Type](https://img.shields.io/badge/Type-Hands--On%20Security%20Lab-ff6b6b?style=for-the-badge)
![Focus](https://img.shields.io/badge/Focus-Enterprise%20VAPT%20%26%20Cloud%20Security-blue?style=for-the-badge)
![Ethics](https://img.shields.io/badge/Ethics-Authorized%20Labs%20Only-brightgreen?style=for-the-badge)
![Cloud](https://img.shields.io/badge/Cloud-AWS%20%7C%20Azure-orange?style=for-the-badge)

<br/>

![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square\&logo=kalilinux\&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server-0078D6?style=flat-square\&logo=windows\&logoColor=white)
![Windows 10](https://img.shields.io/badge/Windows_10-0078D6?style=flat-square\&logo=windows\&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=flat-square\&logo=amazonaws\&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square\&logo=microsoftazure\&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square\&logo=terraform\&logoColor=white)
![Python](https://img.shields.io/badge/Python_3.x-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Bash](https://img.shields.io/badge/Bash_Scripting-4EAA25?style=flat-square\&logo=gnubash\&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square\&logo=portswigger\&logoColor=white)

</div>

---

## ⚡ What Is This Project?

This repository documents a practical **Enterprise Security Assessment Lab** built to simulate the workflow of a real-world security assessment across multiple environments.

The project includes:

* Web application vulnerability assessment methodology
* API security testing methodology
* Internal network and service enumeration
* Active Directory attack path analysis
* Kerberoasting, DCSync, and Pass-the-Hash validation in a private lab
* AWS IAM and cloud misconfiguration testing
* S3 public access testing
* EC2 Instance Metadata Service credential exposure testing
* ScoutSuite cloud security auditing
* AzureGoat deployment attempt, quota limitation analysis, and cleanup verification
* Security documentation, evidence handling, and GitHub-ready reporting

This project focuses not only on exploitation, but also on **safe lab design, evidence collection, redaction, cleanup, and professional documentation**.

> **Ethical Notice:** All testing was performed only against private lab environments, intentionally vulnerable training targets, or personal cloud lab accounts created for learning. No production systems or third-party assets were tested.

---

## 🧭 Project Scope

| Area                  | Scope                                                 |                             Status |
| --------------------- | ----------------------------------------------------- | ---------------------------------: |
| Web VAPT              | DVWA / WebGoat / Juice Shop style testing methodology |                        In Progress |
| API Security          | crAPI, GraphQL, OAuth lab testing, API automation     |                        In Progress |
| Active Directory      | Private AD domain attack chain                        |                          Completed |
| AWS Cloud Security    | CloudGoat, Pacu, ScoutSuite, S3, IMDS, IAM privesc    |                          Completed |
| Azure Security        | AzureGoat deployment attempt and safe cleanup         | Completed as quota-limited attempt |
| GCP                   | Deferred for safety and cost control                  |                            Planned |
| Certification Roadmap | Personal learning path and future certification order |                          Completed |

---

## 🗺️ Lab Architecture

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ENTERPRISE SECURITY ASSESSMENT LAB                       │
├───────────────────────────────┬───────────────────────────────┬─────────────┤
│        ATTACK PLATFORM         │        INTERNAL LAB            │    CLOUD    │
│                               │                               │             │
│  ┌─────────────────────────┐  │  ┌─────────────────────────┐  │  AWS        │
│  │ Kali Linux              │  │  │ Windows Server DC        │  │  CloudGoat  │
│  │ Burp Suite              │  │  │ corp.local Domain        │  │  Pacu       │
│  │ Nmap / Gobuster / ffuf  │  │  │ AD DS / DNS              │  │  ScoutSuite │
│  │ Impacket / Hashcat      │  │  └───────────┬─────────────┘  │  S3 / IAM   │
│  │ BloodHound / Neo4j      │  │              │                │  EC2 / IMDS │
│  │ AWS CLI / Azure CLI     │  │  ┌───────────▼─────────────┐  │             │
│  └─────────────────────────┘  │  │ Windows 10 Endpoint      │  │  Azure      │
│                               │  │ Domain Joined Workstation│  │  CloudShell │
│  Web/API Targets              │  └─────────────────────────┘  │  AzureGoat  │
│  ├─ DVWA                      │                               │  Terraform  │
│  ├─ WebGoat                   │                               │             │
│  ├─ Juice Shop                │                               │             │
│  └─ crAPI / GraphQL labs      │                               │             │
└───────────────────────────────┴───────────────────────────────┴─────────────┘
```

---

## 📁 Repository Structure

```text
enterprise-security-assessment-lab/
│
├── README.md
├── .gitignore
│
├── 01-web-vapt/
│   ├── README.md
│   ├── screenshots/
│   ├── tool-outputs/
│   └── scripts/
│
├── 02-api-security/
│   ├── README.md
│   ├── screenshots/
│   ├── postman-collections/
│   ├── tools/
│   │   └── api_security_tester.py
│   └── scripts/
│
├── 03-ad-network/
│   ├── README.md
│   ├── screenshots/
│   ├── reports/
│   └── notes/
│
├── 04-cloud-security/
│   ├── README.md
│   ├── screenshots/
│   ├── reports/
│   └── scripts/
│
├── 05-azure-security/
│   ├── README.md
│   ├── screenshots/
│   └── reports/
│
└── 06-roadmap/
    └── certification-roadmap.md
```

---

## 📌 Executive Summary

This project demonstrates practical cybersecurity capability across core enterprise security domains.

The strongest completed sections are:

* **Active Directory attack chain:** NTLMv2 capture, cracking, SMB validation, Kerberoasting, BloodHound, DCSync, and Pass-the-Hash.
* **AWS Cloud Security:** CloudGoat deployment, IAM privilege escalation analysis, S3 public access testing, ScoutSuite reporting, IMDS credential exposure, and cleanup verification.
* **Azure Security:** Azure CLI / Cloud Shell authentication, AzureGoat deployment attempt, quota limitation analysis, Terraform cleanup, and resource group deletion.
* **Professional lab hygiene:** MFA, budget alerts, controlled test environments, redaction of sensitive values, and post-lab billing/resource verification.

The project is designed to show that I can not only run tools, but also build an environment, understand attack paths, document evidence, manage cloud cost risk, and clean up safely.

---

# 🔴 1. Web Application VAPT

## Objective

The web security section focuses on testing intentionally vulnerable web applications using manual and automated methods aligned with OWASP-style testing.

## Target Areas

* Authentication weaknesses
* SQL injection
* Cross-site scripting
* Command injection
* File upload risks
* Directory and file enumeration
* Security misconfiguration
* Sensitive information exposure

## Tools

| Tool            | Purpose                                                  |
| --------------- | -------------------------------------------------------- |
| Burp Suite      | Manual request interception and vulnerability validation |
| Nmap            | Service discovery                                        |
| Gobuster / ffuf | Directory and endpoint brute forcing                     |
| Nikto           | Web server misconfiguration checks                       |
| SQLMap          | SQL injection validation in lab targets                  |
| Python          | Custom automation and helper scripts                     |

## Methodology

```text
Reconnaissance
→ Service fingerprinting
→ Directory enumeration
→ Manual request testing
→ Vulnerability validation
→ Evidence screenshots
→ Remediation notes
```

## Evidence Folder

```text
01-web-vapt/screenshots/
01-web-vapt/tool-outputs/
01-web-vapt/scripts/
```

## Status

This section is structured and ready for evidence population. The goal is to keep this section evidence-based and only list confirmed findings once screenshots and tool outputs are added.

---

# 🟠 2. API Security Testing

## Objective

The API security section focuses on REST, GraphQL, OAuth, JWT, and authorization testing in intentionally vulnerable lab environments.

## Target Areas

* Broken Object Level Authorization
* Broken Authentication
* Excessive Data Exposure
* Rate limiting weaknesses
* Broken Function Level Authorization
* Mass assignment
* GraphQL introspection exposure
* OAuth misconfiguration testing in PortSwigger labs

## Tools

| Tool            | Purpose                                  |
| --------------- | ---------------------------------------- |
| Postman         | API request management                   |
| Burp Suite      | API traffic capture and manipulation     |
| ffuf            | Endpoint fuzzing                         |
| jwt_tool        | JWT analysis                             |
| curl / jq       | API request testing and response parsing |
| Python requests | Custom API scanner automation            |

## Custom API Security Tester

A lightweight Python-based API testing tool was created for lab use.

Planned and supported checks include:

* BOLA / IDOR-style object access testing
* Excessive data exposure keyword checks
* GraphQL introspection testing
* Basic response analysis

Example evidence:

```text
15-python-api-security-scanner-output.png
```

## Methodology

```text
Endpoint discovery
→ Authentication testing
→ Authorization testing
→ JWT inspection
→ GraphQL schema discovery
→ API response review
→ Automation with Python
→ Evidence capture
```

## Evidence Folder

```text
02-api-security/screenshots/
02-api-security/postman-collections/
02-api-security/tools/
```

---

# 🟡 3. Internal Network and Active Directory Pentest

## Objective

The Active Directory section demonstrates an end-to-end internal network attack chain in a private Windows domain lab.

The lab was built using:

* Windows Server Domain Controller
* Windows endpoint
* Kali Linux attack machine
* corp.local domain
* Intentionally configured users, service accounts, and permissions

## Tools Used

| Tool                   | Purpose                                        |
| ---------------------- | ---------------------------------------------- |
| Nmap                   | Host and service discovery                     |
| enum4linux-ng          | SMB and domain enumeration                     |
| Responder              | LLMNR/NBT-NS poisoning and NTLMv2 hash capture |
| Hashcat                | Offline hash cracking                          |
| smbclient              | Manual SMB validation                          |
| NetExec / CrackMapExec | SMB credential validation and enumeration      |
| Impacket               | Kerberoasting, DCSync, Pass-the-Hash           |
| BloodHound             | AD attack path visualization                   |
| Neo4j                  | BloodHound graph database                      |

## Completed AD Attack Chain

```text
Network discovery
→ SMB enumeration
→ NTLMv2 hash capture with Responder
→ Offline cracking with Hashcat
→ Credential validation against Domain Controller
→ Kerberoasting service account ticket request
→ Kerberoast hash cracking
→ BloodHound collection and graph analysis
→ DCSync validation
→ Pass-the-Hash validation
→ SYSTEM/domain compromise evidence
```

## Evidence Screenshots

| Screenshot                                     | Purpose                                       |
| ---------------------------------------------- | --------------------------------------------- |
| `10-responder-ntlmv2-hash-captured.png`        | Captured NetNTLMv2 hash in lab                |
| `11-hashcat-ntlmv2-cracked.png`                | Cracked captured NetNTLMv2 hash               |
| `12-smb-enumeration-credential-validation.png` | Validated credentials against SMB/DC          |
| `13-kerberoasting-spn-ticket-requested.png`    | Requested Kerberoastable SPN ticket           |
| `14-kerberoast-hash-cracked.png`               | Cracked Kerberoast hash                       |
| `15-bloodhound-attack-path-domain-admin.png`   | BloodHound path to Domain Admins              |
| `16-bloodhound-domain-overview-graph.png`      | AD domain overview graph                      |
| `17-pass-the-hash-system-shell-obtained.png`   | SYSTEM shell through pass-the-hash validation |
| `18-dcsync-domain-hashes-dumped.png`           | Limited DCSync output                         |
| `18b-dcsync-all-domain-hashes-dumped.png`      | Full lab DCSync output with hashes redacted   |

## Screenshot Gallery

> All screenshots must be redacted before publishing. Full hashes, passwords, tokens, and private values should not be visible.

![Responder NTLMv2 Capture](./03-ad-network/screenshots/10-responder-ntlmv2-hash-captured.png)

![Hashcat NTLMv2 Cracked](./03-ad-network/screenshots/11-hashcat-ntlmv2-cracked.png)

![SMB Enumeration and Credential Validation](./03-ad-network/screenshots/12-smb-enumeration-credential-validation.png)

![Kerberoasting SPN Ticket Requested](./03-ad-network/screenshots/13-kerberoasting-spn-ticket-requested.png)

![Kerberoast Hash Cracked](./03-ad-network/screenshots/14-kerberoast-hash-cracked.png)

![BloodHound Attack Path](./03-ad-network/screenshots/15-bloodhound-attack-path-domain-admin.png)

![BloodHound Domain Overview](./03-ad-network/screenshots/16-bloodhound-domain-overview-graph.png)

![Pass-the-Hash SYSTEM Shell](./03-ad-network/screenshots/17-pass-the-hash-system-shell-obtained.png)

![DCSync Domain Hashes Dumped](./03-ad-network/screenshots/18-dcsync-domain-hashes-dumped.png)

![Full DCSync Lab Output](./03-ad-network/screenshots/18b-dcsync-all-domain-hashes-dumped.png)

## AD Security Lessons

Key lessons demonstrated:

* Weak passwords can turn captured NTLMv2 hashes into valid domain credentials.
* LLMNR/NBT-NS should be disabled in enterprise environments.
* Service accounts with weak passwords are dangerous when Kerberoastable.
* BloodHound is valuable for identifying privilege paths before exploitation.
* Domain Admin or replication privileges can allow DCSync.
* DCSync can expose krbtgt material, which could enable Golden Ticket attacks if abused.
* Passwords, hashes, Kerberos tickets, and secrets must be redacted before reporting.

---

# ☁️ 4. AWS Cloud Security Assessment

## Objective

The AWS section demonstrates cloud misconfiguration testing and IAM privilege escalation concepts using CloudGoat and supporting tools in a private AWS training account.

## Safety Controls Used

* MFA enabled on root account
* Budget alert configured
* Dedicated IAM user for lab operations
* Lab resources deployed only temporarily
* CloudGoat destroyed after testing
* EC2, S3, IAM, and billing/free-tier cleanup verified
* Access keys, secret keys, tokens, and public identifiers redacted

## Tools Used

| Tool       | Purpose                                 |
| ---------- | --------------------------------------- |
| AWS CLI    | Authentication, enumeration, validation |
| CloudGoat  | Vulnerable AWS lab scenarios            |
| Pacu       | AWS privilege escalation scanning       |
| ScoutSuite | AWS security audit reporting            |
| curl / jq  | IMDS and API response testing           |
| Terraform  | CloudGoat infrastructure deployment     |
| Firefox    | Report and console evidence capture     |

## Completed AWS Work

| Area                                          |    Status |
| --------------------------------------------- | --------: |
| AWS CLI authentication                        | Completed |
| MFA and budget setup                          | Completed |
| CloudGoat deployment                          | Completed |
| IAM permissions enumeration                   | Completed |
| Pacu privilege escalation scan                | Completed |
| S3 unauthenticated access test                | Completed |
| ScoutSuite HTML report overview               | Completed |
| ScoutSuite detailed finding screenshot        | Completed |
| IMDS credential exposure via vulnerable proxy | Completed |
| IAM instance profile privilege escalation     | Completed |
| Target EC2 termination objective              | Completed |
| AWS cleanup and billing verification          | Completed |

## AWS Evidence Screenshots

| Screenshot                                      | Purpose                                              |
| ----------------------------------------------- | ---------------------------------------------------- |
| `iam-permissions-enumeration.png`               | IAM permissions / identity enumeration               |
| `pacu-privesc-scan-results.png`                 | Pacu IAM privilege escalation scan output            |
| `s3-public-bucket-unauthenticated-access.png`   | Public/unauthenticated S3 access test                |
| `scoutsuite-html-report-overview.png`           | ScoutSuite dashboard overview                        |
| `scoutsuite-specific-high-severity-finding.png` | Detailed ScoutSuite finding                          |
| `imds-ec2-metadata-credentials-stolen.png`      | IMDS credential exposure proof with secrets redacted |
| `13-cloudgoat-ec2-cleanup-verified.png`         | EC2 cleanup verification                             |
| `14-aws-free-tier-cleanup-check.png`            | Billing/free-tier verification                       |

## Screenshot Gallery

![IAM Permissions Enumeration](./04-cloud-security/screenshots/iam-permissions-enumeration.png)

![Pacu Privilege Escalation Scan](./04-cloud-security/screenshots/pacu-privesc-scan-results.png)

![S3 Public Bucket Unauthenticated Access](./04-cloud-security/screenshots/s3-public-bucket-unauthenticated-access.png)

![ScoutSuite HTML Report Overview](./04-cloud-security/screenshots/scoutsuite-html-report-overview.png)

![ScoutSuite High Severity Finding](./04-cloud-security/screenshots/scoutsuite-specific-high-severity-finding.png)

![IMDS Metadata Credentials Exposure](./04-cloud-security/screenshots/imds-ec2-metadata-credentials-stolen.png)

![CloudGoat EC2 Cleanup Verified](./04-cloud-security/screenshots/13-cloudgoat-ec2-cleanup-verified.png)

![AWS Free Tier Cleanup Check](./04-cloud-security/screenshots/14-aws-free-tier-cleanup-check.png)

## AWS Attack Path Summary

```text
Low-privileged CloudGoat user
→ IAM permission enumeration
→ Pacu privilege escalation scan
→ Instance profile role manipulation
→ Privileged EC2 role assumption
→ Target resource access
→ Objective completion
→ Cleanup and billing verification
```

## Key AWS Findings Demonstrated

| Finding                                  | Service               | Risk                                                                   |
| ---------------------------------------- | --------------------- | ---------------------------------------------------------------------- |
| IAM privilege escalation path identified | IAM                   | Excessive or dangerous IAM permissions can enable privilege escalation |
| Public/unauthenticated S3 access tested  | S3                    | Misconfigured buckets may expose sensitive data                        |
| IMDS credential exposure via proxy       | EC2 / IMDS            | SSRF-style access can expose temporary role credentials                |
| ScoutSuite security findings reviewed    | Multiple AWS services | Misconfigurations require continuous auditing                          |
| Lab cleanup verified                     | AWS account hygiene   | Cloud resources can create cost and exposure if left running           |

## AWS Security Lessons

* IAM permissions should follow least privilege.
* Privilege escalation risks must be reviewed before assigning IAM actions.
* Public S3 access should be blocked unless explicitly required.
* IMDSv2 should be enforced wherever possible.
* Temporary credentials are still sensitive and must be protected.
* Cloud labs should never be left running after testing.
* Billing, budgets, and cleanup checks are part of responsible cloud security practice.

---

# 🔵 5. Azure Security Assessment

## Objective

The Azure section focused on safely attempting AzureGoat deployment in a private Azure subscription using Azure CLI, Azure Cloud Shell, and Terraform.

## Tools Used

| Tool              | Purpose                                      |
| ----------------- | -------------------------------------------- |
| Azure Portal      | Subscription, budget, and resource review    |
| Azure Cloud Shell | Browser-based authenticated terminal         |
| Azure CLI         | Azure authentication and resource operations |
| Terraform         | AzureGoat deployment and cleanup             |
| Cost Management   | Budget and cost monitoring                   |

## Result

AzureGoat deployment was attempted, but the subscription blocked required resources due to quota limitations.

Observed issues included:

* App Service Plan quota restriction
* Basic Public IP quota restriction
* Subscription-level limitations on resource deployment

The deployment was not forced. The partial deployment was cleaned up with Terraform, and the `azuregoat_app` resource group was deleted.

## Azure Evidence Screenshots

| Screenshot                                               | Purpose                                                 |
| -------------------------------------------------------- | ------------------------------------------------------- |
| `01-azure-cli-authenticated.png`                         | Azure CLI / Cloud Shell authentication                  |
| `azuregoat-deployment-blocked-by-subscription-quota.png` | Deployment blocked by Azure quota                       |
| `06-azuregoat-cleanup-confirmed.png`                     | Terraform cleanup and resource group deletion confirmed |

## Screenshot Gallery

![Azure CLI Authenticated](./05-azure-security/screenshots/01-azure-cli-authenticated.png)

![AzureGoat Deployment Blocked by Subscription Quota](./05-azure-security/screenshots/azuregoat-deployment-blocked-by-subscription-quota.png)

![AzureGoat Cleanup Confirmed](./05-azure-security/screenshots/06-azuregoat-cleanup-confirmed.png)

## Azure Security Lessons

* Cloud subscriptions can have quota limitations that affect lab deployment.
* Failed deployments must still be cleaned up properly.
* Azure Cloud Shell can be safer than a broken local CLI environment.
* Terraform destroy and resource group deletion should be verified.
* Responsible cloud security includes cost awareness, quotas, cleanup, and documentation.

---

# 🟢 6. GCP Status

GCPGoat was intentionally deferred.

Reason:

* AWS CloudGoat was already completed.
* AzureGoat hit real subscription quota limitations.
* Running multiple vulnerable cloud labs at once increases cost and cleanup risk.
* The current project already demonstrates strong cloud security skills using AWS and Azure.

Planned future GCP practice:

```text
Create isolated GCP project
→ Configure budget alert
→ Authenticate with gcloud
→ Enumerate IAM and service accounts
→ Review Cloud Storage permissions
→ Practise safer GCP labs
→ Attempt GCPGoat only after billing and cleanup workflow is mature
```

This demonstrates a responsible decision to avoid unnecessary cloud cost and risk.

---

# 🧪 Evidence Matrix

| Area              | Evidence Type                            |    Status |
| ----------------- | ---------------------------------------- | --------: |
| AD NTLMv2 capture | Responder screenshot                     | Completed |
| AD hash cracking  | Hashcat screenshot                       | Completed |
| AD SMB validation | SMB / NetExec / CME evidence             | Completed |
| Kerberoasting     | Impacket + Hashcat evidence              | Completed |
| BloodHound        | Attack path and graph screenshots        | Completed |
| DCSync            | Redacted hash dump evidence              | Completed |
| Pass-the-Hash     | SYSTEM shell evidence                    | Completed |
| AWS IAM           | Permission enumeration evidence          | Completed |
| AWS Pacu          | Privilege escalation scan evidence       | Completed |
| AWS S3            | Public access test evidence              | Completed |
| AWS ScoutSuite    | HTML report and finding evidence         | Completed |
| AWS IMDS          | Metadata credential exposure evidence    | Completed |
| AWS cleanup       | EC2, S3, billing verification            | Completed |
| Azure             | Auth, quota limitation, cleanup evidence | Completed |

---

# 🛠️ Complete Tools Arsenal

<table>
<tr><th>Category</th><th>Tools</th></tr>

<tr>
<td>🌐 Web Pentesting</td>
<td>

![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square\&logo=portswigger\&logoColor=white)
![SQLMap](https://img.shields.io/badge/SQLMap-C23B22?style=flat-square)
![Nikto](https://img.shields.io/badge/Nikto-5C4033?style=flat-square)
![Gobuster](https://img.shields.io/badge/Gobuster-3DDC84?style=flat-square)
![ffuf](https://img.shields.io/badge/ffuf-005571?style=flat-square)

</td>
</tr>

<tr>
<td>🔌 API Security</td>
<td>

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square\&logo=postman\&logoColor=white)
![JWT](https://img.shields.io/badge/JWT_Testing-000000?style=flat-square)
![GraphQL](https://img.shields.io/badge/GraphQL_Testing-E10098?style=flat-square\&logo=graphql\&logoColor=white)
![Python](https://img.shields.io/badge/Python_Requests-3776AB?style=flat-square\&logo=python\&logoColor=white)

</td>
</tr>

<tr>
<td>🏢 Active Directory</td>
<td>

![BloodHound](https://img.shields.io/badge/BloodHound-DC143C?style=flat-square)
![Impacket](https://img.shields.io/badge/Impacket-2E4057?style=flat-square\&logo=python\&logoColor=white)
![Responder](https://img.shields.io/badge/Responder-8B0000?style=flat-square)
![Hashcat](https://img.shields.io/badge/Hashcat-374151?style=flat-square)
![NetExec](https://img.shields.io/badge/NetExec-4A0E0E?style=flat-square)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat-square\&logo=neo4j\&logoColor=white)

</td>
</tr>

<tr>
<td>☁️ Cloud Security</td>
<td>

![AWS CLI](https://img.shields.io/badge/AWS_CLI-FF9900?style=flat-square\&logo=amazonaws\&logoColor=white)
![Azure CLI](https://img.shields.io/badge/Azure_CLI-0078D4?style=flat-square\&logo=microsoftazure\&logoColor=white)
![CloudGoat](https://img.shields.io/badge/CloudGoat-FF6347?style=flat-square)
![AzureGoat](https://img.shields.io/badge/AzureGoat-0078D4?style=flat-square)
![Pacu](https://img.shields.io/badge/Pacu-FF4500?style=flat-square)
![ScoutSuite](https://img.shields.io/badge/ScoutSuite-1E90FF?style=flat-square)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square\&logo=terraform\&logoColor=white)

</td>
</tr>

</table>

---

# 📚 Methodology and Standards

| Standard / Framework      | How It Applies                                     |
| ------------------------- | -------------------------------------------------- |
| OWASP Top 10              | Web application security testing methodology       |
| OWASP API Security Top 10 | API testing methodology and risk categories        |
| MITRE ATT&CK              | AD and cloud attack technique mapping              |
| PTES                      | Overall penetration testing workflow               |
| NIST SP 800-115           | Technical security testing guidance                |
| CIS Benchmarks            | Cloud and configuration baseline reference         |
| CVSS v3.1                 | Severity scoring reference for documented findings |

---

# 🎓 Skills Demonstrated

```text
┌───────────────────────────────────────────────┬───────────────────────────────┐
│ Skill Area                                    │ Evidence                       │
├───────────────────────────────────────────────┼───────────────────────────────┤
│ Active Directory enumeration                  │ SMB, BloodHound, domain recon  │
│ Credential attack validation                  │ NTLMv2, Hashcat, Kerberoasting │
│ AD privilege path analysis                    │ BloodHound attack paths        │
│ Domain compromise simulation                  │ DCSync and PTH in private lab  │
│ AWS IAM security testing                      │ CloudGoat and Pacu             │
│ Cloud misconfiguration validation             │ S3, IMDS, ScoutSuite           │
│ Cloud cleanup and billing awareness           │ EC2/S3/IAM/billing checks      │
│ Azure cloud operations                        │ CLI, Cloud Shell, Terraform    │
│ Evidence handling                             │ Redaction and screenshots      │
│ Professional documentation                    │ GitHub-ready report structure  │
└───────────────────────────────────────────────┴───────────────────────────────┘
```

---

# 🧾 Reports and Documentation

Formal PDF reports are planned as future improvements. Current documentation is maintained through Markdown files, screenshot evidence, and lab notes.

| Document                              | Purpose                                 |                Status |
| ------------------------------------- | --------------------------------------- | --------------------: |
| `README.md`                           | Main project overview                   |             Completed |
| `03-ad-network/README.md`             | AD lab documentation                    | Planned / In Progress |
| `04-cloud-security/README.md`         | AWS cloud security documentation        | Planned / In Progress |
| `05-azure-security/README.md`         | Azure attempt and cleanup documentation | Planned / In Progress |
| `06-roadmap/certification-roadmap.md` | Certification and learning path         |             Completed |

---

# 🚀 How to Reproduce the Lab

## General Requirements

```text
Host System: Windows, Linux, or macOS
Virtualization: VirtualBox or VMware
RAM: 16 GB recommended for AD lab
Storage: 80 GB minimum, 150 GB+ recommended
Cloud: Separate AWS/Azure lab account or subscription
Security: MFA and budget alerts required for cloud labs
```

## Web / API Lab

```bash
# Example vulnerable targets for controlled local testing
docker pull vulnerables/web-dvwa
docker pull bkimminich/juice-shop
git clone https://github.com/OWASP/crAPI.git
```

## Active Directory Lab

The AD lab requires:

* Windows Server evaluation VM
* Windows endpoint VM
* Kali Linux VM
* Host-only lab network
* Created domain users and service accounts
* Intentionally controlled misconfigurations

## AWS Cloud Lab

Cloud labs must be run only in a dedicated training account.

Required safety controls:

```text
MFA enabled
Budget alert enabled
Dedicated IAM user
No production resources
Immediate cleanup after testing
Billing check after cleanup
```

## Azure Lab

AzureGoat was attempted through Azure Cloud Shell and Terraform. Deployment was blocked by subscription quotas, and cleanup was verified.

---

# 🔐 Redaction and Secret Handling

Before publishing screenshots or files, redact:

* AWS account ID
* Azure subscription ID
* Azure tenant ID
* Email addresses
* Access keys
* Secret keys
* Session tokens
* JWTs
* NTLM hashes
* Kerberos hashes
* Passwords
* Private keys
* `.pem` files
* Cloud resource IDs where sensitive
* Full public IPs if privacy is required

This repository should never include:

```text
.env files
.pem files
Terraform state files
AWS credential files
Azure profile files
Full hash dumps
DCSync raw dumps
Session tokens
Cloud secret keys
```

---

# ✅ Cleanup Verification

## AWS Cleanup Completed

AWS cleanup checks included:

```text
CloudGoat destroy
EC2 instance termination check
S3 bucket cleanup check
IAM role cleanup check
Free Tier / billing check
Budget status check
```

## Azure Cleanup Completed

Azure cleanup checks included:

```text
Terraform destroy
azuregoat_app resource group deletion
Azure Portal resource group verification
Budget and billing review
```

---

# 🧠 Certification Roadmap

A certification roadmap was created to guide future learning.

Recommended path:

```text
Security+ or equivalent fundamentals
→ eJPT or beginner practical pentesting
→ PNPT-style practical path or PenTest+
→ AWS Security Specialty or AZ-500
→ OSCP later after stronger fundamentals
```

Roadmap file:

```text
06-roadmap/certification-roadmap.md
```

---

# 🧩 Future Improvements

Planned improvements:

* Complete Web VAPT screenshots and reporting
* Complete API Security screenshots and Postman collection exports
* Add formal PDF reports for each sub-project
* Add final executive summary report
* Add MITRE ATT&CK technique mapping table
* Add CVSS scoring tables for confirmed findings
* Add remediation sections for every confirmed issue
* Add GCP mini-lab only after billing and cleanup workflow is mature

---

# 📬 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-YOUR_USERNAME-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/YOUR_USERNAME)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-YOUR_PROFILE-0077B5?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://linkedin.com/in/YOUR_PROFILE)
[![Email](https://img.shields.io/badge/Email-your@email.com-D14836?style=for-the-badge\&logo=gmail\&logoColor=white)](mailto:your@email.com)

</div>

---

# ⚖️ Legal Disclaimer

This repository is for educational and authorized security testing only.

All techniques shown here must only be used in environments where explicit permission has been granted. Unauthorized testing against third-party systems is illegal and unethical.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:16213e,100:0d1117&height=100&section=footer&text=&fontColor=00d4aa" width="100%"/>

**Built with discipline. Documented with evidence. Practised ethically.**

![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=YOUR_USERNAME.enterprise-security-assessment-lab\&color=00d4aa)
![GitHub Stars](https://img.shields.io/github/stars/YOUR_USERNAME/enterprise-security-assessment-lab?style=social)
![GitHub Forks](https://img.shields.io/github/forks/YOUR_USERNAME/enterprise-security-assessment-lab?style=social)

</div>
