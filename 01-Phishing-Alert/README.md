# SOC Investigation: Phishing Alert

## Scenario

An alert was triggered by an inbound email containing an external link.

## Objective

Determine whether the alert represents malicious activity or a false positive.

## Tools Used

- SIEM
- Splunk
- Firewall logs
- Proxy logs
- Wireshark

## Investigation

### 1. Review the Alert

I reviewed the initial alert and identified the relevant indicators.

--> Alert ID — 8816.

--> Alert name — Access to Blacklisted External URL Blocked by Firewall.

--> Severity and risk score — High.
![Initial Alert](screenshots/alert.png)

### 2. SIEM Investigation

I searched the SIEM for related activity using the available indicators.

--> URL: hxxps[://]bit[.]ly/3sHkX3da12340
--> DestinationIP: 67.199.248.11
--> Rule: Blocked Websites
--> timestamp: 09/29/2026 15:57:02.294
![Initial Alert](screenshots/siemsearch.png)
