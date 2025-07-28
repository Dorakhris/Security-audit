# Project Title
Internal Security & Compliance Audit for Botium Toys



## Case Summary
- **Objective:** My objective was to conduct a comprehensive internal security audit for Botium Toys. I used the NIST Cybersecurity Framework (CSF) as the primary lens to evaluate the company's security posture against critical regulations, including PCI DSS and GDPR, and to identify major gaps in their defenses.
- **Scope:** The audit covered the entire organization's IT environment, with a specific focus on systems, processes, and data flows related to sensitive customer PII and payment card information.
- **Tools Used:** The primary "tools" for this GRC audit were the security frameworks themselves: NIST CSF, PCI DSS, GDPR, and ISO 27001. The process relied on stakeholder interviews, documentation review, and logical analysis.
- **Outcome:** The audit revealed critical deficiencies in foundational security controls, placing the organization at high risk of a data breach and in a state of non-compliance. I produced a prioritized, strategic roadmap to guide remediation efforts and build a resilient security program.



## Tools & Environment
| Tool / Framework | Purpose |
| :--- | :--- |
| **NIST Cybersecurity Framework** | The core framework used to structure the audit around the five functions: Identify, Protect, Detect, Respond, Recover. |
| **PCI DSS v4.0** | The compliance standard used to assess controls protecting cardholder data. |
| **GDPR** | The regulation used to assess controls protecting the personal data of EU citizens. |
| **ISO 27001** | Best-practice standard used as a reference for information security management controls. |
| **Corporate Environment** | The audit was conducted across Botium Toys' on-premise and cloud infrastructure. |



## Case Background
As the designated internal auditor for Botium Toys, I was tasked with performing the company's first formal security assessment. The business has been experiencing rapid growth, but its security practices have not kept pace, creating a significant and unknown level of risk. The primary goal was to move from an assumed security posture to a documented and understood one, ensuring the company could meet its legal and regulatory obligations and protect itself from cyber threats.



## Methodology
My audit followed a structured GRC methodology to ensure a thorough and repeatable assessment.

1.  **Scoping and Framework Selection:** I defined the scope of the audit to include all systems handling sensitive data. I selected the NIST CSF as the guiding framework due to its comprehensive and adaptable nature, using PCI DSS and GDPR as specific control checklists for compliance.
2.  **Evidence Collection:** I conducted a series of interviews with department heads and IT staff, reviewed all available technical documentation, and performed walkthroughs of key processes like user account creation and data handling.
3.  **Gap Analysis:** I systematically compared the "as-is" state of Botium Toys' security controls against the requirements of the selected frameworks. Each control was evaluated for its presence and effectiveness.
4.  **Risk Assessment:** For each identified gap, I assessed the potential business impact (e.g., financial loss, reputational damage) and the likelihood of exploitation. This allowed me to prioritize findings based on a clear risk matrix.
5.  **Roadmap Development:** I translated the prioritized list of risks into a series of actionable recommendations. Each recommendation was designed to close a specific gap, deliver tangible business value, and align with a compliance requirement.
6.  **Reporting:** I compiled all findings and the strategic roadmap into this formal report for review by company leadership.



## Findings & Evidence
The audit revealed systemic failures in fundamental security controls, resulting in both a high-risk operational environment and direct non-compliance with mandatory regulations.

**High-Impact Risk Summary**
| Risk Area | Description | Business Impact |
| :--- | :--- | :--- |
| **Access Control** | The principle of least privilege is not enforced; all employees have broad access to sensitive data. | High risk of insider threat and catastrophic data breach. A single compromised account grants full access. |
| **Data Protection** | Sensitive PII and payment data are stored and transmitted without any encryption. | High risk of data theft and exposure in a breach, leading to severe financial penalties and reputational damage. |
| **Business Continuity** | No documented Disaster Recovery (DR) or data backup plan exists. | Inability to recover from a ransomware attack or other disaster, risking total business shutdown. |
| **Threat Visibility** | No Intrusion Detection System (IDS) or centralized log monitoring is in place. | The organization is effectively blind to ongoing attacks, such as data exfiltration or brute-force attempts. |

**Key Compliance Failures**
| Framework | Requirement / Article | Finding | Status |
| :--- | :--- | :--- | :--- |
| **PCI DSS** | Req. 7: Restrict Access | All employees can access cardholder data. | **FAIL** |
| **PCI DSS** | Req. 3: Protect Stored Data | Cardholder data is stored unencrypted. | **FAIL** |
| **GDPR** | Art. 32: Security of Processing | No technical controls (encryption, access control) to secure EU customer data. | **FAIL** |



## Strategic Roadmap & Recommendations
This section outlines the prioritized plan to remediate the identified risks. My recommendations are focused on achieving the greatest risk reduction with the most logical sequencing of effort.

| Priority | Recommendation | Justification & Business Value | Framework Alignment |
| :--- | :--- | :--- | :--- |
| **CRITICAL** | **Implement Role-Based Access Control (RBAC)** | Immediately reduces the attack surface by ensuring employees only access data essential for their jobs. This is the most effective first step to prevent a widespread data breach from a single compromised account. | **NIST CSF:** PR.AC-4 <br> **PCI DSS:** R7 <br> **GDPR:** Art. 32 |
| **CRITICAL** | **Enforce Data Encryption** | Deploy **AES-256** for data-at-rest and **TLS 1.3** for data-in-transit. This is a non-negotiable compliance requirement and protects data confidentiality even if a system is breached. | **NIST CSF:** PR.DS-1 <br> **PCI DSS:** R3, R4 <br> **GDPR:** Art. 32 |
| **HIGH** | **Develop a Backup & Disaster Recovery Plan** | Establish a "3-2-1" backup strategy and a documented DR plan. This builds resilience against ransomware or hardware failure, ensuring the business can recover and minimizing downtime. | **NIST CSF:** PR.IP-4, RS.RP-1 <br> **ISO 27001:** A.12.3.1 |
| **HIGH** | **Strengthen Authentication Policies** | Enforce a strong password policy and deploy **Multi-Factor Authentication (MFA)** for all remote and critical system access. This hardens initial access points against common credential attacks. | **NIST CSF:** PR.AC-1 <br> **PCI DSS:** R8 |
| **MEDIUM** | **Deploy Threat Detection & Monitoring** | Implement a network **IDS (e.g., Snort)** and centralize logging with a **SIEM**. This provides the necessary visibility to detect attacks in progress, shifting from a purely preventative to a detective posture. | **NIST CSF:** DE.CM-1, DE.AE-2 |



## Conclusion
The audit concludes that Botium Toys is currently operating with an unacceptably high level of cybersecurity risk and is demonstrably non-compliant with PCI DSS and GDPR. The lack of basic controls for access, encryption, and recovery exposes the company to severe financial, reputational, and operational threats.

**Impact:** A security incident under the current posture would likely result in a catastrophic data breach, leading to significant regulatory fines, loss of customer trust, and prolonged business disruption.

**Recommendations:** It is my strong recommendation that leadership immediately sponsor and fund the strategic roadmap outlined above. The initial focus must be on implementing access control (RBAC) and data encryption, as these address the most critical risks and compliance failures.


## Lessons Learned / Reflection
This audit was a powerful case study in how cybersecurity debt accumulates in a growing organization. It highlights that compliance is not just a checkbox exercise but a direct outcome of having strong, foundational security controls in place. The most critical lesson is that the absence of controls like "least privilege" and encryption creates a fragile security posture where a single failure can lead to a total compromise.

For Botium Toys, this audit serves as a crucial turning point. It provides them with the awareness and the plan needed to build a security program that doesn't just avoid fines, but actively protects the business and its customers, enabling safer, more resilient growth in the future.



## References
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- [PCI Security Standards Council](https://www.pcisecuritystandards.org/)
- [EU General Data Protection Regulation (GDPR)](https://gdpr-info.eu/)


#GRC #CybersecurityAudit #NIST #PCIDSS #GDPR #ISO27001 #RiskManagement #Compliance
