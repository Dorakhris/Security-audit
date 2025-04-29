Overview

This project demonstrates an internal IT audit for Botium Toys, a small U.S. toy business with growing online operations. Using the NIST Cybersecurity Framework (NIST CSF), I assessed the company’s security posture, identified risks to critical assets, and evaluated compliance with PCI DSS, GDPR, NIST 800-53, and ISO 27001. Tools like Nessus, Splunk, and Wireshark were used to analyze vulnerabilities and logs, with risks mapped to MITRE ATT&CK for Threat Intelligence. This audit showcases my skills in Digital Forensics and Incident Response (DFIR), Security Operations Center (SOC) operations, and Governance, Risk, and Compliance (GRC).

Date: July 23, 2024

Auditor: Dorathy Christopher

## Scope
This audit encompasses Botium Toys’ entire security program, including all assets (on-premises and employee equipment, management systems, networks), internal processes, and procedures related to controls and compliance best practices.

## Goals
- Assess and classify existing assets to ensure proper management.
- Complete controls and compliance checklists to evaluate security posture.
- Recommend controls and compliance best practices to mitigate risks and ensure regulatory adherence. posture.

## Current Assets
- On-premises equipment: Desktops/laptops, smartphones, remote workstations, surveillance cameras, etc.
- Employee equipment: End-user devices, headsets, cables, keyboards, mice, docking stations.
- Storefront products: Toys sold on-site and online, stored in the warehouse
- Management systems: Accounting, telecommunication, database, security, ecommerce, and inventory management.
- Network: Internet access, internal network.
- Data: Customer data, payment information, inventory records
- Legacy Systems: End-of-life systems requiring human monitoring

## Risk Assessment

### Risk Description:
- Inadequate asset management due to unclassified assets.
- Lack of proper controls (e.g., access restrictions, encryption).
- Non-compliance with U.S. (PCI DSS) and international (GDPR) regulations.

### Control Best Practices:
- Identify: Dedicate resources to classify assets and assess their impact on business continuit
- Protect: Implement access controls, encryption, and monitoring.

### Risk Score: 8/10
### Impact: Medium (uncertain asset exposure increases potential for breaches).
### Compliance Risk: High (lack of controls violates PCI DSS, GDPR requirements).
### Threat Intelligence: Risks mapped to MITRE ATT&CK (e.g., Tactic TA0003: Persistence via unauthorized access).

## Controls Assessment Checklist

| Control                     | Status [YES/NO] | Explanation                                                                                  |
|-----------------------------|-----------------|----------------------------------------------------------------------------------------------|
| Least Privilege             | No              | Employees have unrestricted access to customer data, increasing breach risk.       |
| Disaster Recovery Plan      | No              | No plan exists, risking business continuity during incidents.         |
| Firewall                    | Yes             | Firewall blocks traffic based on defined security rules.                     |
| Password Policies           | ?               | Weak password requirements (e.g., no complexity rules) risk unauthorized access.               |
| Antivirus                   | Yes             | Antivirus software is active and monitored regularly..                                        |
| Backups                     | No              | No backup plan; incremental or full backups needed for data recovery.                 |
| Encryption                  | No              | No encryption for data at rest or in transit, violating confidentiality.                                |
| IIntrusion Detection System (IDS)                       | No              | No IDS to detect suspicious activities, increasing undetected intrusion risk..                    |
| Storefront                  | Yes             | Physical locks are sufficient, though not managed by IT.                                     |
| CCTV                        | Yes             | CCTV is operational; requires regular maintenance.                                                         |
| Fire Detection              | Yes             | Fire detection systems are in place; needs maintenance plan.          |

## Compliance Checklist

### Payment Card Industry Data Security Standard (PCI DSS)

| Best Practice                           | Status [YES/NO] | Explanation                                                                            |
|-----------------------------------------|-----------------|----------------------------------------------------------------------------------------|
| Authorized users access customer credit card data | No              | ll employees have access, violating PCI DSS Req. 7 (Restrict Access).                          |
| Credit card data stored securely                 | No              | Unencrypted storage violates PCI DSS Req. 3 (Protect Stored Data).                                          |
| Encryption secured                               | No              | No encryption implemented, violating PCI DSS Req. 4 (Encrypt Transmission).                                                   |

### General Data Protection Regulation (GDPR)

| Best Practice                           | Status [YES/NO] | Explanation                                                                            |
|-----------------------------------------|-----------------|----------------------------------------------------------------------------------------|
| EU customers’ data secured              | No              | No encryption or access controls, violating GDPR Article 32 (Security).                  |
| Privacy policies maintained             | Yes             | Enforced by IT and staff, meeting GDPR Article 13 (Information Provision).                                           |
| User access policies established        | No              | Unrestricted employee access violates GDPR Article 5 (Data Minimization).   |
| Data integrity maintained               | Yes             | Data integrity is ensured, meeting GDPR Article 5 (Integrity).                                                            |
| Data available to authorized users      | No              | AAll employees have access, violating GDPR Article 25 (Data Protection by Design).                                       |

## Recommendations
To enhance Botium Toys’ security posture and ensure compliance with PCI DSS, GDPR, NIST 800-53, and ISO 27001, implement the following:
- Implement Least Privilege: Restrict access to customer data using Role-Based Access Control (RBAC), ensuring only authorized personnel can view sensitive information, reducing breach risks. Aligns with PCI DSS Requirement 7, GDPR Article 32, and NIST 800-53 AC-2.
- Develop a Disaster Recovery Plan: Create a documented plan with regular testing to maintain business continuity during incidents like ransomware or hardware failures. Include recovery time objectives (RTOs) and align with NIST CSF Recover and ISO 27001 A.17.1.2.
- Strengthen Password Policies: Enforce complex passwords (minimum 12 characters, including uppercase, lowercase, numbers, and special symbols) and require updates every 90 days to prevent unauthorized access. Complies with PCI DSS Requirement 8 and NIST 800-53 IA-5.
- Implement Encryption: Use TLS 1.3 for secure data transmission and AES-256 for data at rest to protect customer and payment information, addressing confidentiality risks. Meets PCI DSS Requirements 3 and 4 and GDPR Article 32.
- Establish User Access Policies: Deploy Multi-Factor Authentication (MFA) and role-based policies to limit data access to authorized users, preventing insider threats and data leaks. Supports GDPR Article 25 and NIST 800-53 AC-3.
- Deploy an Intrusion Detection System (IDS): Implement Snort or Zeek to monitor network traffic and alert on suspicious activities, such as unauthorized login attempts, enhancing real-time threat detection. Aligns with NIST CSF Detect and ISO 27001 A.12.4.1.
- Implement Backups: Schedule daily incremental and weekly full backups with secure offsite storage to ensure data recovery after incidents, minimizing downtime. Complies with NIST CSF Recover and ISO 27001 A.12.3.1.
- Integrate Threat Intelligence: Deploy Splunk for real-time log monitoring to detect anomalies (e.g., failed logins) and map threats to MITRE ATT&CK tactics, such as T1078 (Valid Accounts) for unauthorized access. Use VirusTotal to validate suspicious IPs from audit logs, strengthening proactive threat hunting.

By addressing these areas, Botium Toys can significantly improve their security posture, reduce risks, and ensure compliance with relevant regulations.
