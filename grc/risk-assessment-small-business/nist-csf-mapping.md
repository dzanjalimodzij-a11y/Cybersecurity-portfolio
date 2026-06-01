# NIST Cybersecurity Framework (CSF) Mapping

**Document Reference:** GRC-RA-NIST-001
**Version:** 1.0
**Date:** 2026-06-01
**Framework:** NIST Cybersecurity Framework (CSF) 2.0

This mapping links the recommended controls to the NIST CSF 2.0 functions used in the assessment.

---

## 1. Purpose

This document maps the recommended controls from the [control recommendations](./control-recommendations.md) to the six core functions of the **NIST Cybersecurity Framework (CSF) 2.0**. Mapping to a recognised framework shows that the recommendations form a balanced, complete programme rather than a list of disconnected fixes, and gives the directors a shared language for tracking maturity over time.

---

## 2. NIST CSF 2.0 functions

| Function | Purpose |
|----------|---------|
| **GOVERN (GV)** | Establish and monitor the cybersecurity risk management strategy, roles, and policy |
| **IDENTIFY (ID)** | Understand assets, risks, and the business context |
| **PROTECT (PR)** | Implement safeguards to limit the impact of events |
| **DETECT (DE)** | Find and analyse cybersecurity events |
| **RESPOND (RS)** | Take action on a detected incident |
| **RECOVER (RC)** | Restore capabilities and services after an incident |

---

## 3. Control-to-function mapping

| Recommendation | Control | CSF Function(s) | Example CSF Category |
|----------------|---------|-----------------|----------------------|
| REC-01 | Enforce MFA | PROTECT | PR.AA — Identity management & authentication |
| REC-02 | Harden M365 admin/identity | GOVERN, PROTECT | GV.RR, PR.AA |
| REC-03 | EDR + patching | PROTECT, DETECT | PR.PS — Platform security; DE.CM — Continuous monitoring |
| REC-04 | Tested 3-2-1 backups | RECOVER | RC.RP — Incident recovery plan execution |
| REC-05 | Secure WordPress | PROTECT, DETECT | PR.PS; DE.CM |
| REC-06 | Disk encryption + MDM | PROTECT | PR.DS — Data security; PR.PS |
| REC-07 | Protect student data | GOVERN, PROTECT | GV.PO — Policy; PR.DS; PR.AA |
| REC-08 | Incident response process | RESPOND, GOVERN | RS.MA — Incident management; GV.RR |
| REC-09 | Payment security (PCI SAQ-A) | PROTECT, GOVERN | PR.DS; GV.SC — Supply chain |
| REC-10 | Awareness training | PROTECT | PR.AT — Awareness & training |
| REC-11 | Secure lesson delivery | PROTECT | PR.AA; PR.DS |

---

## 4. Coverage summary

| CSF Function | Covered by | Coverage |
|--------------|-----------|----------|
| **GOVERN** | REC-02, REC-07, REC-08, REC-09 | Good |
| **IDENTIFY** | Asset register, threat register, this assessment | Good |
| **PROTECT** | REC-01, REC-02, REC-03, REC-05, REC-06, REC-07, REC-09, REC-10, REC-11 | Strong |
| **DETECT** | REC-03, REC-05 (plus M365 audit logging in REC-02) | Developing |
| **RESPOND** | REC-08 | Developing |
| **RECOVER** | REC-04 | Adequate |

**Observation:** As expected for a small business at the start of its security journey, the recommendations are strongest in **IDENTIFY** and **PROTECT**. **DETECT** and **RESPOND** are the natural areas for maturity improvement once the foundational protective controls are in place — for example, regularly reviewing Microsoft 365 audit logs and exercising the incident response plan.

---

## 5. Note on standards used

NIST CSF 2.0 is used here as the primary mapping framework because it is free, widely recognised, and well suited to communicating risk posture to non-technical leadership. The control recommendations also align conceptually with **ISO/IEC 27001:2022 Annex A** and the UK's **Cyber Essentials** scheme, either of which BrightPath could pursue as a formal next step (see the [conclusion](./conclusion.md)).
