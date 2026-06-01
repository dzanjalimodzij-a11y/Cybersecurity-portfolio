# Risk Treatment Plan

**Document Reference:** GRC-RTP-001  
**Version:** 1.0  
**Date:** [PLACEHOLDER]  
**Owner:** Managing Director  
**Classification:** Internal — Confidential

---

## Purpose

This risk treatment plan records the decisions made regarding how each risk identified in the risk register will be treated, who is responsible, and the target completion date for implementing controls.

---

## Risk Treatment Decisions

| Risk ID | Risk Description | Inherent Risk | Treatment Option | Control(s) to Implement | Responsible Owner | Target Date | Status |
|---------|-----------------|--------------|-----------------|------------------------|------------------|-------------|--------|
| RISK-001 | Ransomware attack encrypting systems and client data | Critical | Treat | EDR deployment, MFA, offline backups, staff training | IT Manager | [PLACEHOLDER] | [PLACEHOLDER] |
| RISK-002 | Phishing leading to credential compromise | Critical | Treat | MFA on all accounts, phishing simulation, security awareness training | IT Manager | [PLACEHOLDER] | [PLACEHOLDER] |
| RISK-003 | Accidental data disclosure by staff | High | Treat | Data classification training, DLP controls, clear desk policy | Operations Manager | [PLACEHOLDER] | [PLACEHOLDER] |
| RISK-004 | Theft/loss of unencrypted device | High | Treat | BitLocker encryption, MDM enrolment, remote wipe capability | IT Manager | [PLACEHOLDER] | [PLACEHOLDER] |
| RISK-005 | Insider threat — IT admin privilege abuse | High | Treat | Access reviews, separation of duties, audit logging | Managing Director | [PLACEHOLDER] | [PLACEHOLDER] |
| RISK-006 | Third-party SaaS provider breach | High | Transfer / Treat | Cyber insurance review, supplier due diligence, DPA review | Managing Director | [PLACEHOLDER] | [PLACEHOLDER] |
| RISK-007 | Unauthorised access via unsecured Wi-Fi | Medium | Treat | Guest VLAN segregation, network access control | IT Manager | [PLACEHOLDER] | [PLACEHOLDER] |
| RISK-008 | Data loss due to backup failure | High | Treat | 3-2-1 backup implementation, monthly restore testing | IT Manager | [PLACEHOLDER] | [PLACEHOLDER] |

---

## Statement of Applicability (SoA) Summary

The table below summarises which ISO 27001:2022 controls are applicable to this organisation, based on the risk treatment decisions above. A full SoA would cover all 93 controls in Annex A.

| ISO 27001 Control | Control Name | Applicable | Included / Excluded Reason |
|------------------|-------------|-----------|--------------------------|
| 5.15 | Access control | ✅ Yes | Included — manages access to all systems |
| 5.17 | Authentication information | ✅ Yes | Included — password policy required |
| 5.24 | Information security incident management | ✅ Yes | Included — incident response policy in place |
| 6.3 | Information security awareness | ✅ Yes | Included — staff training programme required |
| 8.5 | Secure authentication | ✅ Yes | Included — MFA required |
| 8.7 | Protection against malware | ✅ Yes | Included — EDR deployment |
| 8.13 | Information backup | ✅ Yes | Included — backup policy |
| 8.20 | Networks security | ✅ Yes | Included — Wi-Fi segregation |
| 8.24 | Use of cryptography | ✅ Yes | Included — device and backup encryption |

*[PLACEHOLDER — Expand to cover all applicable controls for a complete SoA]*

---

## Residual Risk Acceptance

Risks that remain after controls are implemented must be formally accepted by the Managing Director. The following risks have been accepted at residual level:

| Risk ID | Residual Risk Level | Accepted By | Date | Notes |
|---------|--------------------|-----------|----|------|
| [PLACEHOLDER] | [Level] | Managing Director | [Date] | [Notes] |

---

## Review

This plan will be reviewed:
- Annually as part of the ISMS management review
- Following any significant change in the risk environment
- Following a security incident
