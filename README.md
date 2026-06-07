# Enterprise-Security-Assessment-Lab
Enterprise-style cybersecurity lab covering Web VAPT, API Security, Active Directory attacks, Network Pentesting, AWS CloudGoat, AzureGoat, and security reporting.
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,50:101827,100:16213e&height=300&section=header&text=Enterprise%20Security%20Assessment%20Lab&fontSize=38&fontColor=00d4aa&animation=fadeIn&fontAlignY=38&desc=Active%20Directory%20%7C%20AWS%20Cloud%20Security%20%7C%20Azure%20Security%20%7C%20Web%20%26%20API%20VAPT&descAlignY=58&descSize=15&descColor=8892b0" width="100%"/>

</div>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono\&size=16\&duration=3000\&pause=1000\&color=00D4AA\&center=true\&vCenter=true\&multiline=true\&repeat=true\&width=900\&height=80\&lines=Enterprise+Security+Assessment+Lab;Active+Directory+Attack+Path+Analysis+%7C+AWS+CloudGoat+%7C+Azure+Cloud+Security;Evidence-Based+Pentesting+%7C+Cloud+Cleanup+%7C+Professional+Reporting)](https://git.io/typing-svg)

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
![Active Directory](https://img.shields.io/badge/Active_Directory-003B57?style=flat-square\&logo=windows\&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=flat-square\&logo=amazonaws\&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square\&logo=microsoftazure\&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square\&logo=terraform\&logoColor=white)
![Python](https://img.shields.io/badge/Python_3.x-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Bash](https://img.shields.io/badge/Bash_Scripting-4EAA25?style=flat-square\&logo=gnubash\&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square\&logo=portswigger\&logoColor=white)

</div>

---

## ⚡ Project Summary

This repository documents a practical **Enterprise Security Assessment Lab** built to demonstrate hands-on cybersecurity skills across internal network security, Active Directory attacks, AWS cloud security, Azure security, and structured VAPT documentation.

The project is focused on **evidence-based security testing**. Every completed section is supported with screenshots, tool outputs, cleanup verification, and notes explaining what was tested, what was observed, and what security lesson was learned.

This lab demonstrates the ability to:

* Build and operate a private enterprise-style security lab
* Perform internal network and Active Directory enumeration
* Validate common AD attack paths in a controlled environment
* Perform AWS IAM and cloud misconfiguration testing
* Use CloudGoat, Pacu, ScoutSuite, AWS CLI, and Terraform
* Test S3 public exposure and EC2 metadata credential exposure
* Attempt AzureGoat deployment safely and handle real subscription quota limits
* Clean up real cloud resources responsibly to avoid cost and exposure
* Document security evidence in a GitHub-ready professional format

> **Ethical Notice:** All testing was performed only in private lab environments, intentionally vulnerable training labs, or personal cloud accounts created for learning. No third-party or production systems were tested.

---

## 🧭 Current Project Status

| Area                                |                               Status | What Was Done                                                                           |
| ----------------------------------- | -----------------------------------: | --------------------------------------------------------------------------------------- |
| Active Directory / Internal Network |                          ✅ Completed | AD lab built, enumeration, Kerberoasting, BloodHound, DCSync, Pass-the-Hash             |
| AWS Cloud Security                  |                          ✅ Completed | CloudGoat, Pacu, ScoutSuite, S3, IMDS, IAM privilege escalation, cleanup                |
| Azure Security                      | ✅ Completed as quota-limited attempt | Azure CLI/Cloud Shell auth, AzureGoat attempt, quota issue documented, cleanup verified |
| API Security                        |                       🟡 In Progress | GraphQL/API testing workflow and custom scanner structure prepared                      |
| Web VAPT                            |                       🟡 In Progress | Web testing structure prepared for DVWA/WebGoat/Juice Shop style labs                   |
| GCP                                 |                           ⏳ Deferred | Intentionally postponed to avoid running multiple billable vulnerable cloud labs        |
| Certification Roadmap               |                          ✅ Completed | Practical learning and certification path documented                                    |

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
│  │ Nmap / SMB tools        │  │  │ corp.local Domain        │  │  Pacu       │
│  │ Responder / Hashcat     │  │  │ AD DS / DNS              │  │  ScoutSuite │
│  │ BloodHound / Neo4j      │  │  └───────────┬─────────────┘  │  S3 / IAM   │
│  │ Impacket / NetExec      │  │              │                │  EC2 / IMDS │
│  │ AWS CLI / Azure CLI     │  │  ┌───────────▼─────────────┐  │             │
│  └─────────────────────────┘  │  │ Windows 10 Endpoint      │  │  Azure      │
│                               │  │ Domain-joined machine    │  │  CloudShell │
│  Web/API Practice Targets     │  └─────────────────────────┘  │  AzureGoat  │
│  ├─ DVWA / WebGoat            │                               │  Terraform  │
│  ├─ Juice Shop                │                               │             │
│  ├─ crAPI                     │                               │             │
│  └─ GraphQL / OAuth labs      │                               │             │
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

# 🟡 1. Internal Network and Active Directory Pentest

## Objective

The Active Directory section demonstrates an end-to-end internal network attack chain in a private Windows domain lab. The goal was to understand how weak credentials, misconfigurations, excessive privileges, and poor hardening can lead to domain compromise.

## Lab Environment

| Component         | Details                                              |
| ----------------- | ---------------------------------------------------- |
| Domain            | `corp.local`                                         |
| Domain Controller | Windows Server                                       |
| Endpoint          | Windows 10 domain-joined workstation                 |
| Attack Machine    | Kali Linux                                           |
| Network Type      | Private lab network                                  |
| Users / Groups    | Intentionally configured test users and privileges   |
| Purpose           | Controlled AD enumeration and attack path validation |

## Tools Used

| Tool                      | Purpose                                |
| ------------------------- | -------------------------------------- |
| Nmap                      | Host discovery and service enumeration |
| enum4linux-ng / SMB tools | SMB and domain enumeration             |
| Responder                 | NTLMv2 hash capture in lab             |
| Hashcat                   | Offline hash cracking                  |
| smbclient                 | Manual SMB validation                  |
| NetExec / CrackMapExec    | SMB authentication and enumeration     |
| Impacket                  | Kerberoasting, DCSync, Pass-the-Hash   |
| BloodHound                | AD attack path visualization           |
| Neo4j                     | BloodHound graph database              |

## Completed AD Attack Chain

```text
Network discovery
→ SMB enumeration
→ NTLMv2 hash capture with Responder
→ Offline hash cracking with Hashcat
→ Credential validation
→ Kerberoasting ticket request
→ Kerberoast hash cracking
→ BloodHound collection and graph analysis
→ Domain Admin path validation
→ DCSync testing
→ Pass-the-Hash validation
→ SYSTEM shell / domain compromise evidence
```

## AD Evidence Screenshots

| Screenshot                                     | Purpose                                               |
| ---------------------------------------------- | ----------------------------------------------------- |
| `10-responder-ntlmv2-hash-captured.png`        | Captured NetNTLMv2 hash in the private lab            |
| `11-hashcat-ntlmv2-cracked.png`                | Cracked captured NetNTLMv2 hash                       |
| `12-smb-enumeration-credential-validation.png` | Validated credentials against SMB/DC                  |
| `13-kerberoasting-spn-ticket-requested.png`    | Requested Kerberoastable SPN ticket                   |
| `14-kerberoast-hash-cracked.png`               | Cracked Kerberoast hash                               |
| `15-bloodhound-attack-path-domain-admin.png`   | BloodHound path to Domain Admins                      |
| `16-bloodhound-domain-overview-graph.png`      | AD domain overview graph                              |
| `17-pass-the-hash-system-shell-obtained.png`   | Pass-the-Hash validation and SYSTEM shell             |
| `18-dcsync-domain-hashes-dumped.png`           | Limited DCSync evidence with hashes redacted          |
| `18b-dcsync-all-domain-hashes-dumped.png`      | Full lab DCSync output with sensitive values redacted |

## AD Screenshot Gallery

> All screenshots should be redacted before publishing. Do not expose full hashes, passwords, tickets, or private identifiers.

![Responder NTLMv2 Hash Captured](./03-ad-network/screenshots/10-responder-ntlmv2-hash-captured.png)

![Hashcat NTLMv2 Cracked](./03-ad-network/screenshots/11-hashcat-ntlmv2-cracked.png)

![SMB Enumeration and Credential Validation](./03-ad-network/screenshots/12-smb-enumeration-credential-validation.png)

![Kerberoasting SPN Ticket Requested](./03-ad-network/screenshots/13-kerberoasting-spn-ticket-requested.png)

![Kerberoast Hash Cracked](./03-ad-network/screenshots/14-kerberoast-hash-cracked.png)

![BloodHound Attack Path](./03-ad-network/screenshots/15-bloodhound-attack-path-domain-admin.png)

![BloodHound Domain Overview Graph](./03-ad-network/screenshots/16-bloodhound-domain-overview-graph.png)

![Pass-the-Hash SYSTEM Shell](./03-ad-network/screenshots/17-pass-the-hash-system-shell-obtained.png)

![DCSync Domain Hashes Dumped](./03-ad-network/screenshots/18-dcsync-domain-hashes-dumped.png)

![Full DCSync Lab Output](./03-ad-network/screenshots/18b-dcsync-all-domain-hashes-dumped.png)

## Key AD Lessons

* Weak passwords can turn captured NTLMv2 hashes into valid domain credentials.
* LLMNR/NBT-NS can expose credentials through name resolution poisoning.
* Kerberoastable service accounts should use long, complex passwords.
* BloodHound is useful for identifying privilege escalation paths.
* DCSync access can expose domain credential material.
* krbtgt material could enable Golden Ticket attacks if abused, so it must be protected carefully.
* Hashes, tickets, passwords, and secrets must be redacted before public reporting.

---

# ☁️ 2. AWS Cloud Security Assessment

## Objective

The AWS section demonstrates practical cloud misconfiguration testing and IAM privilege escalation concepts using intentionally vulnerable AWS lab environments.

## Safety Controls Used

| Control                                     | Status |
| ------------------------------------------- | -----: |
| AWS root MFA enabled                        | ✅ Done |
| Budget alert configured                     | ✅ Done |
| Dedicated lab IAM user created              | ✅ Done |
| CloudGoat deployed only temporarily         | ✅ Done |
| CloudGoat resources destroyed after testing | ✅ Done |
| Billing / Free Tier checked after cleanup   | ✅ Done |
| Access keys, tokens, and hashes redacted    | ✅ Done |

## Tools Used

| Tool       | Purpose                                     |
| ---------- | ------------------------------------------- |
| AWS CLI    | Authentication, enumeration, and validation |
| CloudGoat  | Vulnerable AWS lab scenarios                |
| Pacu       | AWS privilege escalation scanning           |
| ScoutSuite | AWS security audit reporting                |
| Terraform  | Lab deployment and destruction              |
| curl / jq  | IMDS and API response testing               |
| Firefox    | Console and report evidence capture         |

## Completed AWS Work

| Area                                          |      Status |
| --------------------------------------------- | ----------: |
| AWS CLI authentication                        | ✅ Completed |
| IAM permissions enumeration                   | ✅ Completed |
| Pacu privilege escalation scan                | ✅ Completed |
| S3 unauthenticated access test                | ✅ Completed |
| ScoutSuite HTML report overview               | ✅ Completed |
| ScoutSuite detailed finding review            | ✅ Completed |
| IMDS credential exposure via vulnerable proxy | ✅ Completed |
| IAM instance profile privilege escalation     | ✅ Completed |
| Target EC2 termination objective              | ✅ Completed |
| AWS EC2 cleanup verification                  | ✅ Completed |
| AWS Free Tier / billing verification          | ✅ Completed |

## AWS Evidence Screenshots

| Screenshot                                      | Purpose                                              |
| ----------------------------------------------- | ---------------------------------------------------- |
| `iam-permissions-enumeration.png`               | IAM identity and permission enumeration              |
| `pacu-privesc-scan-results.png`                 | Pacu IAM privilege escalation scan output            |
| `s3-public-bucket-unauthenticated-access.png`   | S3 unauthenticated access test                       |
| `scoutsuite-html-report-overview.png`           | ScoutSuite report dashboard                          |
| `scoutsuite-specific-high-severity-finding.png` | ScoutSuite detailed security finding                 |
| `imds-ec2-metadata-credentials-stolen.png`      | IMDS credential exposure proof with secrets redacted |
| `13-cloudgoat-ec2-cleanup-verified.png`         | EC2 cleanup verification                             |
| `14-aws-free-tier-cleanup-check.png`            | Free Tier / billing cleanup verification             |

## AWS Screenshot Gallery

![IAM Permissions Enumeration](./04-cloud-security/screenshots/iam-permissions-enumeration.png)

![Pacu Privilege Escalation Scan](./04-cloud-security/screenshots/pacu-privesc-scan-results.png)

![S3 Public Bucket Unauthenticated Access](./04-cloud-security/screenshots/s3-public-bucket-unauthenticated-access.png)

![ScoutSuite HTML Report Overview](./04-cloud-security/screenshots/scoutsuite-html-report-overview.png)

![ScoutSuite Specific Finding](./04-cloud-security/screenshots/scoutsuite-specific-high-severity-finding.png)

![IMDS Credential Exposure](./04-cloud-security/screenshots/imds-ec2-metadata-credentials-stolen.png)

![CloudGoat EC2 Cleanup Verified](./04-cloud-security/screenshots/13-cloudgoat-ec2-cleanup-verified.png)

![AWS Free Tier Cleanup Check](./04-cloud-security/screenshots/14-aws-free-tier-cleanup-check.png)

## AWS Attack Path Summary

```text
CloudGoat low-privileged user
→ IAM permission enumeration
→ Pacu privilege escalation scan
→ Instance profile role manipulation
→ Privileged EC2 role assumption
→ Target EC2 objective completed
→ CloudGoat cleanup
→ Billing and Free Tier verification
```

## Key AWS Findings Demonstrated

| Finding                       | Service     | Risk                                                     |
| ----------------------------- | ----------- | -------------------------------------------------------- |
| IAM privilege escalation path | IAM         | Excessive IAM permissions can allow privilege escalation |
| S3 public access exposure     | S3          | Misconfigured buckets can expose sensitive data          |
| IMDS credential exposure      | EC2 / IMDS  | SSRF-style access can expose temporary role credentials  |
| ScoutSuite security findings  | AWS Account | Automated auditing can identify cloud misconfigurations  |
| Cloud cleanup verification    | AWS Account | Unused lab resources create cost and security risk       |

## AWS Security Lessons

* IAM permissions should follow least privilege.
* S3 public access must be reviewed and restricted.
* EC2 metadata exposure can leak temporary credentials.
* IMDSv2 should be enforced wherever possible.
* Temporary cloud credentials are sensitive and must be redacted.
* Cloud labs should be destroyed immediately after testing.
* Billing verification is part of responsible cloud security work.

---

# 🔵 3. Azure Security Assessment

## Objective

The Azure section focused on safely attempting AzureGoat deployment in a private Azure subscription using Azure Portal, Azure Cloud Shell, Azure CLI, and Terraform.

## Tools Used

| Tool              | Purpose                                      |
| ----------------- | -------------------------------------------- |
| Azure Portal      | Subscription, budget, and resource review    |
| Azure Cloud Shell | Browser-based authenticated terminal         |
| Azure CLI         | Azure authentication and resource operations |
| Terraform         | AzureGoat deployment and cleanup             |
| Cost Management   | Budget and cost monitoring                   |

## What Was Completed

| Step                                    |      Status |
| --------------------------------------- | ----------: |
| Azure account login                     | ✅ Completed |
| Budget setup                            | ✅ Completed |
| Azure CLI / Cloud Shell authentication  | ✅ Completed |
| AzureGoat Terraform deployment attempt  | ✅ Completed |
| Quota limitation identified             | ✅ Completed |
| Terraform cleanup                       | ✅ Completed |
| `azuregoat_app` resource group deletion | ✅ Completed |
| Portal cleanup verification             | ✅ Completed |

## AzureGoat Result

AzureGoat deployment was attempted, but the Azure subscription blocked required resources due to quota limitations.

Observed issues included:

* App Service Plan quota restriction
* Basic Public IP quota restriction
* Subscription-level lab deployment limitation

The deployment was not forced. Partial resources were destroyed with Terraform, and the `azuregoat_app` resource group was deleted.

## Azure Evidence Screenshots

| Screenshot                                               | Purpose                                                 |
| -------------------------------------------------------- | ------------------------------------------------------- |
| `01-azure-cli-authenticated.png`                         | Azure Cloud Shell / CLI authentication                  |
| `azuregoat-deployment-blocked-by-subscription-quota.png` | AzureGoat blocked by subscription quota                 |
| `06-azuregoat-cleanup-confirmed.png`                     | Terraform destroy and resource group deletion confirmed |

## Azure Screenshot Gallery

![Azure CLI Authenticated](./05-azure-security/screenshots/01-azure-cli-authenticated.png)

![AzureGoat Deployment Blocked by Subscription Quota](./05-azure-security/screenshots/azuregoat-deployment-blocked-by-subscription-quota.png)

![AzureGoat Cleanup Confirmed](./05-azure-security/screenshots/06-azuregoat-cleanup-confirmed.png)

## Azure Security Lessons

* Cloud subscription quotas can block lab deployment.
* Failed deployments still require cleanup.
* Azure Cloud Shell can be more reliable than a broken local CLI environment.
* Terraform destroy should be verified.
* Resource groups should be checked after cleanup.
* Budget and billing monitoring are required for real cloud labs.

---

# 🟠 4. API Security Work

## Objective

The API security section is focused on learning and documenting API testing methods using safe lab environments.

## Work Prepared

| Area                           |                    Status |
| ------------------------------ | ------------------------: |
| GraphQL introspection workflow |               🟡 Prepared |
| GraphQL query testing process  |               🟡 Prepared |
| OAuth lab testing workflow     |               🟡 Prepared |
| Python API security tester     | 🟡 Prepared / In Progress |
| crAPI testing workflow         |  🟡 Planned / In Progress |

## Testing Areas

* BOLA / IDOR-style object access
* Excessive data exposure
* JWT handling
* GraphQL introspection
* GraphQL field discovery
* OAuth parameter review in PortSwigger labs
* API response keyword analysis

## Planned Evidence

| Screenshot                                      | Purpose                          |
| ----------------------------------------------- | -------------------------------- |
| `12-graphql-introspection-schema-discovery.png` | GraphQL schema discovery         |
| `13-graphql-user-data-query-test.png`           | Querying discovered fields       |
| `14-oauth-lab-burp-request-analysis.png`        | OAuth request analysis in Burp   |
| `15-python-api-security-scanner-output.png`     | Custom Python API scanner output |

## Security Note

Real OAuth providers such as Google, Microsoft, Facebook, and production applications are not tested. OAuth testing is planned only inside PortSwigger Web Security Academy labs or intentionally vulnerable local environments.

---

# 🌐 5. Web VAPT Work

## Objective

The Web VAPT section is prepared for structured testing against intentionally vulnerable web applications.

## Planned Targets

* DVWA
* WebGoat
* OWASP Juice Shop
* Local Docker-based vulnerable applications

## Testing Areas

* Authentication weakness testing
* SQL injection validation
* XSS testing
* File upload checks
* Directory enumeration
* Security misconfiguration review
* Sensitive information exposure

## Tools

| Tool            | Purpose                                 |
| --------------- | --------------------------------------- |
| Burp Suite      | Manual request interception and testing |
| Nmap            | Service discovery                       |
| Gobuster / ffuf | Directory enumeration                   |
| Nikto           | Web server checks                       |
| SQLMap          | SQL injection validation in lab targets |
| Python          | Custom helper scripts                   |

## Status

This section is intentionally marked **In Progress**. Findings will be added only after screenshots and tool output evidence are captured.

---

# 🟢 6. GCP Status

GCPGoat was intentionally deferred.

## Reason

* AWS CloudGoat was already completed.
* AzureGoat hit real subscription quota limitations.
* Running multiple vulnerable cloud labs at the same time increases cost and cleanup risk.
* The current project already demonstrates AWS and Azure cloud security handling.

## Future GCP Plan

```text
Create isolated GCP project
→ Configure budget alert
→ Authenticate with gcloud
→ Enumerate IAM and service accounts
→ Review Cloud Storage permissions
→ Practise safer GCP labs
→ Attempt GCPGoat only after billing workflow is mature
```

This decision demonstrates responsible cloud lab management.

---

# 🧪 Evidence Matrix

| Area              | Evidence Type                            |         Status |
| ----------------- | ---------------------------------------- | -------------: |
| AD NTLMv2 capture | Responder screenshot                     |    ✅ Completed |
| AD hash cracking  | Hashcat screenshot                       |    ✅ Completed |
| AD SMB validation | SMB evidence                             |    ✅ Completed |
| Kerberoasting     | Impacket + Hashcat evidence              |    ✅ Completed |
| BloodHound        | Attack path and graph screenshots        |    ✅ Completed |
| DCSync            | Redacted hash dump evidence              |    ✅ Completed |
| Pass-the-Hash     | SYSTEM shell evidence                    |    ✅ Completed |
| AWS IAM           | Permission enumeration evidence          |    ✅ Completed |
| AWS Pacu          | Privilege escalation scan evidence       |    ✅ Completed |
| AWS S3            | Public access test evidence              |    ✅ Completed |
| AWS ScoutSuite    | HTML report and finding evidence         |    ✅ Completed |
| AWS IMDS          | Metadata credential exposure evidence    |    ✅ Completed |
| AWS cleanup       | EC2 and billing verification             |    ✅ Completed |
| Azure             | Auth, quota limitation, cleanup evidence |    ✅ Completed |
| API               | GraphQL/OAuth/scanner workflow           | 🟡 In Progress |
| Web               | VAPT workflow                            | 🟡 In Progress |

---

# 🛠️ Tools Arsenal

<table>
<tr><th>Category</th><th>Tools Used / Prepared</th></tr>

<tr>
<td>🏢 Active Directory</td>
<td>

![BloodHound](https://img.shields.io/badge/BloodHound-DC143C?style=flat-square)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat-square\&logo=neo4j\&logoColor=white)
![Impacket](https://img.shields.io/badge/Impacket-2E4057?style=flat-square\&logo=python\&logoColor=white)
![Responder](https://img.shields.io/badge/Responder-8B0000?style=flat-square)
![Hashcat](https://img.shields.io/badge/Hashcat-374151?style=flat-square)
![NetExec](https://img.shields.io/badge/NetExec-4A0E0E?style=flat-square)
![Nmap](https://img.shields.io/badge/Nmap-0E83CD?style=flat-square)

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

<tr>
<td>🔌 API Security</td>
<td>

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square\&logo=postman\&logoColor=white)
![JWT](https://img.shields.io/badge/JWT_Testing-000000?style=flat-square)
![GraphQL](https://img.shields.io/badge/GraphQL_Testing-E10098?style=flat-square\&logo=graphql\&logoColor=white)
![Python](https://img.shields.io/badge/Python_Requests-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square\&logo=portswigger\&logoColor=white)

</td>
</tr>

<tr>
<td>🌐 Web VAPT</td>
<td>

![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square\&logo=portswigger\&logoColor=white)
![SQLMap](https://img.shields.io/badge/SQLMap-C23B22?style=flat-square)
![Nikto](https://img.shields.io/badge/Nikto-5C4033?style=flat-square)
![Gobuster](https://img.shields.io/badge/Gobuster-3DDC84?style=flat-square)
![ffuf](https://img.shields.io/badge/ffuf-005571?style=flat-square)

</td>
</tr>

</table>

---

# 📚 Methodology and Standards

| Standard / Framework      | Application                                      |
| ------------------------- | ------------------------------------------------ |
| OWASP Top 10              | Web application testing methodology              |
| OWASP API Security Top 10 | API testing methodology                          |
| MITRE ATT&CK              | AD and cloud attack technique mapping            |
| PTES                      | General penetration testing workflow             |
| NIST SP 800-115           | Security testing guidance                        |
| CIS Benchmarks            | Cloud configuration review reference             |
| CVSS v3.1                 | Planned scoring reference for confirmed findings |

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
│ Azure cloud operations                        │ Cloud Shell, CLI, Terraform    │
│ Evidence handling                             │ Redaction and screenshots      │
│ Professional documentation                    │ GitHub-ready report structure  │
└───────────────────────────────────────────────┴───────────────────────────────┘
```

---

# 🧾 Documentation Status

Formal PDF reports are planned as future improvements. Current documentation is maintained through Markdown files, screenshot evidence, and lab notes.

| Document                              | Purpose                                 |         Status |
| ------------------------------------- | --------------------------------------- | -------------: |
| `README.md`                           | Main project overview                   |    ✅ Completed |
| `03-ad-network/README.md`             | AD lab documentation                    | 🟡 In Progress |
| `04-cloud-security/README.md`         | AWS cloud documentation                 | 🟡 In Progress |
| `05-azure-security/README.md`         | Azure attempt and cleanup documentation | 🟡 In Progress |
| `06-roadmap/certification-roadmap.md` | Certification and learning path         |    ✅ Completed |

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
* Terraform state data
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
Private keys
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

* Complete Web VAPT screenshots and tool outputs
* Complete API Security screenshots and Postman collection exports
* Add formal Markdown reports for each sub-project
* Add final executive summary document
* Add MITRE ATT&CK technique mapping table
* Add CVSS scoring only for confirmed findings
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
