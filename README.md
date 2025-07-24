# Internal Security Audit For Botium Toys

## Executive Summary
This report presents the findings of an internal security audit conducted for Botium Toys, a growing retail business. Using the **NIST Cybersecurity Framework (CSF)** as a guiding structure, this assessment evaluated the company's security posture against key industry regulations, including **PCI DSS**, **GDPR**, and best practices from **ISO 27001**.

The audit identified **critical deficiencies** in fundamental security domains, most notably in access control, data protection, and incident preparedness. These gaps present a significant risk of data breaches, financial penalties from non-compliance, and potential business disruption.

This report provides a prioritized, actionable roadmap for remediation. The recommendations are designed to not only close existing security gaps but also to build a resilient and compliant security program that can support the company's future growth.

**Date:** July 23, 2024

**Auditor:** Dorathy Christopher

---

## Risk Assessment Summary

The audit revealed several high-impact risks stemming from a lack of foundational security controls. The most significant risks are summarized below:

| Risk Area | Description | Business Impact | Key Compliance Violation |
| :--- | :--- | :--- | :--- |
| **Access Control** | The principle of least privilege is not enforced; all employees have unrestricted access to sensitive customer and payment data. | High risk of insider threat, data misuse, and catastrophic data breach. A single compromised account grants full access. | **PCI DSS** (Req. 7), **GDPR** (Art. 5, 25, 32) |
| **Data Protection** | Sensitive data (customer PII, payment info) is stored and transmitted without encryption. | High risk of data theft and exposure in the event of a breach, leading to severe financial and reputational damage. | **PCI DSS** (Req. 3, 4), **GDPR** (Art. 32) |
| **Business Continuity** | No documented Disaster Recovery (DR) or data backup plan exists. | Inability to recover from a ransomware attack, hardware failure, or other disasters, risking prolonged or total business shutdown. | **ISO 27001** (A.12.3.1, A.17.1.2) |
| **Threat Visibility** | No Intrusion Detection System (IDS) or centralized log monitoring is in place. | The organization is effectively blind to ongoing attacks, such as brute-force attempts or data exfiltration. | **NIST CSF** (DE.AE-2, DE.CM-1) |

---

## Key Compliance Gaps

The lack of fundamental controls results in direct non-compliance with major regulations.

### Payment Card Industry Data Security Standard (PCI DSS)
| Requirement | Finding | Status |
| :--- | :--- | :--- |
| **Req. 7: Restrict Access** | All employees can access cardholder data. | **FAIL** |
| **Req. 3: Protect Stored Data** | Cardholder data is stored unencrypted. | **FAIL** |
| **Req. 4: Encrypt Transmission** | No encryption for data in transit over public networks. | **FAIL** |

### General Data Protection Regulation (GDPR)
| Article | Finding | Status |
| :--- | :--- | :--- |
| **Art. 32: Security of Processing** | No technical controls (encryption, access control) to secure EU customer data. | **FAIL** |
| **Art. 5 & 25: Data Minimization** | Unrestricted internal access violates data protection by design and default. | **FAIL** |

---

## Strategic Roadmap for Remediation

The following recommendations are prioritized to address the most critical risks first. Each recommendation is aligned with business value and specific compliance frameworks.

| Priority | Recommendation | Justification & Business Value | Framework Alignment |
| :--- | :--- | :--- | :--- |
| **CRITICAL** | **Implement Least Privilege & RBAC** | Immediately reduces the attack surface by ensuring employees can only access data essential for their roles. This is the single most effective control to prevent a widespread data breach from a compromised account. | **PCI DSS:** R7 <br> **GDPR:** Art. 32 <br> **NIST CSF:** PR.AC-4 |
| **CRITICAL** | **Enforce Data Encryption** | Deploy **AES-256** for data-at-rest and **TLS 1.3** for data-in-transit. This protects data confidentiality even if storage is compromised and is a non-negotiable requirement for PCI DSS and GDPR compliance. | **PCI DSS:** R3, R4 <br> **GDPR:** Art. 32 <br> **ISO 27001:** A.10.1.1 |
| **HIGH** | **Develop a Backup & Disaster Recovery Plan** | Create a "3-2-1" backup strategy (3 copies, 2 media, 1 offsite) and a documented DR plan. This ensures the business can recover from a catastrophic event like ransomware, minimizing downtime and financial loss. | **NIST CSF:** PR.IP-4, RS.RP-1 <br> **ISO 27001:** A.12.3.1, A.17.1.2 |
| **HIGH** | **Strengthen Authentication Policies** | Enforce a strong password policy (12+ characters, complexity) and deploy **Multi-Factor Authentication (MFA)** for all remote access and access to critical systems. This hardens initial access points against credential theft. | **NIST CSF:** PR.AC-1 <br> **PCI DSS:** R8 |
| **MEDIUM** | **Deploy Threat Detection & Monitoring Tools** | Implement a network **IDS (e.g., Snort)** and centralize logging with a **SIEM (e.g., Splunk)**. This provides critical visibility into network traffic and allows for the detection of threats mapped to **MITRE ATT&CK** TTPs. | **NIST CSF:** DE.CM-1, DE.AE-2 <br> **ISO 27001:** A.12.4.1 |
| **MEDIUM** | **Establish a Vulnerability Management Program** | Conduct regular, authenticated vulnerability scans using a tool like **Nessus**. Create a process to prioritize and remediate identified vulnerabilities to systematically reduce the attack surface over time. | **NIST CSF:** ID.RA-1 <br> **PCI DSS:** R11.2 |

By implementing this strategic roadmap, Botium Toys can transform its security program from a high-risk liability into a resilient business enabler.
