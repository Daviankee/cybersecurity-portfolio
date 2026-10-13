# RetailNova Cybersecurity Risk Assessment & Threat Matrix

This repository contains the threat identification and cybersecurity risk assessment for **RetailNova Pty Ltd**, evaluated against standard 5x5 risk prioritization matrices and Australian regulatory contexts (OAIC / Privacy Act).

---

## 🏢 Company Profile

* **Company:** RetailNova Pty Ltd
* **Headquarters:** Melbourne, Australia
* **Employees:** ~1,200 staff
* **Revenue:** $450 Million AUD
* **Footprint:** 85 physical stores nationwide + E-commerce Platform
* **Core Tech Stack:** AWS, SAP ERP, Salesforce CRM, Cloud POS, PayPal/Afterpay
* **Key Risk Factors:** BYOD Policy, Remote VPN Access, Third-Party Logistics/Marketing Integrations

---

## 🔍 Part 1: Threat and Vulnerability Identification Table

| Asset Name | Asset Description | Associated Threats | Potential Vulnerabilities | Mitigation Notes |
| :--- | :--- | :--- | :--- | :--- |
| **Corporate Credentials & Network** | Corporate email, VPN access, Teams/Slack, internal tools. | Phishing, Social Engineering, Credential Theft, Unauthorized Access. | Basic security training; lack of mandatory MFA across corporate access; unmonitored remote VPN. | Enforce mandatory MFA for all VPN and corporate accounts; implement advanced phishing simulations and continuous training. |
| **Endpoint Devices (BYOD & POS)** | BYOD corporate devices and cloud-connected POS systems (85 stores). | Ransomware, Malware Infections, Device Theft/Loss, Data Exfiltration. | Lack of MDM/MAM on BYOD devices; reliance on endpoint antivirus without full EDR / Zero Trust controls. | Deploy MDM/MAM for BYOD endpoints; upgrade endpoint protection to full EDR with central SOC monitoring; enforce local data encryption. |
| **Customer Data & Vendor Ecosystem** | Customer PII, purchase history, and marketing databases shared externally. | Third-Party Data Leak, Supply Chain Compromise, Regulatory Fines (OAIC). | Over-sharing of PII with external vendors; lack of third-party risk assessments (TPRM); no automated DLP. | Conduct Third-Party Risk Assessments (TPRM); enforce contractual SLAs and data minimization; implement DLP for customer PII. |

---

## 📋 Part 2: Detailed Risk Assessments

### 🛡️ Risk Assessment 1: Credential Compromise via Phishing (BYOD / Remote VPN)

| Field | Details |
| :--- | :--- |
| **Risk ID** | `RSK-2026-001` |
| **Date Identified** | 14 Oct 2026 |
| **Risk Title** | Phishing Attack Leading to Corporate Network Infiltration & Credential Theft |
| **Review Date** | 14 Jan 2027 |
| **Risk Description** | Attackers send targeted phishing emails to customer service and corporate staff. Staff members enter credentials on fake login portals, giving attackers valid VPN and Microsoft Teams/Slack credentials to access internal systems. |
| **Assets at Risk** | Corporate Network, Customer Service Portals, VPN, Email, Teams/Slack |
| **Threat** | Cybercriminals / External Threat Actors |
| **Vulnerability** | Reliance on basic security training; lack of phishing-resistant Multi-Factor Authentication (MFA) on VPN and corporate logins. |
| **Existing Controls** | Basic security awareness training, firewall, antivirus software. |

#### Risk Evaluation
* **Inherent Risk:** `Likely (4)` × `Major (4)` = **HIGH**
* **Residual Risk:** `Unlikely (2)` × `Moderate (3)` = **MEDIUM**

#### Treatment Plan
1. Enforce mandatory Multi-Factor Authentication (MFA) across all remote VPN, email, and internal tools.
2. Implement advanced email security gateways (anti-phishing / anti-spoofing protocols: SPF, DKIM, DMARC).
3. Conduct quarterly phishing simulation testing for higher-risk departments (e.g., customer service).
* **Risk Owner:** Head of IT Security / CISO

---

### 🛡️ Risk Assessment 2: Ransomware Infection across BYOD and Store POS Systems

| Field | Details |
| :--- | :--- |
| **Risk ID** | `RSK-2026-002` |
| **Date Identified** | 14 Oct 2026 |
| **Risk Title** | Ransomware Outage Impacting E-Commerce & POS Store Operations |
| **Review Date** | 14 Jan 2027 |
| **Risk Description** | Malware or ransomware introduced through unmonitored personal devices (BYOD) or store network endpoints spreads to store POS networks or cloud servers, causing store downtime and revenue loss. |
| **Assets at Risk** | Cloud POS Systems (85 stores), AWS Infrastructure, SAP ERP, BYOD Laptops/Phones |
| **Threat** | Ransomware Operators / Cybercriminals |
| **Vulnerability** | Lack of Mobile Device Management (MDM) on BYOD devices; flat network segmentation between corporate BYOD and POS networks. |
| **Existing Controls** | Endpoint protection / antivirus software (prevented an incident in 2024 with 2 hours downtime), firewalls. |

#### Risk Evaluation
* **Inherent Risk:** `Possible (3)` × `Major (4)` = **HIGH**
* **Residual Risk:** `Unlikely (2)` × `Minor (2)` = **LOW**

#### Treatment Plan
1. Mandate MDM / EDR deployment on all BYOD devices accessing internal resources.
2. Implement strict micro-segmentation separating store POS systems from general staff networks.
3. Establish immutable offsite cloud backups for SAP, Salesforce, and store database configurations with tested recovery playbooks.
* **Risk Owner:** Infrastructure & IT Operations Manager

---

### 🛡️ Risk Assessment 3: Customer Data Breach via Third-Party Vendor Ecosystem

| Field | Details |
| :--- | :--- |
| **Risk ID** | `RSK-2026-003` |
| **Date Identified** | 14 Oct 2026 |
| **Risk Title** | Exfiltration of Customer PII via Third-Party Service Provider |
| **Review Date** | 14 Jan 2027 |
| **Risk Description** | A compromise at a third-party marketing, logistics, or loyalty partner results in unauthorized exposure or exfiltration of RetailNova customer details (names, emails, phones, addresses, purchase history). |
| **Assets at Risk** | Customer Personal Data (PII), Marketing Databases, Brand Reputation |
| **Threat** | Cybercriminals targeting supply chain / third-party vendors |
| **Vulnerability** | Lack of strict vendor security oversight and data minimization standards; unencrypted data transfers or poor third-party storage practices. |
| **Existing Controls** | Basic contract clauses, tokenized payment storage via payment gateways. |

#### Risk Evaluation
* **Inherent Risk:** `Likely (4)` × `Major (4)` = **HIGH**
* **Residual Risk:** `Unlikely (2)` × `Moderate (3)` = **MEDIUM**

#### Treatment Plan
1. Institute a formal Third-Party Risk Management (TPRM) Framework requiring annual security audits and SOC 2 Type II compliance for suppliers.
2. Enforce data minimization, pseudonymization, and encryption for all customer data exported to third-party marketing and logistics tools.
3. Implement Data Loss Prevention (DLP) controls to monitor and restrict exfiltration of customer PII.
* **Risk Owner:** Data Governance Officer / Legal & Compliance Manager

---

## 📊 5x5 Risk Matrix Reference

| Likelihood ↓ \ Impact → | Insignificant (1) | Minor (2) | Moderate (3) | Major (4) | Extreme (5) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **5 – Almost Certain** | MEDIUM | HIGH | HIGH | EXTREME | EXTREME |
| **4 – Likely** | MEDIUM | MEDIUM | HIGH | HIGH | EXTREME |
| **3 – Possible** | LOW | MEDIUM | MEDIUM | HIGH | HIGH |
| **2 – Unlikely** | LOW | LOW | MEDIUM | MEDIUM | HIGH |
| **1 – Rare** | LOW | LOW | LOW | MEDIUM | MEDIUM |