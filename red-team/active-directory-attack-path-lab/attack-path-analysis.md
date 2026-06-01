# Attack Path Analysis — Active Directory Lab

## Overview

This document describes the attack paths identified during the lab, tracing the route from an initial low-privileged foothold to full Domain Admin compromise. Each step is documented with the technique used, the evidence collected, and the MITRE ATT&CK reference.

---

## Starting Position

**Initial Access:** Low-privileged domain user account (`helpdesk-user`)  
**Starting machine:** WS01 (workstation)  
**Objective:** Achieve Domain Admin privileges on DC01

---

## Attack Path 1 — Kerberoasting to Privilege Escalation

### Step 1: Enumeration

**Technique:** AD Enumeration  
**MITRE ATT&CK:** T1087.002 — Account Discovery: Domain Account

> [PLACEHOLDER — Describe enumeration steps performed. E.g.:]
> Using BloodHound/SharpHound, the domain was enumerated to map users, groups, ACLs, and delegation settings. SharpHound was run with the `All` collection method to gather comprehensive domain data.

```
[PLACEHOLDER — Add command used and relevant output]
Example:
.\SharpHound.exe -c All
```

**Findings from enumeration:**
- [PLACEHOLDER — List key findings: Kerberoastable accounts, misconfigured ACLs, etc.]

---

### Step 2: Kerberoasting

**Technique:** Kerberoasting  
**MITRE ATT&CK:** T1558.003 — Steal or Forge Kerberos Tickets: Kerberoasting

> [PLACEHOLDER — Describe the Kerberoasting attack against the `svc-sql` service account]

```
[PLACEHOLDER — Add command used]
Example: Rubeus.exe kerberoast /outfile:hashes.txt
```

**Result:** [PLACEHOLDER — Service ticket hash captured for `svc-sql`]

**Offline cracking:** [PLACEHOLDER — Hash cracked offline using wordlist attack, revealing plaintext password]

---

### Step 3: ACL Abuse — Privilege Escalation to Domain Admin

**Technique:** ACL Modification / Abuse  
**MITRE ATT&CK:** T1484.001 — Domain Policy Modification

> [PLACEHOLDER — Describe how the GenericAll ACL on the `helpdesk-user` account was abused to add the account to Domain Admins or reset a privileged account password]

```
[PLACEHOLDER — Add command used]
```

**Result:** [PLACEHOLDER — helpdesk-user added to Domain Admins group]

---

### Step 4: Domain Admin Access

**Technique:** Valid Accounts  
**MITRE ATT&CK:** T1078.002 — Valid Accounts: Domain Accounts

> [PLACEHOLDER — Describe access achieved as Domain Admin. E.g., DCSync attack performed to extract all domain credential hashes]

```
[PLACEHOLDER — Add command used]
```

**Result:** [PLACEHOLDER — Full domain compromise achieved]

---

## Attack Path 2 — [PLACEHOLDER — Alternative path]

> *[PLACEHOLDER — Document additional attack paths identified, e.g., via unconstrained delegation or AS-REP roasting]*

---

## Attack Path Diagram

> 📁 Add BloodHound screenshot or attack path diagram to `screenshots/`

```
[PLACEHOLDER — Text representation of attack path]

helpdesk-user
    │
    ▼ (Kerberoasting → password cracking)
svc-sql credentials
    │
    ▼ (ACL abuse — GenericAll)
Domain Admins group membership
    │
    ▼
DOMAIN ADMIN ✓
```

---

## Summary

| Step | Technique | MITRE ID | Difficulty |
|------|-----------|----------|-----------|
| 1 | AD Enumeration (BloodHound) | T1087.002 | Low |
| 2 | Kerberoasting | T1558.003 | Low–Medium |
| 3 | ACL Abuse | T1484.001 | Medium |
| 4 | Domain Admin access | T1078.002 | Low (once achieved) |
