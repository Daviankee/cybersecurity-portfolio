# Datacom Cyber Security Operations Job Simulation

**Platform:** Forage  
**Completion Date:** 13 October 2026  
**Focus Areas:** Cybersecurity Operations, Incident Investigation, Risk Assessment and Risk Management

## Overview

I completed the Datacom Cyber Security Operations Job Simulation on Forage. The simulation focused on how a cybersecurity team investigates cyber threats, assesses organisational risks and recommends security improvements for clients.

Through this exercise, I investigated a simulated ransomware incident, documented the findings in an incident report and identified measures to improve the organisation's cybersecurity posture.

## Tasks Completed

- Investigated a simulated ransomware attack affecting a mid-sized company.
- Analysed the suspected initial attack vector and indicators of compromise.
- Identified potentially compromised data and affected systems.
- Assessed the operational, financial, legal and reputational impact of the incident.
- Identified potential security weaknesses and recommended mitigation measures.
- Conducted a cybersecurity risk assessment.
- Documented investigation findings and recommendations in a structured report.

## Scenario Overview

The simulated organisation experienced a ransomware attack that began with a phishing email sent to a finance team member. The email contained a malicious Excel attachment.

### Incident Details

| Category | Findings |
|---|---|
| Incident Type | Ransomware Attack |
| Initial Entry Point | Phishing email with malicious Excel attachment |
| Affected Systems | File server, HR systems, finance systems and backup server |
| Potentially Compromised Data | Employee payroll records, patient appointment schedules and internal system credentials |
| Suspicious Activity | Unusual overseas login and use of Mimikatz |
| Ransomware Indicator | Files with the `.orionlock` extension |

## Investigation Findings

The available indicators suggested that the attacker gained an initial foothold through a phishing email and potentially harvested credentials using Mimikatz.

The suspicious overseas login indicated possible unauthorised access. The attacker then appeared to reach multiple business systems and encrypt files, including files on part of the backup server.

The incident affected three important areas of information security:

- **Confidentiality:** Payroll records, patient appointment schedules and internal credentials were potentially exposed.
- **Integrity:** The organisation needed to verify whether files or system configurations had been modified.
- **Availability:** Ransomware encryption disrupted access to critical business systems and threatened recovery operations.

Data exfiltration was not confirmed in the scenario. Further investigation would be required to determine whether sensitive information had left the organisation's network.

## Indicators of Compromise (IOCs)

| Indicator | Security Significance |
|---|---|
| Suspicious overseas IP login | Possible unauthorised access |
| Mimikatz | Possible credential harvesting |
| `.orionlock` file extension | Indicator of ransomware-related file encryption |
| Malicious Excel attachment | Suspected initial delivery mechanism |

These indicators would require correlation with endpoint, authentication, firewall and network logs to establish the attack timeline and scope.

## Risk Assessment

| Risk | Potential Impact | Recommended Control |
|---|---|---|
| Phishing and malicious attachments | Initial system compromise | Email filtering, attachment scanning and employee awareness training |
| Credential theft | Unauthorised account access | Multifactor authentication, credential protection and least-privilege access |
| Lateral movement | Compromise of additional systems | Network segmentation and restricted administrative access |
| Ransomware encryption | Business disruption and data unavailability | Endpoint detection and response, centralised monitoring and incident response procedures |
| Backup compromise | Longer recovery time and potential data loss | Offline or immutable backups and regular restoration testing |
| Personal data exposure | Regulatory and reputational consequences | Access controls, data protection procedures and breach response planning |

## Recommendations

### 1. Incident Containment
- Isolate affected systems to prevent further encryption.
- Disable compromised accounts and revoke suspicious active sessions.
- Preserve forensic evidence and investigate additional affected devices.

### 2. Identity and Access Security
- Enforce multifactor authentication on remote access and privileged accounts.
- Rotate compromised credentials and review service-account permissions.
- Apply least-privilege access principles.

### 3. Endpoint and Email Security
- Improve phishing detection and malicious attachment filtering.
- Restrict risky Office macros and document behaviours.
- Use endpoint detection and response tools to identify suspicious processes and credential theft.

### 4. Network Security
- Segment finance, HR, user workstations and backup infrastructure.
- Restrict unnecessary connections between servers.
- Monitor suspicious authentication activity and lateral movement.

### 5. Backup and Recovery
- Maintain offline or immutable backups.
- Separate backup administration accounts from ordinary user accounts.
- Test backup restoration and disaster recovery procedures regularly.

### 6. Security Monitoring
- Centralise system and authentication logs in a SIEM platform.
- Create alerts for unusual logins, credential dumping and mass file encryption.
- Review security alerts and investigate suspicious activity promptly.

## Key Learning Outcomes

This simulation helped me develop my understanding of:

- Cyberattack investigation and incident analysis.
- Indicators of compromise and attack vectors.
- Cybersecurity risk assessment and mitigation.
- The confidentiality, integrity and availability principles.
- Incident response, backup security and business continuity.
- Communicating technical findings through structured reports.

It also reinforced the importance of investigating evidence before drawing conclusions, particularly when determining whether data was exfiltrated or the full network was compromised.

## Tools and Technologies

Concepts covered in this exercise included:

- Security information and event management (SIEM)
- Endpoint detection and response (EDR)
- Windows authentication and security logs
- Network security and firewall monitoring
- Incident response and risk assessment

These represent technologies and concepts relevant to the investigation. They should not be interpreted as tools personally deployed during the simulation unless explicitly used.

## Certificate

**Datacom Cyber Security Operations Job Simulation, Forage**

Completed: 13 October 2026

[View Completion Certificate](https://www.theforage.com/completion-certificates/gCW7Xki5Y3vNpBmnn/yTszJTvkHFBH6zAn3_gCW7Xki5Y3vNpBmnn_6acde7e475a2e300d32c3f1e_1791902030334_completion_certificate.pdf)

## Disclaimer

This repository documents a simulated cybersecurity job exercise completed through Forage. The incident, affected organisation and attack details are fictional scenario elements provided for training purposes. The findings and recommendations reflect my analysis of the exercise.
