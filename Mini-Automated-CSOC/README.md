# Mini Automated Cyber Security Operations Center (CSOC)

A laboratory-based automated Cyber Security Operations Center built using
Wazuh, Windows, Ubuntu Server, Kali Linux, n8n, and Telegram.

## Project Overview

This project demonstrates a small-scale CSOC capable of security monitoring,
threat detection, automated incident response, alert notification, and
security visualization.

##  Architecture

Kali Linux
     │
     │ Security Testing
     ▼
Ubuntu Wazuh Server
     │
     ├── Wazuh Manager
     ├── Wazuh Indexer
     ├── Wazuh Dashboard
     └── n8n
          │
          ▼
      Telegram

Windows Host
     │
     └── Wazuh Agent
          │
          ▼
     Wazuh Manager

## Detection Modules

- SSH Authentication Failure Detection
- Ubuntu SSH Brute-Force Detection
- Windows Brute-Force Detection
- Windows Firewall Detection
- Suspicious PowerShell Base64 Detection
- File Integrity Monitoring (FIM)

##  Automated Incident Response

Ubuntu SSH brute-force attacks trigger Wazuh Active Response.

Detection condition:

5 failed SSH attempts
        ↓
Same Source IP
        ↓
Within 120 seconds
        ↓
Rule 100101
        ↓
firewall-drop
        ↓
Block IP for 120 seconds
        ↓
Automatic Unblock

##  Automation

Wazuh alerts are integrated with n8n.

Wazuh
  ↓
Webhook
  ↓
Severity Filter
  ↓
Alert Processing
  ↓
Telegram

High-severity alerts are automatically sent to Telegram.

##  Dashboards

Two Wazuh dashboards were created:

1. Mini CSOC Security Overview
2. CSOC Incident Detection & Response

The dashboards provide visibility into:

- Security alerts
- Alert severity
- Brute-force activity
- PowerShell activity
- File Integrity Monitoring
- Active Response events
- Detection rules

##  Technologies

- Wazuh
- Splunk
- Ubuntu Server
- Windows
- Kali Linux
- n8n
- Docker
- Telegram
- Nmap
- Wireshark
- MITRE ATT&CK

##  Key Outcome

The project successfully demonstrated an end-to-end security workflow:

Detection → Analysis → Response → Notification → Visualization

##  Project Screenshots

See the `Screenshots/`, `Dashboards/`, and `Architecture/` directories.

##  Documentation

[ View PDF Report]([url](https://github.com/urbiplob/Cybersecurity-Projects/blob/main/Mini-Automated-CSOC/Documentation/Mini-Automated-CSOC-Report.pdf))
