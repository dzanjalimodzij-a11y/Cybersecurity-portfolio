# Detection Rules — Windows Sysmon Detection Lab

This document contains the detection logic developed during the lab. Rules are written in [SIEM query language — e.g., SPL / KQL / Lucene] and are mapped to MITRE ATT&CK techniques.

---

## Rule Format

Each rule includes:
- **Name** — Descriptive rule name
- **MITRE ATT&CK** — Technique ID and name
- **Description** — What the rule detects and why it matters
- **Query** — The detection logic
- **False Positive Considerations** — Known benign activity that may trigger the rule
- **Severity** — Low / Medium / High / Critical

---

## Detection Rules

---

### Rule 1: Suspicious PowerShell Encoded Command

**MITRE ATT&CK:** T1059.001 — Command and Scripting Interpreter: PowerShell  
**Severity:** High

**Description:** Detects PowerShell execution with Base64-encoded command arguments, a common technique used by attackers to obfuscate malicious scripts.

```
[PLACEHOLDER — Add your SIEM query here]

Example (Splunk SPL):
index=sysmon EventCode=1
| where Image LIKE "%powershell.exe"
| where CommandLine LIKE "%-EncodedCommand%" OR CommandLine LIKE "%-enc %"
| table _time, ComputerName, User, CommandLine, ParentImage
```

**False Positive Considerations:** Some legitimate administrative scripts and software deployment tools use encoded commands. Tune by whitelisting known ParentImage paths (e.g., specific management software executables).

---

### Rule 2: Process Created by LSASS (Credential Access Indicator)

**MITRE ATT&CK:** T1003.001 — OS Credential Dumping: LSASS Memory  
**Severity:** Critical

**Description:** Detects unusual process access to lsass.exe, which may indicate credential dumping attempts.

```
[PLACEHOLDER — Add your SIEM query here]

Example (Splunk SPL):
index=sysmon EventCode=10
| where TargetImage LIKE "%lsass.exe"
| where NOT (SourceImage LIKE "%MsMpEng.exe" OR SourceImage LIKE "%svchost.exe")
| table _time, ComputerName, SourceImage, TargetImage, GrantedAccess
```

**False Positive Considerations:** Antivirus and EDR tools legitimately access LSASS. Build an exclusion list of known-good SourceImage paths.

---

### Rule 3: Scheduled Task Created via Command Line

**MITRE ATT&CK:** T1053.005 — Scheduled Task/Job: Scheduled Task  
**Severity:** Medium

**Description:** Detects creation of scheduled tasks using schtasks.exe, which attackers use for persistence.

```
[PLACEHOLDER — Add your SIEM query here]

Example (Splunk SPL):
index=sysmon EventCode=1
| where Image LIKE "%schtasks.exe"
| where CommandLine LIKE "%/create%"
| table _time, ComputerName, User, CommandLine, ParentImage
```

**False Positive Considerations:** Legitimate software installers and update tools create scheduled tasks. Review ParentImage and CommandLine to confirm.

---

### Rule 4: Lateral Movement — Remote Service Creation

**MITRE ATT&CK:** T1021.002 — Remote Services: SMB/Windows Admin Shares  
**Severity:** High

**Description:** Detects service creation events that may indicate lateral movement via remote service installation.

```
[PLACEHOLDER — Add your SIEM query here]
```

**False Positive Considerations:** [To be completed during lab]

---

### Rule 5: [PLACEHOLDER — Add additional rules as developed]

**MITRE ATT&CK:** [Technique ID — Technique Name]  
**Severity:** [Level]

**Description:** [What this rule detects]

```
[PLACEHOLDER — Query]
```

**False Positive Considerations:** [To be completed]

---

## Detection Coverage Map

| MITRE Technique | Rule | Status |
|----------------|------|--------|
| T1059.001 — PowerShell | Rule 1 | ✅ Implemented |
| T1003.001 — LSASS Dumping | Rule 2 | ✅ Implemented |
| T1053.005 — Scheduled Task | Rule 3 | ✅ Implemented |
| T1021.002 — SMB Lateral Movement | Rule 4 | 🔄 In Progress |
| [Add more as lab develops] | | 📋 Planned |

---

## Tuning Notes

> *Document any adjustments made to rules during testing to reduce false positives or improve detection fidelity.*

- [PLACEHOLDER — e.g., "Rule 1 modified to exclude known software deployment tool path after 12 false positives in first 24 hours"]
