# Phishing Analysis & Incident Response Playbook

## 1. Project Overview

This project demonstrates the end-to-end process of analysing a simulated phishing email campaign and developing a reusable Incident Response (IR) Playbook for phishing incidents. It covers technical email forensics, IOC extraction, and the development of structured response procedures suitable for a SOC or IT security team environment.

---

## 2. Scenario

A series of simulated phishing emails were created for analysis purposes, representing common attack patterns: credential harvesting lures, malicious attachment delivery, and business email compromise (BEC) style pretexting. Each email was analysed to extract indicators of compromise, assess the threat level, and document the findings in a format suitable for incident response teams.

> *No real phishing emails or malicious content were used. Simulated samples were created in a controlled environment.*

---

## 3. Objectives

- Analyse simulated phishing emails using a structured methodology
- Extract and document Indicators of Compromise (IOCs)
- Perform header analysis to trace email origin
- Assess any attachments or links in a safe, sandboxed environment
- Produce analysis reports for each sample
- Develop an Incident Response Playbook for phishing events
- Create a user awareness guide to support phishing prevention

---

## 4. Tools Used

| Tool | Purpose |
|------|---------|
| [Email client / .eml viewer] | View raw email headers and content |
| MXToolbox / Google Admin Toolbox | Header analysis and SPF/DKIM/DMARC checking |
| VirusTotal | URL and attachment reputation checking |
| Any.run / Joe Sandbox | Sandboxed attachment analysis |
| CyberChef | Decoding obfuscated content |
| WHOIS / URLScan.io | Domain and URL investigation |

*[Update with the specific tools used in your analysis]*

---

## 5. Methodology

1. **Sample Collection** — Simulated phishing emails sourced/created for analysis
2. **Header Analysis** — Inspected email headers for spoofed sender fields, suspicious relay hops, and authentication failures (SPF, DKIM, DMARC)
3. **Content Analysis** — Reviewed email body for social engineering techniques, urgency cues, and suspicious links
4. **Link/URL Analysis** — Extracted URLs and submitted to reputation services; examined destination pages
5. **Attachment Analysis** — Submitted attachments to sandboxes and reviewed static properties (file type, hashes, macros)
6. **IOC Extraction** — Documented all indicators for use in blocklists and SIEM rules
7. **Report Writing** — Produced structured analysis reports per sample
8. **Playbook Development** — Developed a repeatable IR playbook based on lessons from the analysis process

---

## 6. Evidence / Screenshots

> 📁 Analysis reports are in [`analysis-reports/`](./analysis-reports/)  
> 📁 Sample emails are in [`sample-emails/`](./sample-emails/)

| Item | Description |
|------|-------------|
| `[PLACEHOLDER]` | Email header analysis — Sample 1 |
| `[PLACEHOLDER]` | Sandbox analysis results — Sample 2 attachment |
| `[PLACEHOLDER]` | URLScan.io results for suspicious link |

---

## 7. Key Findings

> ⚠️ *To be completed on project conclusion.*

**Placeholder findings structure:**
- How many samples were analysed
- Common phishing techniques observed
- Most useful analysis techniques
- IOCs extracted (types and quantities)

---

## 8. Lessons Learned

> *To be completed on project conclusion.*

---

## 9. Employer Relevance

This project demonstrates readiness for Tier 1/2 SOC analyst roles and any position requiring email security or incident response skills. Specific transferable skills include:

- Structured threat analysis and documentation
- IOC extraction for SIEM and blocklist integration
- Playbook development for repeatable incident response
- User-facing communication on security threats

---

## 10. Status

🔄 **In Progress**
