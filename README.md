# Week 6 – Web Security & Vulnerability Assessment (VAPT)

## 📌 Overview

This project was completed as part of **Week 6: Web Security & Vulnerability Testing (VAPT Basics)**.

The objective of this project was to understand common web application vulnerabilities and perform basic vulnerability testing in a controlled and authorized laboratory environment.

The practical assessment was performed primarily against **Damn Vulnerable Web Application (DVWA)**, an intentionally vulnerable web application designed for security testing and learning.

---

## 🎯 Objectives

The main objectives of this project were:

- Understand the fundamentals of Vulnerability Assessment and Penetration Testing (VAPT).
- Study selected OWASP Top 10 web application vulnerabilities.
- Set up DVWA in a local testing environment.
- Perform SQL Injection testing.
- Perform Reflected and Stored XSS testing.
- Capture and analyze HTTP requests and responses using Burp Suite.
- Perform automated vulnerability scanning using OWASP ZAP.
- Identify vulnerabilities and assign appropriate risk levels.
- Understand mitigation techniques for identified vulnerabilities.
- Document the complete testing process with screenshots and reports.

---

## 🔐 Vulnerabilities Studied

The following vulnerabilities were studied:

### 1. SQL Injection

SQL Injection occurs when untrusted user input is incorporated into SQL queries without proper validation or parameterization.

**Potential impact:**
- Unauthorized data access
- Authentication bypass
- Data modification or deletion
- Exposure of sensitive database information

### 2. Cross-Site Scripting (XSS)

XSS occurs when an application processes untrusted input in a way that allows malicious JavaScript to execute in a user's browser.

The project covered:

- Reflected XSS
- Stored XSS
- Basic understanding of DOM-based XSS

### 3. Broken Authentication

Broken authentication involves weaknesses in login, session management, password handling, or authentication controls.

**Examples:**
- Weak credentials
- Lack of rate limiting
- Poor session management
- Missing multi-factor authentication

### 4. Security Misconfiguration

Security misconfiguration occurs when security settings are incorrectly implemented or default/unnecessary configurations remain enabled.

**Examples:**
- Default credentials
- Verbose error messages
- Unnecessary services
- Missing security headers
- Outdated components

---

## 🧰 Tools Used

| Tool | Purpose |
|------|---------|
| DVWA | Intentionally vulnerable web application for testing |
| Burp Suite Community Edition | HTTP request interception and manual testing |
| OWASP ZAP | Automated web vulnerability scanning |
| XAMPP | Local Apache, PHP and MySQL/MariaDB environment |
| Firefox | Web browser used for testing |
| FoxyProxy | Proxy switching between browser and security tools |

---

## 🖥️ Lab Environment

The DVWA application was configured in a local testing environment using XAMPP.

### Environment Components

- **Web Server:** Apache
- **Database:** MySQL/MariaDB
- **Application:** DVWA
- **Browser:** Firefox
- **Proxy:** Burp Suite / OWASP ZAP
- **Testing Environment:** Local and controlled lab

DVWA was configured with the **Low** security level for initial vulnerability testing.

The security level can also be changed to Medium, High, and Impossible to observe how different security controls affect vulnerability exploitation.

---

## 🧪 Testing Performed

### SQL Injection

The DVWA SQL Injection module was tested by submitting normal input followed by SQL Injection payloads.

The objective was to determine whether user input could alter the underlying SQL query and expose unintended database information.

Evidence is included in the project report under the SQL Injection testing section.

---

### Reflected XSS

The Reflected XSS module was tested using a harmless JavaScript alert payload.

Example:

```text
<script>alert('Reflected XSS')</script>
