# Lab Design — Active Directory Attack Path Lab

## Environment Overview

| Component | Details |
|-----------|---------|
| Hypervisor | [PLACEHOLDER — e.g., VMware Workstation / VirtualBox] |
| Network | Host-only isolated network — no external internet access |
| Domain Name | [PLACEHOLDER — e.g., corp.lab] |

## Virtual Machines

| VM | OS | Role | IP Address |
|----|-----|------|-----------|
| DC01 | Windows Server 2019 | Domain Controller | [PLACEHOLDER] |
| WS01 | Windows 10 Pro | Workstation (User 1) | [PLACEHOLDER] |
| WS02 | Windows 10 Pro | Workstation (User 2) | [PLACEHOLDER] |
| Kali | Kali Linux | Attacker machine | [PLACEHOLDER] |

---

## Intentional Misconfigurations

The following misconfigurations were deliberately introduced to simulate real-world AD weaknesses. These are documented for transparency and to frame the subsequent attack path analysis.

| # | Misconfiguration | Affected Object | Realistic Prevalence |
|---|-----------------|----------------|---------------------|
| 1 | Service account with Kerberoastable SPN and weak password | `svc-sql` | Very common |
| 2 | GenericAll ACL on a privileged group granted to a regular user | `helpdesk-user` → `Domain Admins` | Common |
| 3 | Unconstrained delegation enabled on a workstation | WS02 | Common |
| 4 | Password in SYSVOL / Group Policy Preferences | GPP XML file | Older environments |
| 5 | AS-REP Roastable account (pre-authentication disabled) | `svc-backup` | Less common but still found |
| 6 | Local admin password reuse across workstations | WS01, WS02 | Extremely common |

> *These misconfigurations reflect issues commonly found during real enterprise AD assessments, based on published research and penetration testing reports.*

---

## User Accounts

| Username | Role | Privileges | Notes |
|----------|------|-----------|-------|
| `helpdesk-user` | Helpdesk staff | Domain Users + GenericAll on IT OU | Starting point for attack simulation |
| `svc-sql` | SQL service account | Service account with SPN set | Kerberoastable |
| `svc-backup` | Backup service account | Pre-auth disabled | AS-REP Roastable |
| `it-admin` | IT Administrator | Local Admin on WS01, WS02 | Password reuse across machines |
| `domain-admin` | Domain Administrator | Full domain admin | Target account |

---

## Network Diagram

> 📁 Add network diagram to `../../assets/diagrams/ad-lab-network.png`

```
[PLACEHOLDER — Insert network diagram]

Example:
  Kali Linux (Attacker)
       |
  [Host-only Network: 192.168.x.0/24]
       |
  ┌────────┐     ┌──────┐     ┌──────┐
  │  DC01  │     │ WS01 │     │ WS02 │
  │  (DC)  │     │ (WS) │     │ (WS) │
  └────────┘     └──────┘     └──────┘
```
