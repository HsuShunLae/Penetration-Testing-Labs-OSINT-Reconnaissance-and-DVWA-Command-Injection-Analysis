# 🕰️ Wayback Machine Analysis – dublincity.ie

## 📌 Overview

The Wayback Machine was used to analyse historical snapshots of **[www.dublincity.ie](http://www.dublincity.ie)** to identify:

* Legacy endpoints
* Exposed data
* Deprecated features
* Historical security configurations

---
Screenshots

<img width="720" height="161" alt="image" src="https://github.com/user-attachments/assets/421ed942-370a-408f-923d-c7880f3920de" />

<img width="1103" height="354" alt="image" src="https://github.com/user-attachments/assets/ebc78555-6097-444f-b3e9-86e899ebcb41" />

<img width="763" height="354" alt="image" src="https://github.com/user-attachments/assets/64f66aee-da45-435b-9d1d-0dcf24ebdb9e" />

<img width="707" height="365" alt="image" src="https://github.com/user-attachments/assets/9a88b0f5-987c-4356-b193-eff892d8314d" />

<img width="769" height="332" alt="image" src="https://github.com/user-attachments/assets/a162b244-5d38-445d-bc40-4a0c924e8b52" />

<img width="660" height="323" alt="image" src="https://github.com/user-attachments/assets/32e81adf-c839-43a8-8e23-da304b694831" />

---

## 📂 Discovered Historical Artifacts

### 🔹 `.well-known` Directory

Identified files:

* `security.txt`
* `trust.txt`
* `dnt-policy.txt`
* `ai-plugin.json`
* `assetlinks.json`
* `gpc.json`

### 🔍 Analysis

* These files indicate **previous implementation of security and privacy standards**
* Currently:

  * Returning **4xx errors**
  * Redirecting to homepage

👉 Suggests:

* Cleanup or restructuring
* Possible removal of outdated configurations

---

## 👥 Historical User Data Exposure (2014)

### 🔹 Accessibility Forum

Discovered:

* Login page
* Active users page
* User profile pages

### 🔍 Exposed Information

* Usernames
* Browser details (e.g., IE 8.0)
* Operating systems (WinXP, WinNT)
* Join dates and last login times

### ⚠️ Security Impact

* Enables **user environment fingerprinting**
* Potential for:

  * Targeted attacks
  * Credential reuse attacks

---

## 📧 Contact Information Exposure (2023)

### 🔹 Animal Welfare Page

Exposed:

* Email: `animalwelfare@dublincity.ie`
* Multiple phone numbers
* Office hours and voicemail instructions

### ⚠️ Security Impact

* Useful for:

  * Social engineering
  * Phishing campaigns

---

## 🗺️ Site Structure Analysis

### 🔹 Identified Directories

* `/events`
* `/business`
* `/council`
* `/residential`
* `/culturenearyou`
* `/find`
* `/ga`

### 🔍 Analysis

* Reveals **organizational structure**
* Helps attackers:

  * Map application logic
  * Identify high-value endpoints

---

## 🏢 Additional Contact Exposure

Discovered:

* Address: Civic Offices, Dublin 8
* Phone: 01 222 2222
* Email: [customerservices@dublincity.ie](mailto:customerservices@dublincity.ie)

---

## 📊 Key Takeaways

* Historical snapshots expose **data no longer available publicly**
* Legacy systems may contain **unpatched vulnerabilities**
* Sensitive information (emails, users) was previously accessible

---

## 🧠 Final Insight

The Wayback Machine demonstrates that:

👉 **“Removed does not mean gone”**

Historical data can:

* Reveal attack vectors
* Provide reconnaissance intelligence
* Expose sensitive information long after removal

This makes it a **powerful OSINT tool for attackers**.
