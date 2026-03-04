# 🛡️ Threat Detection Investigation

## 📌 Scenario

A Security Operations Center (SOC) detected unusual outbound traffic from an internal workstation.
The traffic was flagged by a monitoring system because it attempted to communicate with an unknown external server.

The purpose of this investigation is to analyze the suspicious activity and determine whether it indicates a potential cyber attack.

---

## 📂 Network Activity Log

Example network traffic log:

```text
Timestamp           Source IP       Destination IP     Port     Action
-----------------------------------------------------------------------
2026-03-04 10:22:11 192.168.1.45    185.199.108.153    443      Outbound Connection
2026-03-04 10:22:14 192.168.1.45    185.199.108.153    443      Outbound Connection
2026-03-04 10:22:19 192.168.1.45    185.199.108.153    443      Outbound Connection
```

---

## 🔎 Investigation

Findings:

* Repeated outbound connections from the same internal workstation
* Communication with an unknown external IP
* Traffic pattern suggests possible command-and-control (C2) communication

Possible Indicators of Compromise (IOC):

* Suspicious external IP address
* Unusual network traffic pattern
* Repeated outbound connections

---

## ⚠ Threat Assessment

Potential Threat:

Command-and-Control Communication

Possible Scenario:

A compromised system may be communicating with an attacker-controlled server.

Risk Level: High

Potential Impact:

* Data exfiltration
* Malware persistence
* Remote attacker control

---

## 🛠 Incident Response Actions

Recommended response actions:

1. Isolate affected workstation from network
2. Investigate running processes on the host
3. Perform malware scan
4. Block suspicious IP address at firewall
5. Collect forensic evidence for further analysis

---

## 🧠 MITRE ATT&CK Mapping

Technique:

T1071 – Application Layer Protocol

Description:

Attackers use common network protocols such as HTTPS to communicate with command-and-control servers.

---

## 🔐 Security Improvements

Recommended controls:

* Network traffic monitoring
* Endpoint detection and response (EDR)
* Threat intelligence integration
* SIEM alerting rules

---

## 🎯 Skills Demonstrated

* Threat detection
* Network traffic investigation
* Indicator of compromise (IOC) analysis
* Incident response planning
* MITRE ATT&CK framework understanding
