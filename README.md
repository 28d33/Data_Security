# 🔐 Data Security Assessment – JFin Payments

A detailed data security analysis project conducted for JFin Payments, a rapidly growing online payment processor. This project covers strategic data governance, encryption and access control, system hardening, backup strategy, and compliance with global data protection standards.

---

## 🧭 Project Overview

**Organization:** JFin Payments  
**Role:** Data Security Analyst  
**Location:** Los Angeles, California  
**Scope:**  
- Data governance and classification  
- Confidentiality, integrity, and availability of critical data  
- Regulatory compliance (GDPR, PCI-DSS, ISO 27001)  
- Backup and retention strategies  
- Disk and file encryption using custom C++ utilities  

---

## 📘 Sections

### 1. 🗂️ Data Governance

- **Annual Data Classification:**  
  Classify all datasets as *Confidential*, *Internal*, or *Public*

- **System & Application Categorization:**  
  Prioritize security controls for business-critical systems

- **Regulatory Assessments:**  
  Map policies to evolving standards like **GDPR**, **PCI DSS**, **RBI**, and **ISO/IEC 27001**

#### 🔐 Classification Table
| Data Type | Classification |
|-----------|----------------|
| Employee/customer profiles | Confidential |
| Internal communications | Internal |
| Technical diagrams/IP | Confidential |
| Blogs and press releases | Public |

---

### 2. 🔏 Data Confidentiality

- **Disk Encryption:**  
  Implemented custom C++ utilities using RSA-2048 key pair for disk image encryption  
  GitHub: [E-D--Crypto](https://github.com/28d33/E-D--Crypto)

- **Regulatory Policies Implemented:**
  - Data Encryption Policy (AES-256, TLS 1.2+)
  - Access Control with MFA and RBAC
  - Data Retention and Secure Disposal
  - Breach Notification within 72 hours (GDPR)
  - Classification & Labeling
  - Annual Employee Security Awareness Training

---

### 3. 🔐 Data Integrity

- **Hash Verification (SHA-256 & SHA-1)** for critical DLL files  
  - Verified file versions
  - Detected unknown or unverifiable hashes

- **System Hardening (VM Security):**
  - Strong password policy enforcement
  - Account lockout thresholds
  - Full audit logging for:
    - Logon events
    - Object access
    - System events
  - Hardened system options (UAC, guest/admin account disabling, LAN hash blocking)

---

### 4. 💾 Data Availability

#### 🔁 Backup Strategy by Classification

| Classification | Frequency | Retention |
|----------------|-----------|-----------|
| **Confidential** | Real-time/Daily | 7 Years |
| **Internal**     | Daily     | 90 Days  |
| **Public**       | Weekly    | 30 Days  |

- **Implementation:**  
  PowerShell-based backup automation script:
  ```powershell
  Copy-Item "C:\Path\To\Data" "C:\Backup\Path\Data_$(Get-Date -Format yyyyMMdd)" -Recurse
``


## 🧰 Tools & Technologies

* **Language:** C++ (for RSA encryption)
* **PowerShell:** For local data backup automation
* **SHA Tools:** For file integrity checking
* **Windows Security Policies:** Enforced via GPO and Local Security Policy

---

## 📌 Compliance References

* ✅ GDPR – General Data Protection Regulation
* ✅ PCI DSS – Payment Card Industry Data Security Standard
* ✅ ISO/IEC 27001 – Information Security Management Standard
* ✅ DoD 5220.22-M – Data Sanitization Standard

---

## 👤 Author

**Deekshith A**
Role: Data Security Analyst
Expertise: Information Security, Compliance, Cryptography, Risk Management

---

## 📄 License

This project is provided for educational and informational purposes only.


