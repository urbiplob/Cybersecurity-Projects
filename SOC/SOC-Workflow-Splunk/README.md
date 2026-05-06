# SOC Workflow Simulation and Windows Security Event Investigation Using Splunk SIEM

## Project Overview

This project demonstrates a SOC (Security Operations Center) workflow simulation using Splunk SIEM for monitoring and investigating Windows Security Events within a local Windows environment.

The objective of this project was to simulate real-world SOC analyst responsibilities including:

- Security event monitoring
- Authentication analysis
- Failed login detection
- Privileged access monitoring
- Event correlation
- Threat hunting
- SIEM dashboard creation

The project was performed using Splunk Enterprise installed on a local Windows machine.

---

# Environment Setup

## Operating System
- Windows 11

## SIEM Platform
- Splunk Enterprise

## Log Sources
- WinEventLog:Security
- WinEventLog:System
- WinEventLog:Application
- Perfmon Logs

---

# Project Objectives

- Configure Splunk SIEM in a Windows environment
- Ingest and analyze Windows Event Logs
- Monitor successful and failed authentication events
- Investigate privileged logon activity
- Perform event correlation using SPL queries
- Create a mini SOC monitoring dashboard
- Simulate real-world SOC investigation workflow

---

# Key Windows Event IDs

| Event ID | Description |
|---|---|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4672 | Special Privileges Assigned to New Logon |

---

# Splunk Queries Used

## Source Overview

```spl
index=*
| stats count by source
