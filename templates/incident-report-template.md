# Incident Report

> *Use this template for any security incident report — real (lab) or simulated. Replace all `[PLACEHOLDER]` fields.*

---

## Report Details

| Field | Value |
|-------|-------|
| Report Reference | IR-[YEAR]-[NNN] |
| Date of Report | [Date] |
| Incident Date/Time (UTC) | [Date and time] |
| Incident Type | [e.g., Malware / Phishing / Data Breach / Unauthorised Access] |
| Prepared By | [Your name] |
| Classification | [Confidential / Internal / Simulated — Educational] |
| Severity | [Critical / High / Medium / Low] |
| Status | [Open / Contained / Closed] |

---

## 1. Executive Summary

[2–3 paragraph non-technical summary of the incident. Cover: what happened, when it was detected, what systems or data were affected, what actions were taken, and the current status. Write for a non-technical reader — a manager or stakeholder who needs to understand the situation without technical detail.]

---

## 2. Incident Timeline

| Date/Time (UTC) | Event |
|----------------|-------|
| [Timestamp] | [Event description] |
| [Timestamp] | [Event description] |
| [Timestamp] | Incident detected — Alert: [alert name / detection method] |
| [Timestamp] | Analyst began triage |
| [Timestamp] | Incident confirmed as [True Positive / False Positive] |
| [Timestamp] | Containment action: [description] |
| [Timestamp] | Eradication completed |
| [Timestamp] | Normal operations restored |
| [Timestamp] | Incident report finalised |

---

## 3. Affected Systems / Users

| System / User | Role | Impact |
|--------------|------|--------|
| [Hostname / Username] | [Role] | [Description of impact] |

---

## 4. Technical Analysis

### 4.1 Initial Detection

[How was the incident detected? What alert, log, or user report triggered the investigation? Include rule name, Event IDs, or other detection indicators.]

### 4.2 Attack / Incident Description

[Describe what happened in technical terms. Include: the attack vector, techniques used (with MITRE ATT&CK references if applicable), affected systems, tools or malware identified, and any evidence of lateral movement or data exfiltration.]

**MITRE ATT&CK Techniques (if applicable):**

| Technique ID | Technique Name |
|-------------|---------------|
| [T-ID] | [Technique Name] |

### 4.3 Evidence

```
[Paste relevant log entries, command lines, file paths, or other artefacts here]
```

### 4.4 Scope Assessment

[Was the incident contained to a single system? Were other systems affected? Was any data accessed or exfiltrated? Quantify the scope as precisely as possible.]

---

## 5. Containment Actions

| Action | Taken By | Timestamp |
|--------|---------|-----------|
| [e.g., Device isolated from network] | [Name/role] | [Timestamp] |
| [e.g., User account suspended] | [Name/role] | [Timestamp] |
| [e.g., Malicious IP blocked at firewall] | [Name/role] | [Timestamp] |

---

## 6. Eradication and Recovery

[Describe steps taken to remove the threat and restore normal operations. Include: malware removal, account remediation, patch application, system rebuild if required, credential resets, and verification that the threat was fully removed.]

---

## 7. Root Cause Analysis

[What allowed this incident to occur? Identify the root cause(s) — this may be a technical gap (missing patch, no MFA), a process failure, or a human factor. Be specific and evidence-based.]

---

## 8. Recommendations

| # | Recommendation | Priority | Owner | Target Date |
|---|---------------|----------|-------|-------------|
| 1 | [Recommendation] | High | [Role] | [Date] |
| 2 | [Recommendation] | Medium | [Role] | [Date] |
| 3 | [Recommendation] | Low | [Role] | [Date] |

---

## 9. Lessons Learned

[What did this incident reveal about the organisation's (or lab's) security posture? What worked well in the response? What should be improved? This section drives continuous improvement.]

---

## 10. Appendix

### A. Screenshots / Evidence Files

> 📁 Reference files in the `screenshots/` folder

### B. Full Log Extracts

[Include full log extracts referenced in the Technical Analysis section]

### C. References

- MITRE ATT&CK: https://attack.mitre.org/
- [Other references]
