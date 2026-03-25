# 🔐 Certificate Transparency Analysis – crt.sh

## 📌 Overview

crt.sh was used to analyse SSL/TLS certificates associated with **dublincity.ie**, revealing:

* Subdomains
* Certificate history
* Infrastructure changes

---

## Screenshots

<img width="734" height="444" alt="image" src="https://github.com/user-attachments/assets/9d9c5bb2-635a-4dc4-abd3-333cd04473ab" />

<img width="766" height="358" alt="image" src="https://github.com/user-attachments/assets/3c60080a-0fec-4a7b-b5ce-be03fa0a2618" />

<img width="761" height="380" alt="image" src="https://github.com/user-attachments/assets/61854383-8412-4147-807b-3911de424544" />

<img width="760" height="298" alt="image" src="https://github.com/user-attachments/assets/9985dc95-d419-410e-a58a-ae57645a84c4" />

---

## 🔍 Certificate Overview

* Certificates issued between **2020 – 2025**
* Issuers include:

  * Google Trust Services
  * Let’s Encrypt
  * DigiCert Inc
  * Amazon RSA

### 🔍 Analysis

* Multiple issuers → evolving infrastructure
* Indicates:

  * Migration between providers
  * Changes in hosting/security strategies

---

## 🌐 Subdomain Enumeration

Discovered subdomains:

* uat.dublincity.ie
* training.dublincity.ie
* events.dublincity.ie
* consult.dublincity.ie
* whatsthestory.dublincity.ie
* alerts.dublincity.ie
* libraries.dublincity.ie
* hgv.dublincity.ie
* engage.dublincity.ie
* consultation.dublincity.ie

---

## ⚠️ Security Analysis

### 🔹 Development Environments

* `uat`, `training`

👉 Risk:

* Often poorly secured
* May expose test data or vulnerabilities

---

### 🔹 Public Services

* `events`, `alerts`, `libraries`

👉 Risk:

* Multiple entry points
* Increased attack surface

---

## 🔐 Wildcard Certificates

* `*.dublincity.ie`

### ⚠️ Risk

* If compromised → affects all subdomains

---

## 📊 Key Takeaways

* Certificate logs reveal **hidden infrastructure**
* Subdomains significantly expand attack surface
* Historical certificates show infrastructure evolution

---

## 🧠 Final Insight

crt.sh enables attackers to:

* Discover hidden endpoints
* Map subdomain architecture
* Identify weak or forgotten services

👉 It is one of the most powerful tools for **passive reconnaissance**.
