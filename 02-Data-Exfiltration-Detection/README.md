# Data Exfiltration Detection

This section documents my practical cybersecurity investigations into different data exfiltration techniques using TryHackMe labs.

## Objective

The objective of these investigations is to understand how data exfiltration occurs through different protocols and how SOC analysts can detect suspicious activity using network traffic, logs and security monitoring tools.

## Techniques Investigated

| Technique         | Tools             | Investigation Focus                                   |
| ----------------- | ----------------- | ----------------------------------------------------- |
| DNS Exfiltration  | Wireshark, Splunk | DNS tunneling, unusual query lengths, query frequency |
| FTP Exfiltration  | Wireshark, Splunk | Suspicious FTP activity and file transfers            |
| HTTP Exfiltration | Wireshark, Splunk | Unusual HTTP requests and outbound traffic            |
| [Technique]       | [Tools]           | [Investigation focus]                                 |

## Investigation Methodology

For each investigation, I follow a similar process:

1. Review the initial scenario or security alert.
2. Identify relevant indicators such as IP addresses, domains, ports and timestamps.
3. Analyse network traffic or security logs.
4. Use filtering and search queries to narrow down suspicious activity.
5. Correlate findings across available data sources.
6. Identify the source and destination involved.
7. Determine whether the activity is consistent with data exfiltration.
8. Document the findings and supporting evidence.
9. Record the lessons learned from the investigation.

## Tools Used

* Wireshark
* Splunk
* SIEM
* Network traffic analysis
* DNS logs
* Firewall logs
* Proxy logs
* TryHackMe lab environments

## Investigations

### DNS Exfiltration

Investigated DNS tunneling and analysed suspicious DNS queries for indicators such as unusual query lengths, high query volumes and repeated communication with an external domain.

[View DNS Exfiltration Investigation](DNSTunneling/)

### FTP Exfiltration

Investigated suspicious FTP activity and analysed network traffic associated with potential file transfers.

[View FTP Exfiltration Investigation](FTP-Exfiltration/)

### HTTP Exfiltration

Investigated potential data exfiltration over HTTP and analysed outbound requests and network activity.

[View HTTP Exfiltration Investigation](HTTP-Exfiltration/)

## Skills Demonstrated

* Network traffic analysis
* SIEM investigation
* Log analysis
* Alert triage
* Indicator identification
* IP and domain analysis
* Wireshark filtering
* Splunk queries
* Incident documentation
* Data exfiltration detection

## Key Learning

These investigations helped me understand how attackers can use legitimate network protocols to move data outside an environment. I learned how unusual traffic patterns, query characteristics, connection frequency and log activity can be used as indicators during a SOC investigation.

Each investigation contains the evidence, analysis, findings and lessons learned from the individual lab.
