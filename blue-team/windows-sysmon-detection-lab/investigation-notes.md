# Investigation Notes — Windows Sysmon Detection Lab

This document records the step-by-step investigation process for alerts generated during the lab. Each entry follows a structured triage approach.

---

## Investigation Log Format

Each alert investigation follows this structure:

1. **Alert triggered** — Timestamp, rule name, affected host
2. **Initial triage** — Is this a true positive, false positive, or requires further investigation?
3. **Evidence gathered** — Relevant log entries, process trees, file activity, network connections
4. **Timeline reconstruction** — Chronological sequence of events
5. **Conclusion** — Determination and escalation decision

---

## Investigation Entry 1

**Date/Time:** `[PLACEHOLDER — e.g., 2024-11-10 14:32:07 UTC]`  
**Rule Triggered:** `[PLACEHOLDER — Rule name]`  
**Affected Host:** `[PLACEHOLDER — Hostname]`  
**User Account:** `[PLACEHOLDER — Username]`  
**Initial Severity:** `[High / Medium / Low]`

### Evidence Gathered

```
[PLACEHOLDER — Paste relevant Sysmon log entries here]

Example format:
EventCode: 1
UtcTime: [timestamp]
ProcessGuid: {guid}
Image: C:\Windows\System32\powershell.exe
CommandLine: powershell.exe -EncodedCommand [base64 string]
ParentImage: C:\Windows\explorer.exe
User: LAB\testuser
```

### Process Tree

```
[PLACEHOLDER — Document the parent-child process chain]

Example:
explorer.exe (PID 1234)
  └─ powershell.exe -EncodedCommand [...]  (PID 5678)
       └─ [child process if any]
```

### Timeline

| Time (UTC) | Event | Source |
|-----------|-------|--------|
| `[PLACEHOLDER]` | `[Event description]` | Sysmon Event ID [X] |
| `[PLACEHOLDER]` | `[Event description]` | Sysmon Event ID [X] |

### Conclusion

**Verdict:** `[True Positive / False Positive / Benign Unusual Activity]`

**Reasoning:** `[PLACEHOLDER — Explain why this determination was made based on the evidence]`

**Action Taken:** `[PLACEHOLDER — e.g., Escalated to incident report / Tuned rule / No action required]`

---

## Investigation Entry 2

> *[PLACEHOLDER — Add additional investigation entries as alerts are triaged during the lab]*

---

## Triage Summary

| Alert # | Rule | Verdict | Action |
|---------|------|---------|--------|
| 1 | [Rule name] | [Verdict] | [Action] |
| 2 | | | |
| 3 | | | |

---

## Notes and Observations

> *[PLACEHOLDER — Record any observations about detection gaps, unexpected attacker behaviours, or interesting log patterns observed during the investigation process]*
