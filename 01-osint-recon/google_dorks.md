# 🔎 Google Dorking Analysis – dublincity.ie

## 📌 Overview

Google Dorking was used to identify publicly indexed sensitive information across the domain.

Techniques used:

* `site:*.dublincity.ie inurl:login OR inurl:admin`
* `site:www.dublincity.ie "@dublincity.ie"`

---

## 🔐 Login & Admin Interfaces

### 🔹 Discovered Portals

* citizenhub.dublincity.ie
* alerts.dublincity.ie
* hgv.dublincity.ie
* consult.dublincity.ie
* whatsthestory.dublincity.ie
* careers.dublincity.ie

---

## ⚠️ Security Impact

* Multiple login endpoints increase attack surface
* Potential targets for:

  * Brute-force attacks
  * Credential stuffing

---

## 📧 Email Enumeration

### 🔹 Department Emails

Examples:

* [customerservices@dublincity.ie](mailto:customerservices@dublincity.ie)
* [hsgapplications@dublincity.ie](mailto:hsgapplications@dublincity.ie)
* [dataprotection@dublincity.ie](mailto:dataprotection@dublincity.ie)
* [press@dublincity.ie](mailto:press@dublincity.ie)

---

### 🔹 Personal Emails (Exposed)

* [marie.kavanagh@dublincity.ie](mailto:marie.kavanagh@dublincity.ie)
* [liam.barry@dublincity.ie](mailto:liam.barry@dublincity.ie)

---

## 📞 Contact Information

Discovered:

* Multiple direct phone numbers
* Department-specific contact details

---

## 📄 Indexed Documents

* PDF files containing:

  * Emails
  * Contact data
  * Internal information

---

## ⚠️ Security Risks

### 🔹 Social Engineering

* Email + phone = phishing targets

### 🔹 Information Leakage

* Sensitive data publicly indexed

### 🔹 Attack Surface Expansion

* Multiple exposed services and portals

---

## 📊 Key Takeaways

* Search engines can expose **sensitive organizational data**
* Public indexing increases risk of:

  * Phishing
  * Reconnaissance
  * Targeted attacks

---

## 🧠 Final Insight

Google Dorking highlights that:

👉 **Security is not just about systems, but also about what is publicly exposed**

Improper indexing can:

* Leak sensitive data
* Reveal attack vectors
* Assist attackers without active scanning

---

## 🚀 Conclusion

Google Dorking is a powerful OSINT technique that enables attackers to:

* Discover hidden endpoints
* Extract sensitive information
* Map organizational structure

👉 Emphasising the importance of **secure content management and indexing controls**.
