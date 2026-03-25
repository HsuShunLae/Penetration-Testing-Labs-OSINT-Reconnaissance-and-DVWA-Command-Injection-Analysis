# 🧠 Source Code Analysis – Command Injection (DVWA)

## 📌 Overview

This section analyses the **underlying source code implementation** of the command injection vulnerability in DVWA across different security levels.

The goal is to understand:

* Why the vulnerability exists
* How it is exploited
* How security controls improve protection

---

## 🔍 Vulnerable Code Pattern (Low Security)

### Logic

```php
system("ping " . $_GET['ip']);
```

---

## ⚠️ Root Cause

* User input is directly concatenated into a system command
* No validation or sanitisation
* The system executes arbitrary input

---

## 💣 Why This is Dangerous

* Allows **command injection**
* Enables attackers to execute:

  * File system commands
  * Network commands
  * Privilege escalation attempts

---

## ⚔️ Exploitation Flow

1. User inputs malicious payload:

```bash
127.0.0.1; ls
```

2. Application constructs command:

```bash
ping 127.0.0.1; ls
```

3. System executes both commands

---

## 🔄 Medium Security Analysis

### Behavior

* Some characters filtered (e.g., `;`)
* Still vulnerable

### Issue

* Uses **blacklist filtering**

### Example Weak Logic

```php
$ip = str_replace(";", "", $_GET['ip']);
```

---

### ⚠️ Problem

* Blacklisting is incomplete
* Attackers bypass using:

```bash
127.0.0.1 && ls
```

---

## 🔒 High Security Analysis

### Behavior

* Input validation applied
* Restricted execution logic

---

### Improvements Observed

* Special characters blocked
* Input sanitised
* Execution constrained

---

## 📊 Security Comparison

| Level  | Validation Type | Security     |
| ------ | --------------- | ------------ |
| Low    | None            | ❌ Vulnerable |
| Medium | Blacklist       | ⚠️ Weak      |
| High   | Validation      | ✅ Secure     |

---

## 🧠 Key Insight

👉 **The vulnerability is not in the command itself, but in how input is handled**

---

## 🚨 Core Security Lessons

* Never trust user input
* Avoid direct system command execution
* Use validation, not filtering
* Prefer secure APIs over shell commands

---

## 📌 Final Conclusion

The DVWA implementation clearly demonstrates:

👉 **Input handling determines system security**

Even small improvements in validation drastically reduce exploitability.
