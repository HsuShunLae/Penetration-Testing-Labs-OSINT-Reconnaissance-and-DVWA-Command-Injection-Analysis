# 🌐 Shodan Analysis – dublincity.ie

## 📌 Overview

A Shodan scan was performed on the public-facing infrastructure of **[www.dublincity.ie](http://www.dublincity.ie)** to identify exposed services, server configurations, and potential security risks.

Shodan provides real-world visibility into:

* Open ports and services
* Server technologies
* SSL/TLS configurations
* Fingerprinting data

---

## Screenshots

<img width="713" height="319" alt="image" src="https://github.com/user-attachments/assets/e31a9326-6072-4a6f-ad05-238dd27bd7e8" />


<img width="709" height="317" alt="image" src="https://github.com/user-attachments/assets/9967f7f0-470e-4f90-800c-8845cd33e2ff" />


---

## 🔍 Target Identification

| Attribute  | Value                     |
| ---------- | ------------------------- |
| IP Address | 137.191.238.56            |
| Hostname   | h137-191-238-56.gn.gov.ie |
| Location   | Fairview, Ireland         |
| Ownership  | Irish Government          |

### 🧠 Insight

The hostname and IP association confirm that the infrastructure is part of a **government-managed network**, increasing its importance as a high-value target.

---

## 🌐 Open Ports & Services

| Port | Service | Description        |
| ---- | ------- | ------------------ |
| 443  | HTTPS   | Secure web traffic |

### 🔍 Analysis

* Only **port 443** is exposed → good security practice
* Indicates **minimal attack surface at network level**
* No unnecessary services exposed

---

## 🖥️ Server Technology Stack

| Component   | Value              |
| ----------- | ------------------ |
| Web Server  | Microsoft IIS/10.0 |
| Framework   | ASP.NET            |
| Environment | Windows Server     |

### 🔍 Analysis

* IIS + ASP.NET → common enterprise stack
* Potential risks:

  * Known IIS vulnerabilities (if unpatched)
  * Misconfigured ASP.NET endpoints

---

## 🔐 SSL/TLS Configuration

| Attribute        | Value                      |
| ---------------- | -------------------------- |
| Certificate Type | Wildcard (*.dublincity.ie) |
| Issuer           | DigiCert Inc               |
| Protocols        | TLS 1.2, TLS 1.3           |

### 🔍 Analysis

* Trusted certificate authority (**DigiCert**)
* Modern protocols → strong encryption
* Wildcard certificate:

  * Covers all subdomains
  * But increases risk if private key is compromised

---

## 🔁 HTTP Behavior

* Server returns **HTTP 302 redirect**

### 🔍 Analysis

* Likely enforces HTTPS or redirects to secure endpoints
* Good practice for:

  * Preventing plaintext traffic
  * Ensuring secure browsing

---

## 🧬 Fingerprinting Data

| Type             | Value                               |
| ---------------- | ----------------------------------- |
| JA3S Fingerprint | 08d08d00000000000042d00042da53957d… |
| JARM Fingerprint | 79c7fe91f79d5f9d5dfb530895689381    |

### 🔍 Analysis

* Used for:

  * TLS fingerprinting
  * Server identification
  * Threat intelligence correlation

👉 Attackers can use this to:

* Identify similar servers
* Detect specific configurations
* Match known vulnerabilities

---

## ⚠️ Security Considerations

Even with strong configuration, the following risks exist:

### 1. Technology Exposure

* IIS/ASP.NET versions visible → enables targeted attacks

### 2. Wildcard Certificate Risk

* Compromise affects all subdomains

### 3. Fingerprinting Data

* Enables reconnaissance and profiling

### 4. Government Infrastructure

* High-value target for:

  * DDoS attacks
  * Advanced persistent threats (APT)

---

## 📊 Key Takeaways

* Minimal exposed surface (only HTTPS) → strong baseline security
* Proper TLS configuration with modern encryption
* Enterprise-grade infrastructure (IIS + ASP.NET)
* However, metadata exposure still provides **valuable reconnaissance data**

---

## 🧠 Final Insight

Shodan analysis demonstrates that even well-secured systems expose **critical metadata** that can be leveraged by attackers for:

* Target profiling
* Vulnerability identification
* Attack planning
