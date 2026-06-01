# Control Mapping — Mini ISMS Policy Pack

This document maps each policy in the ISMS Policy Pack to the relevant ISO 27001:2022 controls and NIST Cybersecurity Framework (CSF) categories, demonstrating alignment with recognised international standards.

---

## Policy to ISO 27001 Control Mapping

| Policy | ISO 27001:2022 Clause(s) | Control Description |
|--------|------------------------|-------------------|
| Acceptable Use Policy (POL-001) | 5.10 | Acceptable use of information and other associated assets |
| Acceptable Use Policy (POL-001) | 8.1 | User endpoint devices |
| Password Policy (POL-002) | 5.17 | Authentication information |
| Password Policy (POL-002) | 8.5 | Secure authentication |
| Access Control Policy (POL-003) | 5.15 | Access control |
| Access Control Policy (POL-003) | 5.16 | Identity management |
| Access Control Policy (POL-003) | 5.18 | Access rights |
| Incident Response Policy (POL-004) | 5.24 | Information security incident management planning and preparation |
| Incident Response Policy (POL-004) | 5.25 | Assessment and decision on information security events |
| Incident Response Policy (POL-004) | 5.26 | Response to information security incidents |
| Incident Response Policy (POL-004) | 5.27 | Learning from information security incidents |
| Backup Policy (POL-005) | 8.13 | Information backup |
| Data Classification Policy (POL-006) | 5.12 | Classification of information |
| Data Classification Policy (POL-006) | 5.13 | Labelling of information |

---

## Policy to NIST CSF Mapping

| Policy | NIST CSF Function | NIST CSF Category |
|--------|------------------|------------------|
| Acceptable Use Policy | Protect | PR.AT — Awareness and Training; PR.IP — Information Protection Processes |
| Password Policy | Protect | PR.AC — Identity Management, Authentication and Access Control |
| Access Control Policy | Protect | PR.AC — Identity Management, Authentication and Access Control |
| Incident Response Policy | Respond | RS.RP — Response Planning; RS.CO — Communications; RS.AN — Analysis |
| Incident Response Policy | Recover | RC.RP — Recovery Planning |
| Backup Policy | Protect | PR.IP-4 — Backups of information conducted, maintained, and tested |
| Data Classification Policy | Identify | ID.AM — Asset Management |
| Data Classification Policy | Protect | PR.DS — Data Security |

---

## NIST CSF Functions Coverage Summary

| Function | Coverage |
|----------|---------|
| **Identify** | Data Classification Policy, Risk Assessment |
| **Protect** | Acceptable Use, Password, Access Control, Backup, Data Classification |
| **Detect** | [PLACEHOLDER — Future: Security monitoring policy, log management] |
| **Respond** | Incident Response Policy |
| **Recover** | Backup Policy, Incident Response Policy |

---

## Gaps and Future Policies

The following areas are not yet covered by this policy pack and represent recommended additions for a more mature ISMS:

| Gap | Recommended Policy | ISO 27001 Clause |
|-----|--------------------|-----------------|
| Change management | Change Management Policy | 8.32 |
| Supplier security | Supplier Relationships Policy | 5.19, 5.20 |
| Business continuity | Business Continuity and DR Policy | 5.29, 5.30 |
| Physical security | Physical Security Policy | 7.1, 7.2, 7.3 |
| Logging and monitoring | Security Monitoring Policy | 8.15, 8.16 |
| Cryptography | Cryptographic Controls Policy | 8.24 |
