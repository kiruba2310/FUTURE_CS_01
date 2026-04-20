# FUTURE_CS_01
Vulnerability Assessment Report of the Altoro Mutual demo banking application, conducted using OWASP ZAP, Nmap, and Gobuster. The report identifies 16 security issues including CSRF, missing security headers, and information disclosure, along with recommended mitigations.
# 🔐 Vulnerability Assessment Report – Altoro Mutual

## 📌 Project Overview

This project presents a **security assessment** of the Altoro Mutual demo banking application.
The analysis was performed in a **read-only environment** using industry-standard tools.

---

## 👤 Author

**Kiruba N**
Cybersecurity Intern

---

## 🎯 Objective

To identify security vulnerabilities in a live web application and provide remediation recommendations.

---

## 🌐 Target Application

* **Application Name:** Altoro Mutual
* **URL:** http://demo.testfire.net
* **IP Address:** 65.61.137.117

---

## 🛠️ Tools Used

* OWASP ZAP
* Nmap
* Gobuster

---

## ⚙️ Assessment Scope

* External testing only
* No exploitation performed
* Read-only security analysis

---

## 🚨 Key Findings

A total of **16 vulnerabilities** were identified:

### 🟠 Medium Risk (5)

* CSRF (No anti-CSRF tokens)
* Missing Content Security Policy (CSP)
* Cross-Origin Misconfiguration (CORS)
* Missing X-Frame-Options (Clickjacking risk)
* Subresource Integrity Missing

### 🟡 Low Risk (6)

* Cookies without SameSite attribute
* Server version disclosure
* Missing X-Content-Type-Options
* Missing HSTS header
* Timestamp disclosure

### 🔵 Informational (5)

* Suspicious comments in code
* Session management details exposed
* Cache misconfigurations
* Directory enumeration findings

---

## 🔍 Sample Vulnerability

### Missing Content Security Policy (CSP)

* **Risk:** Medium
* **Impact:** Increased risk of XSS attacks
* **Fix:** Implement strict CSP headers

---

## 📂 Additional Findings

* Open ports: 80, 443, 8080
* Service detected: Apache Tomcat
* Hidden directories: `/admin`, `/bank`, `/static`

---

## 🛡️ Recommendations

* Implement security headers (CSP, HSTS, X-Frame-Options)
* Add CSRF protection
* Restrict CORS policies
* Hide server information
* Secure cookies with SameSite attribute

---

## ✅ Conclusion

The application contains multiple security misconfigurations and a CSRF vulnerability.
Most issues can be resolved through proper configuration, significantly improving security posture.

---

## ⚠️ Disclaimer

This project was conducted for **educational purposes only** in a controlled, legal environment.
No harmful actions were performed.

---
