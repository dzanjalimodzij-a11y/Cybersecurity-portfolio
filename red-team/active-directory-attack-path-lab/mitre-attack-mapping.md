# MITRE ATT&CK Mapping — Active Directory Attack Path Lab

This document maps all techniques used or observed during the lab to the MITRE ATT&CK Enterprise framework.

Reference: https://attack.mitre.org/

---

## Technique Map

| MITRE ID | Technique Name | Tactic | Used In Lab | Finding Reference |
|----------|---------------|--------|------------|-----------------|
| T1087.002 | Account Discovery: Domain Account | Discovery | ✅ Yes | FIND-001 |
| T1558.003 | Steal or Forge Kerberos Tickets: Kerberoasting | Credential Access | ✅ Yes | FIND-002 |
| T1558.004 | Steal or Forge Kerberos Tickets: AS-REP Roasting | Credential Access | ✅ Yes | FIND-003 |
| T1484.001 | Domain Policy Modification: Group Policy Modification | Defence Evasion, Privilege Escalation | ✅ Yes | FIND-004 |
| T1078.002 | Valid Accounts: Domain Accounts | Defence Evasion, Persistence, Privilege Escalation | ✅ Yes | Multiple |
| T1021.002 | Remote Services: SMB/Windows Admin Shares | Lateral Movement | ✅ Yes | FIND-005 |
| T1003.006 | OS Credential Dumping: DCSync | Credential Access | ✅ Yes | FIND-006 |
| T1134.001 | Access Token Manipulation: Token Impersonation | Defence Evasion, Privilege Escalation | [PLACEHOLDER] | |
| T1550.003 | Use Alternate Authentication Material: Pass the Hash | Defence Evasion, Lateral Movement | [PLACEHOLDER] | |

---

## ATT&CK Navigator Layer

> *[PLACEHOLDER — Export your ATT&CK Navigator layer file and reference it here, or include a screenshot of the navigator view showing techniques highlighted]*
>
> Export from: https://mitre-attack.github.io/attack-navigator/

---

## Tactic Coverage

| Tactic | Techniques Covered |
|--------|-------------------|
| Reconnaissance | [PLACEHOLDER] |
| Discovery | T1087.002 |
| Credential Access | T1558.003, T1558.004, T1003.006 |
| Lateral Movement | T1021.002 |
| Privilege Escalation | T1484.001, T1078.002 |
| Defence Evasion | T1078.002 |
| Persistence | [PLACEHOLDER] |
