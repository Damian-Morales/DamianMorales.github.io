#  Internal IT Security Audit – Botium Toys

This document presents a comprehensive assessment of Botium Toys' current security controls and compliance status, based on the risk assessment report and aligned with industry standards.

---

## Audit Scope

- **Objective**: Evaluate existing security controls and identify areas for improvement.
- **Standards Referenced**: NIST Cybersecurity Framework (CSF), PCI DSS, GDPR, SOC 2.
- **Methodology**: Review of administrative, technical, and physical controls; compliance check against relevant standards.

---

##  Controls Assessment Checklist

| **Control**                              | **Implemented** | **Notes**                                                                |
|------------------------------------------|-----------------|--------------------------------------------------------------------------|
| Least Privilege                          |  No            | Access rights are not restricted based on user roles.                    |
| Disaster Recovery Plans                  |  No            | No formal disaster recovery plan documented.                             |
| Password Policies                        |  No            | Lack of enforced password complexity and rotation policies.              |
| Separation of Duties                     |  No            | Critical tasks are not divided among different individuals.              |
| Firewall                                 |  Yes           | Firewall is in place to monitor and control network traffic.             |
| Intrusion Detection System (IDS)         |  No            | No IDS implemented to detect unauthorized access.                        |
| Backups                                  |  No            | Inconsistent backup procedures; no regular schedule.                     |
| Antivirus Software                       |  Yes           | Antivirus solutions are deployed across all systems.                     |
| Manual Monitoring (Legacy Systems)       |  No            | Legacy systems lack continuous monitoring mechanisms.                    |
| Encryption                               |  No            | Encryption is not implemented.                                           |
| Password Management System               |  No            | There is no password management system currently in place.                |
| Physical Locks (Offices, Storefront)     |  Yes           | Locks are installed at all access points.                                |
| CCTV Surveillance                        |  yes           | Surveillance systems are installed and functioning at the physical location. |
| Fire detection/prevention                |  yes           | Has a functioning fire detection and prevention system.                  |

---

##  Compliance Best Practices Checklist

### PCI DSS

| **Requirement**                                   | **Compliant** | **Notes**                                                   |
|---------------------------------------------------|----------------|--------------------------------------------------------------|
| Restrict access to cardholder data                |  No           | Access controls are not enforced.                            |
| Secure storage/transmission of cardholder data    |  No           | Encryption not implemented.                                  |
| Implement strong encryption protocols             |  No           | Data is vulnerable.                                          |
| Enforce secure password policies                  |  No           | Password policy does not meet PCI DSS standards.             |

### GDPR

| **Requirement**                                   | **Compliant** | **Notes**                                                   |
|---------------------------------------------------|----------------|--------------------------------------------------------------|
| Protect EU customer data                          |  No           | Inadequate data protection for EU clients.                   |
| Notify breaches within 72 hours                   |  Yes          | There is a plan to notify E.U. customers within 72 hours of a breach.|
| Inventory and classify personal data              |  No           | Data is not systematically documented or classified.         |
| Privacy policy and transparency documentation     |  Yes          | Private policies, procedures, and processes have been developed and enforced.|

### SOC 2

| **Requirement**                                   | **Compliant** | **Notes**                                                   |
|---------------------------------------------------|----------------|--------------------------------------------------------------|
| User access policies and reviews                  |  No           | User roles and access levels are not consistently reviewed.  |
| Maintain confidentiality of sensitive data        |  No           | Controls for protecting sensitive data are insufficient.     |
| Ensure data integrity and accuracy                |  Yes          | Data integrity is in place.                                  |
| Data availability                                 |  No           | Authorization needs to be limited to only those who need it. |

---

##  Recommendations

**Immediate control actions**
- Develop and implement a comprehensive password policy.
- Establish a formal disaster recovery and business continuity plan.
- Implement an intrusion detection system for real-time threat monitoring.
- Encrypt sensitive data at all times.

**Compliance measures**
- Restrict access to cardholder data and enforce encryption protocols.
- Achieve GDPR compliance by protecting EU customer data and implementing a breach data notification procedure.
- Manage user access and ensure data integrity and availability.

**Planning for the future**
- Regularly conduct audits and reviews of security policies and procedures.
- Initiate ongoing cybersecurity training programs for employees.

---

📁 [← Back to Portfolio](../index.html)
