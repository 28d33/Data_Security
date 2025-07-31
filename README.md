# Data Security Framework at JFin Payments

## Overview

Welcome to the Data Security repository. This project was developed as part of a data security assessment for **JFin Payments**, a rapidly growing online payment processing company. The goal is to establish a comprehensive and practical approach to data security—covering confidentiality, integrity, and availability—aligned with global best practices and regulatory requirements like **GDPR**, **ISO/IEC 27001**, and **PCI DSS**.

## Table of Contents

- [Project Scenario](#project-scenario)
- [Key Focus Areas](#key-focus-areas)
- [1. Data Governance](#1-data-governance)
- [2. Data Confidentiality](#2-data-confidentiality)
- [3. Data Integrity](#3-data-integrity)
- [4. Data Availability](#4-data-availability)
- [References](#references)

---

## Project Scenario

As a **Data Security Analyst** at JFin Payments, you are responsible for protecting over 100,000 customer profiles across the US and Europe. The role involves working with various teams to define and implement data governance and security policies, encrypt sensitive data, monitor data integrity, and design backup and availability strategies.

---

## Key Focus Areas

This project emphasizes:

- Developing and enforcing **strategic security policies**
- **Encrypting** data using RSA and AES standards
- **Hashing and validating** file integrity
- Implementing **robust audit policies**
- Establishing an effective **data backup strategy**

---

## 1. Data Governance

### Strategic Policies Implemented:

- **Data Classification**: Confidential, Internal, Public
- **Application & System Classification**
- **Annual Regulatory Assessments**

### Benefits:

- Ensures regulatory compliance (e.g., GDPR, RBI)
- Enhances risk management and incident readiness
- Streamlines operational and security processes

### Example Classification:

| Dataset                      | Classification |
|-----------------------------|----------------|
| Employee/Customer Profiles  | Confidential   |
| Company Emails/Newsletters  | Internal       |
| Blog Repository             | Public         |

---

## 2. Data Confidentiality

### Encryption Workflow

- **RSA 2048-bit key pair generation**
- **Disk encryption** using a custom C++ script
- Encryption protocols: `AES-256`, `TLS 1.2+`

### Repository Link:

🔗 [Encryption Source Code and Binaries](https://github.com/28d33/E-D--Crypto)

---

## 3. Data Integrity

### File Integrity Verification:

- SHA256 and SHA1 hash validation for `.dll` files
- Identification of legitimate and suspicious file versions

### Audit Policies Applied:

- **Password Policy**: Min. length 12, history enforced, complexity enabled
- **Account Lockout**: 5 attempts, 15-minute lockout
- **Audit Logging**: Success and failure logs for login, system, and object access
- **Security Options**: Disable default admin/guest, enforce UAC, disable LM hashes

---

## 4. Data Availability

### Backup Strategies by Data Type:

| Data Type   | Frequency   | Retention Period |
|-------------|-------------|------------------|
| Confidential | Real-time/Daily | 7 Years       |
| Internal     | Daily       | 90 Days          |
| Public       | Weekly/As Needed | 30 Days     |

### Local Backup Command (PowerShell):

```powershell
Copy-Item "C:\Users\d33\VirtualBox VMs\Ububtu" "C:\Users\d33\VirtualBox VMs Backup\Ububtu_$(Get-Date -Format yyyyMMdd)" -Recurse
```

References
🔐 E-D--Crypto GitHub Repo

📄 GDPR, PCI DSS, ISO/IEC 27001 Documentation

🛡️ CIS Benchmarks, NIST SP 800-53

Author

Deekshith A

Data Security Analyst at JFin Payments

License

This project is open for educational and professional demonstration purposes. For commercial or production use, please contact the author.
