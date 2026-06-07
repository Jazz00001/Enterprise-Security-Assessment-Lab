# Enterprise-Security-Assessment-Lab
Enterprise-style cybersecurity lab covering Web VAPT, API Security, Active Directory attacks, Network Pentesting, AWS CloudGoat, AzureGoat, and security reporting.
# Enterprise Security Assessment Lab  
## Web, API, Network, Active Directory & Cloud VAPT

> A full-stack cybersecurity lab simulating an enterprise environment with vulnerable web applications, APIs, Active Directory infrastructure, internal network attacks, and cloud misconfigurations.

---

## Project Objective

The objective of this project was to build and assess a realistic enterprise-style security lab covering multiple attack surfaces:

- Web Application VAPT
- API Security Testing
- Network Enumeration and Exploitation
- Active Directory Misconfiguration Attacks
- AWS Cloud Security Assessment
- Azure Cloud Security Practice
- Professional Security Reporting and Remediation

This project was completed in a controlled private lab environment for educational and portfolio purposes.

---

## Lab Scope

| Area | Environment | Main Focus |
|---|---|---|
| Web VAPT | DVWA, WebGoat | SQLi, XSS, command injection, file upload, CSRF |
| API Security | crAPI, DVGA, Postman | JWT, BOLA, IDOR, mass assignment, rate limiting, GraphQL |
| AD / Network | Kali, Windows Server DC, Windows Endpoint | SMB, LLMNR poisoning, NTLMv2, Kerberoasting, BloodHound, DCSync |
| Cloud Security | AWS CloudGoat, ScoutSuite, Pacu, AzureGoat | IAM misconfiguration, privilege escalation, S3, metadata credentials, cleanup |
| Reporting | Markdown reports | Findings, evidence, risk, remediation |

---

## Lab Architecture

The lab included the following systems:

| System | Role |
|---|---|
| Kali Linux | Attacker machine and security testing workstation |
| Windows Server DC1 | Domain Controller for `corp.local` |
| Windows Endpoint | Domain-joined workstation |
| Metasploitable / DVWA | Vulnerable web target |
| crAPI | Vulnerable API lab |
| DVGA | Vulnerable GraphQL lab |
| AWS CloudGoat | Vulnerable AWS IAM scenario |
| AzureGoat | Vulnerable Azure security practice lab |

---

## Tools Used

| Category | Tools |
|---|---|
| Recon | Nmap, WhatWeb, Nikto, Gobuster |
| Web Testing | Burp Suite, SQLMap, John the Ripper |
| API Testing | Postman, ffuf, Kiterunner, JWT.io |
| AD Testing | Responder, Hashcat, NetExec, Impacket, BloodHound |
| Cloud Security | AWS CLI, CloudGoat, Pacu, ScoutSuite, Azure CLI, AzureGoat |
| Documentation | Markdown, Flameshot, GitHub |

---

## Project Phases

### 1. Web Application VAPT

Covered DVWA/WebGoat testing including:

- Reconnaissance and fingerprinting
- SQL Injection manual proof
- SQLMap database enumeration
- Password hash cracking demonstration
- Burp Suite request modification
- Reflected and Stored XSS
- Command Injection
- File Upload leading to webshell execution
- CSRF password change proof

See: [`01-web-vapt`](./01-web-vapt)

---

### 2. API Security Testing

Covered API testing using crAPI, Postman, JWT analysis, and GraphQL:

- crAPI deployment
- JWT login and token decoding
- BOLA / IDOR testing
- Excessive data exposure
- Rate limiting test using ffuf
- Mass assignment testing
- API endpoint discovery
- GraphQL introspection and data query testing

See: [`02-api-security`](./02-api-security)

---

### 3. Active Directory & Network Pentesting

Covered internal network and AD attack paths:

- Domain Controller setup
- Domain-joined Windows endpoint
- AD users and groups
- Nmap AD port enumeration
- Responder NTLMv2 capture
- Hashcat cracking demonstration
- SMB enumeration
- Kerberoasting
- BloodHound attack path analysis
- Pass-the-Hash
- DCSync attack demonstration

See: [`03-ad-network`](./03-ad-network)

---

### 4. Cloud Security Assessment

Covered AWS and Azure cloud security practice:

- AWS CLI authentication
- CloudGoat scenario deployment
- IAM role and instance profile enumeration
- Pacu privilege escalation analysis
- S3 access testing
- ScoutSuite cloud audit
- EC2 metadata credential exposure demonstration
- Azure CLI authentication
- AzureGoat deployment and cleanup

See: [`04-cloud-security`](./04-cloud-security)

---

## Key Findings Summary

| ID | Area | Finding | Severity |
|---|---|---|---|
| WEB-01 | Web | SQL Injection allowed database enumeration | Critical |
| WEB-02 | Web | Command Injection allowed OS command execution | Critical |
| WEB-03 | Web | File Upload allowed webshell execution | Critical |
| API-01 | API | BOLA/IDOR allowed access to another user's data | Critical |
| API-02 | API | Excessive data exposure leaked hidden fields | Medium |
| AD-01 | AD | Weak domain credentials were crackable | High |
| AD-02 | AD | Kerberoasting exposed service account risk | High |
| AD-03 | AD | Misconfigured privileges enabled domain compromise | Critical |
| CLOUD-01 | Cloud | Over-permissive IAM role enabled privilege escalation path | Critical |
| CLOUD-02 | Cloud | EC2 metadata service exposed temporary credentials | Critical |
| CLOUD-03 | Cloud | Cloud audit identified encryption and security group issues | High |

---

## Evidence Handling

All screenshots and outputs in this repository are redacted. The following sensitive data was removed before publishing:

- Passwords
- Hashes
- JWT tokens
- Session cookies
- AWS access keys
- Secret keys
- Session tokens
- Cloud account IDs
- Azure tenant/subscription IDs
- Public IP addresses
- Private key files

---

## Disclaimer

This project was performed entirely in a controlled lab environment using intentionally vulnerable systems and private cloud lab scenarios. No unauthorized systems were tested. The purpose of this repository is education, ethical security practice, and portfolio demonstration.

---

## Author

Rimanshu Sharma  
Cybersecurity Portfolio Project
