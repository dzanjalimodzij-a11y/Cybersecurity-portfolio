# Active Directory Attack Path Lab

## 1. Project Overview

This project documents the design and analysis of an Active Directory (AD) lab environment with intentional misconfigurations, used to simulate realistic enterprise attack paths. The goal is to identify how an attacker could escalate privileges within an AD domain — and to map those paths to the MITRE ATT&CK framework with corresponding defensive recommendations.

> ⚠️ **All activity was conducted in an isolated local lab environment. No real AD infrastructure was accessed or targeted.**

---

## 2. Scenario

A small enterprise environment is simulated with a Windows Server 2019 Domain Controller and two Windows 10 workstations. The AD environment was intentionally configured with common real-world misconfigurations — such as Kerberoastable accounts, overprivileged service accounts, and weak ACLs — to demonstrate how attackers identify and exploit these weaknesses. The analysis documents the attack paths discovered and provides actionable hardening recommendations.

---

## 3. Objectives

- Design and build a realistic (misconfigured) AD lab environment
- Enumerate the AD environment using standard attacker tooling
- Identify privilege escalation and lateral movement opportunities
- Map all attack paths to MITRE ATT&CK techniques
- Produce a findings report with severity ratings
- Provide detailed defensive recommendations for each finding

---

## 4. Tools Used

| Tool | Purpose |
|------|---------|
| BloodHound / SharpHound | AD enumeration and attack path visualisation |
| PowerView | AD enumeration via PowerShell |
| Impacket | Kerberos attacks and lateral movement simulation |
| Rubeus | Kerberoasting and ticket manipulation |
| Mimikatz | Credential extraction (lab only) |
| MITRE ATT&CK Navigator | Technique mapping |

*[Update with specific tools and versions used]*

---

## 5. Methodology

1. **Lab Design** — Designed AD environment with documented misconfigurations. See [lab-design.md](./lab-design.md).
2. **Enumeration** — Performed AD enumeration using BloodHound/SharpHound and PowerView to map the environment.
3. **Attack Path Analysis** — Identified privilege escalation routes from a low-privileged user to Domain Admin. See [attack-path-analysis.md](./attack-path-analysis.md).
4. **MITRE ATT&CK Mapping** — Mapped each technique used to the relevant ATT&CK technique ID. See [mitre-attack-mapping.md](./mitre-attack-mapping.md).
5. **Findings Documentation** — Documented each vulnerability/misconfiguration with severity, impact, and evidence.
6. **Defensive Recommendations** — Produced hardening guidance for each finding. See [defensive-recommendations.md](./defensive-recommendations.md).

---

## 6. Evidence / Screenshots

> 📁 Screenshots stored in [`screenshots/`](./screenshots/)

| Screenshot | Description |
|-----------|-------------|
| `[PLACEHOLDER]` | BloodHound graph — attack path from user to Domain Admin |
| `[PLACEHOLDER]` | Kerberoastable accounts identified |
| `[PLACEHOLDER]` | ACL misconfiguration highlighted in BloodHound |
| `[PLACEHOLDER]` | Lateral movement demonstrated via [technique] |

---

## 7. Key Findings

> ⚠️ *To be completed on project conclusion.*

**Placeholder finding categories:**
- Kerberoastable service accounts with weak passwords
- Accounts with DCSync rights outside Domain Admins
- Misconfigured ACLs enabling privilege escalation
- Unconstrained delegation enabled on workstations
- Password reuse across privileged accounts

---

## 8. Lessons Learned

> *To be completed on project conclusion.*

---

## 9. Employer Relevance

This project demonstrates skills directly applicable to:
- Junior / Mid-level Penetration Tester roles
- Red Team Analyst positions
- Purple Team / Detection Engineering roles
- Identity and Access Management (IAM) security roles

Understanding Active Directory attack paths is a core competency for any security professional working in enterprise Windows environments.

---

## 10. Status

🔄 **In Progress**
