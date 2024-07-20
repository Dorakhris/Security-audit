# Case Scenerio
Botium Toys is a small U.S. business that develops and sells toys. The business has a single physical location, which serves as their main office, a storefront, and warehouse for their products. However, Botium Toy’s online presence has grown, attracting customers in the U.S. and abroad. As a result, their information technology (IT) department is under increasing pressure to support their online market worldwide.

The manager of the IT department has decided that an internal IT audit needs to be conducted. She expresses concerns about not having a solidified plan of action to ensure business continuity and compliance, as the business grows. She believes an internal audit can help better secure the company’s infrastructure and help them identify and mitigate potential risks, threats, or vulnerabilities to critical assets. The manager is also interested in ensuring that they comply with regulations related to internally processing and accepting online payments and conducting business in the European Union (E.U.).

The IT manager starts by implementing the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF), establishing an audit scope and goals, listing assets currently managed by the IT department, and completing a risk assessment. The goal of the audit is to provide an overview of the risks and/or fines that the company might experience due to the current state of their security posture.

Your task is to review the IT manager’s scope, goals, and risk assessment report. Then, perform an internal audit by completing a controls and compliance checklist.

# Security Audit for Botium Toys

**Date:** July 23, 2024

**Auditor:** Dorathy Christopher

## Scope
The scope of this audit encompasses Botium Toys’ entire security program. This includes all assets, internal processes, and procedures related to the implementation of controls and compliance best practices.

## Goals
- Assess existing assets.
- Complete the controls and compliance checklist.
- Determine which controls and compliance best practices need to be implemented to improve Botium Toys’ security posture.

## Current Assets
- On-premises equipment: Desktops/laptops, smartphones, remote workstations, surveillance cameras, etc.
- Employee equipment: End-user devices, headsets, cables, keyboards, mice, docking stations.
- Storefront products: Items available for sale on-site and online, stored in the adjoining warehouse.
- Management systems: Accounting, telecommunication, database, security, ecommerce, and inventory management systems.
- Internet access
- Internal network
- Data retention and storage
- Legacy system maintenance: End-of-life systems that require human monitoring.

## Risk Assessment

### Risk Description:
- Inadequate asset management.
- Lack of proper controls.
- Non-compliance with U.S. and international regulations and standards.

### Control Best Practices:
- Identify: Dedicate resources to identify and classify assets to manage them appropriately. Determine the impact of asset loss on business continuity.

### Risk Score: 8 (on a scale of 1 to 10)
### Impact: Medium (due to uncertainty about which assets are at risk)
### Compliance Risk: High (due to insufficient controls and adherence to compliance best practices).

## Controls Assessment Checklist

| Control                     | Status [YES/NO] | Explanation                                                                                  |
|-----------------------------|-----------------|----------------------------------------------------------------------------------------------|
| Least Privilege             | No              | Employees have access to customer data. This must be restricted to reduce breach risk.       |
| Disaster Recovery Plan      | No              | No plan for handling disasters. Implementation is necessary for business continuity.         |
| Firewall                    | Yes             | A firewall is in place to block traffic based on defined security rules.                     |
| Password Policies           | ?               | A policy exists but has weak requirements, risking identity management access.               |
| Antivirus                   | Yes             | Antivirus software is active and regularly monitored.                                        |
| Backups                     | No              | No backup plan is in place. Implement incremental, full, or partial backups.                 |
| Encryption                  | No              | No encryption is implemented to protect data confidentiality.                                |
| IDS                         | No              | An Intrusion Detection System is needed to identify potential intrusions.                    |
| Storefront                  | Yes             | Sufficient locks are in place, though not managed by IT.                                     |
| CCTV                        | Yes             | CCTV is operational and functioning.                                                         |
| Fire Detection              | Yes             | Fire detection systems are in place, but maintenance and a usage plan are required.          |

## Compliance Checklist

### Payment Card Industry Data Security Standard (PCI DSS)

| Best Practice                           | Status [YES/NO] | Explanation                                                                            |
|-----------------------------------------|-----------------|----------------------------------------------------------------------------------------|
| Authorized users access customer credit card data | No              | All employees currently have access, which is a bad practice.                          |
| Credit card data stored securely                 | No              | Data is not encrypted, violating regulations.                                          |
| Encryption secured                               | No              | Encryption has not been implemented.                                                   |

### General Data Protection Regulation (GDPR)

| Best Practice                           | Status [YES/NO] | Explanation                                                                            |
|-----------------------------------------|-----------------|----------------------------------------------------------------------------------------|
| EU customers’ data secured              | No              | GDPR practices are not applied, risking fines from the EU government.                  |
| Privacy policies maintained             | Yes             | Enforced by IT team members and other staff.                                           |
| User access policies established        | No              | Employees have access to internally stored data, indicating a lack of access policy.   |
| Data integrity maintained               | Yes             | Data integrity is in place.                                                            |
| Data available to authorized users      | No              | All employees currently have access to all data.                                       |

## Recommendations
Botium Toys needs to address several critical areas to improve their security posture and compliance:
- Implement Least Privilege: Restrict access to customer data to authorized personnel only.
- Develop a Disaster Recovery Plan: Create and maintain a plan to ensure business continuity in the event of a disaster.
- Strengthen Password Policies: Update and enforce strong password requirements to enhance identity management security.
- Implement Encryption: Protect sensitive data by encrypting it both in transit and at rest.
- Establish User Access Policies: Limit data access to authorized users only to prevent unauthorized access.
- Deploy IDS: Implement an Intrusion Detection System to monitor and detect suspicious activities.

By addressing these areas, Botium Toys can significantly improve their security posture, reduce risks, and ensure compliance with relevant regulations.
