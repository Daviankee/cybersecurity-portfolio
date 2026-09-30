# SOC Investigation: Data Exfiltration Detection

## Room

TryHackMe: Data Exfiltration Detection

## Objective

Identify suspicious data exfiltration activity and determine how the activity was detected.

## Tools Used

- SIEM
- Splunk
- Network logs
- DNS logs
- Firewall logs
- [Other tools used in the room]

## Scenario

[Briefly describe the situation given by the room.]

## Investigation

### 1. Initial Alert

[What alert or suspicious activity did you receive?]

- Timestamp:
- Source IP:
- Destination IP:
- Username:
- Protocol:
- Destination port:

![Initial Alert](screenshots/alert.png)

### 2. Log Investigation

[Explain what you searched for.]

Example:

I searched the available logs for activity associated with the source IP and reviewed the related network events.

![Log Investigation](screenshots/log-search.png)

### 3. Indicators

During the investigation, I identified the following indicators:

- Source IP:
- Destination IP:
- Domain:
- Port:
- Protocol:
- File:
- Username:

### 4. Analysis

[Explain what made the activity suspicious.]

For example:

- Unusual amount of outbound traffic
- Unexpected external destination
- Suspicious DNS requests
- Unusual protocol or port
- Activity occurring outside normal hours
- Repeated connections to the same destination

![Evidence](screenshots/evidence.png)

### 5. Investigation Result

[Explain what you determined from the evidence.]

### 6. Classification

Classification: [True Positive / False Positive]

Reason:

[Explain the evidence supporting your classification.]

### 7. Response

[Explain what action was taken in the simulation.]

Examples:

- Blocked destination IP
- Blocked domain
- Isolated host
- Escalated the incident
- Continued monitoring

### Lessons Learned

- I learned how to identify indicators associated with possible data exfiltration.
- I learned how to correlate network activity with other log sources.
- I improved my understanding of how SOC analysts investigate unusual outbound traffic.
- I learned the importance of establishing whether suspicious activity represents actual data exfiltration or an attempted connection.
