# Email Forensics & Threat Analysis

## Introduction
This project presents a forensic investigation of a suspicious email titled "Farewell." The analysis focused on validating email authenticity, tracing the originating infrastructure, decoding embedded payloads, and identifying indicators of compromise (IOCs).

## Objective
To analyze the authenticity, transmission path, and content of the email in order to identify spoofing attempts, malicious behavior, and potential threats.

## Tools Used
- MXToolbox
- MHA Header Analyzer
- VirusTotal
- IPTrackerOnline
- Base64 Decoder
- CentralOps

## Methodology
1. Email Header Analysis
2. Relay Path Examination
3. SPF/DKIM/DMARC Validation
4. Originating IP Investigation
5. Payload Decoding
6. Threat Content Assessment

## Key Findings
- SPF, DKIM, and DMARC validation passed successfully
- Email originated from legitimate ProtonMail infrastructure
- No evidence of spoofing or relay manipulation was identified
- Decoded payload contained psychologically manipulative and threatening content
- Indicators consistent with harassment and social engineering behavior were observed

## Indicators of Compromise (IOCs)
- Originating IP: 109.224.244.24
- Email Provider: ProtonMail
- Sender Domain: protonmail.com

## Conclusion
The forensic investigation confirmed that the email was technically authentic and originated from legitimate ProtonMail infrastructure. Although no spoofing or header manipulation was detected, the decoded payload contained threatening and emotionally manipulative language consistent with harassment and cyberstalking behavior.

## Full Report
[View PDF Report](./Email_Forensics_Report.pdf)
