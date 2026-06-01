# Windows Sysmon Detection Lab

## 1. Project Overview

This project documents the setup of a Windows-based detection lab using Microsoft Sysmon (System Monitor) integrated with a SIEM platform. The goal was to simulate common attacker behaviours and develop detection logic to identify them through structured log analysis.

---

## 2. Scenario

A simulated enterprise environment consisting of a Windows 10 workstation and a Windows Server 2019 domain controller was built in a local virtualised lab. Sysmon was deployed to capture detailed endpoint telemetry. Common attacker techniques were executed in the lab to generate realistic log data, and detection rules were then written to identify these behaviours.

---

## 3. Objectives

- Deploy and configure Sysmon with a hardened configuration file
- Forward logs to a SIEM for centralised analysis
- Simulate attacker techniques mapped to the MITRE ATT&CK framework
- Write detection rules to identify simulated malicious activity
- Investigate generated alerts and produce an incident report

---

## 4. Tools Used

| Tool | Purpose |
|------|---------|
| Microsoft Sysmon | Endpoint telemetry and event logging |
| [SIEM Platform — e.g., Splunk / Elastic / Wazuh] | Log ingestion and alerting |
| Windows Event Viewer | Local log review |
| MITRE ATT&CK Navigator | Technique mapping |
| PowerShell | Simulation scripting |

*[Update with the specific tools used in your lab]*

---

## 5. Methodology

1. **Environment Setup** — Configured two Windows VMs (workstation + server) in an isolated network. See [lab-setup.md](./lab-setup.md).
2. **Sysmon Deployment** — Installed Sysmon using a community-recommended configuration (e.g., SwiftOnSecurity ruleset). Tuned rules to reduce noise.
3. **Log Forwarding** — Configured Windows Event Forwarding (WEF) to ship Sysmon logs to the SIEM.
4. **Attack Simulation** — Executed a series of techniques (process injection, credential dumping simulation, lateral movement indicators) in the lab environment.
5. **Detection Rule Development** — Wrote queries and alert rules in the SIEM to detect simulated activity. See [detection-rules.md](./detection-rules.md).
6. **Investigation** — Triaged generated alerts, traced activity through the log chain, and documented findings. See [investigation-notes.md](./investigation-notes.md).
7. **Reporting** — Produced a structured incident report. See [incident-report.md](./incident-report.md).

---

## 6. Evidence / Screenshots

> 📁 Screenshots are stored in the [`screenshots/`](./screenshots/) folder.

| Screenshot | Description |
|-----------|-------------|
| `[PLACEHOLDER]` | Sysmon configuration deployed and running |
| `[PLACEHOLDER]` | SIEM dashboard showing ingested Sysmon events |
| `[PLACEHOLDER]` | Alert triggered for simulated suspicious process creation |
| `[PLACEHOLDER]` | Log chain showing attack activity timeline |

*Add your screenshots to the screenshots/ folder and update this table with filenames and descriptions.*

---

## 7. Key Findings

> ⚠️ *This section will be completed once the lab exercises are finished. Findings will include specific detection gaps identified, techniques successfully detected, and any tuning required to reduce false positives.*

**Placeholder findings structure:**

- **Detected:** [Technique name — MITRE ID] — Alert fired within [X] seconds. Detection rule performed as expected.
- **Missed:** [Technique name — MITRE ID] — No alert generated. Root cause: [e.g., Sysmon event type not enabled / rule too narrow].
- **False Positive:** [Description] — Legitimate activity triggered alert. Rule tuned to exclude [condition].

---

## 8. Lessons Learned

> *To be completed on project conclusion.*

- What configuration choices had the most impact on detection quality?
- Which attacker techniques were hardest to detect and why?
- What would be done differently in a production environment?
- How did this lab improve understanding of attacker tradecraft?

---

## 9. Employer Relevance

This project demonstrates direct readiness for roles in Security Operations (SOC), Threat Detection Engineering, and Incident Response. Specific transferable skills include:

- Configuring endpoint telemetry tools in a Windows environment
- Writing and tuning detection logic in a SIEM
- Investigating alerts using structured log analysis
- Producing clear, evidence-based incident documentation

---

## 10. Status

🔄 **In Progress** — Lab environment built; attack simulations and detection rule development underway.
