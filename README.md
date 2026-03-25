# Penetration-Testing-Labs-OSINT-Reconnaissance-and-DVWA-Command-Injection-Analysis

## 📌 Overview

This project demonstrates a complete **penetration testing workflow**, covering:

* Passive reconnaissance (OSINT)
* Web application exploitation (DVWA)
* Source code analysis
* Security remediation

The objective is to simulate a real-world attacker approach while also providing defensive insights.

---

## 🧭 Methodology

The project follows a structured penetration testing lifecycle:

1. **Reconnaissance (OSINT)**
2. **Vulnerability Identification**
3. **Exploitation**
4. **Analysis**
5. **Remediation**

---

## 🔍 Phase 1: OSINT Reconnaissance

Target: Public domain (dublincity.ie)

Tools used:

* WHOIS
* Shodan
* Wayback Machine
* crt.sh
* Google Dorking

### 🎯 Key Findings

* Public infrastructure exposure via Shodan
* Historical data leakage through Wayback Machine
* Subdomain and certificate discovery via crt.sh
* Indexed sensitive information via Google Dorks

👉 Demonstrates how attackers build an **attack surface before exploitation**

---

## 💣 Phase 2: Web Application Exploitation (DVWA)

Target: Damn Vulnerable Web Application (DVWA)

### Attack Type: Command Injection

---

### 🔓 Low Security

* No input validation
* Direct command execution

**Payload:**

```
127.0.0.1; ls
```

✔ Full system command execution

---

### ⚠️ Medium Security

* Partial filtering
* Bypass achieved

**Payload:**

```
127.0.0.1 && ls
```

✔ Filter bypass successful

---

### 🔒 High Security

* Strong validation
* Exploit significantly restricted

✔ Demonstrates effectiveness of secure coding

---

## 🧠 Phase 3: Source Code Analysis

* Identified insecure use of system commands
* Weak input sanitization logic
* Inconsistent validation across security levels

---

## 🛠️ Phase 4: Remediation

Key security improvements:

* Implement strict input validation (whitelisting)
* Avoid direct command execution
* Apply least privilege principle
* Use secure APIs instead of shell execution

---

## 📊 Key Insights

* OSINT significantly expands attack surface before exploitation
* Input validation is the most critical defense layer
* Incremental security controls drastically reduce exploitability
* Secure coding practices outperform reactive patching

---

## 🧰 Tools Used

* Kali Linux
* DVWA
* Browser DevTools
* OSINT tools (WHOIS, Shodan, crt.sh, Wayback Machine)

---

## 📁 Project Structure

* `/01-osint-recon` → reconnaissance findings
* `/02-dvwa-exploitation` → attack execution
* `/03-source-code-analysis` → technical breakdown
* `/04-remediation` → fixes and recommendations

---

## 🚀 Why This Project Matters

This repository demonstrates:

✔ Real penetration testing workflow

✔ Practical exploitation techniques

✔ Ability to think like both attacker and defender

✔ Strong understanding of web application security

---

## ⚠️ Disclaimer

This project is for educational purposes only. All testing was conducted in controlled environments.

---

## 👤 Author

Hsu Shun Lae

MSc Cybersecurity
