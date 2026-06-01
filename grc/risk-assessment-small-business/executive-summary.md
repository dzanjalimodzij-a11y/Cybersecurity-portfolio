# Executive Summary — Cyber Risk Assessment

**Organisation:** BrightPath Tutoring Ltd
**Document Reference:** GRC-RA-ES-001
**Date:** 2026-06-01
**Prepared by:** Justin Dzanjalimodzi
**Classification:** Confidential — Directors

## Purpose

This summary presents the results of a cyber risk assessment of BrightPath Tutoring Ltd in plain, non-technical language for the directors. It explains where the business is most exposed and what to do first. Full detail is in the accompanying [risk register](./risk-register.md) and [control recommendations](./control-recommendations.md).

---

## The situation in one paragraph

BrightPath is a small, online-first tutoring business that handles **children's personal data**, takes **online payments**, and runs almost entirely on a few cloud services and a **WordPress website** — with **no dedicated IT or security staff**. This is a high-value, frequently targeted profile. The good news is that the most important risks can be reduced quickly and cheaply, mostly using tools the business already pays for.

---

## Risk profile

The assessment identified and scored **10 risks**:

| Risk level | Number of risks |
|-----------|:---------------:|
| 🔴 Critical | 2 |
| 🟠 High | 7 |
| 🟡 Medium | 1 |
| 🟢 Low | 0 |

**The two critical risks are:**

1. **Weak Microsoft 365 account security (score 20).** Without multi-factor authentication (MFA), a single stolen or guessed password could give an attacker full access to email and to children's personal data — a serious, reportable data breach.
2. **Ransomware infection (score 20).** With no modern endpoint protection and untested backups, a ransomware attack could stop the business operating and permanently lose student records.

---

## Top priority actions

These five actions remove most of the risk for very little cost:

| # | Action | Cost | Effort |
|---|--------|------|--------|
| 1 | Turn on multi-factor authentication (MFA) for everyone in Microsoft 365 | Included in licence | 1–2 days |
| 2 | Use separate admin accounts and review the Microsoft Secure Score | Included | Low |
| 3 | Turn on Microsoft Defender (EDR) and automatic updates on all laptops | Minimal | Low–Medium |
| 4 | Set up and **test** proper backups (3-2-1) | A few £/user/month | Medium |
| 5 | Write a simple incident response plan (including the ICO 72-hour breach rule) | Low | Low–Medium |

---

## Why this matters to the business

- **Regulatory:** BrightPath processes children's data, so UK GDPR and the Data Protection Act 2018 apply with heightened expectations. A serious breach must be reported to the ICO within 72 hours and can attract fines and mandatory parent notifications.
- **Reputational:** Parents trust BrightPath with their children. A breach or a disrupted lesson (e.g., an uninvited stranger joining) would damage that trust quickly.
- **Operational & financial:** Ransomware or a lost website during enrolment season would directly hit revenue.

---

## Recommended next steps

1. Approve this assessment and the risk register.
2. Assign an owner and a target date to each Priority 1 action and complete them within 30 days.
3. Schedule the Priority 2 actions over the following 60–90 days.
4. Re-review the risk register in six months to confirm risks have reduced.

> For technical detail, see the [risk register](./risk-register.md), [control recommendations](./control-recommendations.md), and [NIST CSF mapping](./nist-csf-mapping.md).
