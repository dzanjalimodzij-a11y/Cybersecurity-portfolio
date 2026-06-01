# Control Recommendations — BrightPath Tutoring Ltd

**Document Reference:** GRC-RA-CR-001
**Version:** 1.0
**Date:** 2026-06-01
**Classification:** Internal — Confidential

The recommendations are proportionate to a small organisation with limited internal IT and security capacity.

---

## 1. Overview

These recommendations are prioritised by the [risk register](./risk-register.md) and chosen to be **affordable and achievable** for a small business — most are included in services BrightPath already pays for (Microsoft 365, Windows, Stripe, WordPress). Each control is mapped to the [NIST Cybersecurity Framework](./nist-csf-mapping.md) and tagged by control type: **Technical (T)**, **Procedural (P)**, or **Physical (Ph)**.

---

## 2. Priority 1 — Critical & urgent (within 30 days)

### REC-01 — Enforce multi-factor authentication (MFA) across Microsoft 365
- **Addresses:** R-02, R-01, R-04
- **Type:** Technical
- **Action:** Enforce MFA for every user via Conditional Access; require it first for the directors/global admins. Disable legacy authentication. Use the Microsoft Authenticator app.
- **Effort / cost:** Low (1–2 days) / included in M365 licensing.

### REC-02 — Harden Microsoft 365 admin and identity
- **Addresses:** R-02
- **Type:** Technical + Procedural
- **Action:** Create separate admin accounts (no day-to-day email on global admin); enforce a strong password policy; enable the unified audit log; review the Microsoft Secure Score.
- **Effort / cost:** Low / included.

### REC-03 — Deploy endpoint protection (EDR) and patching
- **Addresses:** R-04
- **Type:** Technical
- **Action:** Enable Microsoft Defender Antivirus/EDR on all devices; turn on automatic Windows and application updates; consider upgrading to Microsoft 365 Business Premium for Defender for Business + Intune.
- **Effort / cost:** Low–Medium / minimal (or a small per-user uplift for Business Premium).

### REC-04 — Implement and test backups (3-2-1)
- **Addresses:** R-09, R-04
- **Type:** Technical + Procedural
- **Action:** Add a dedicated third-party Microsoft 365 backup; keep an independent off-site copy; **test a restore** and document it. Protect backups from deletion.
- **Effort / cost:** Medium / low (a few £/user/month).

---

## 3. Priority 2 — High (within 60–90 days)

### REC-05 — Secure the WordPress website
- **Addresses:** R-03
- **Type:** Technical + Procedural
- **Action:** Enable automatic updates; remove unused plugins/themes; enforce strong admin passwords + MFA on the WordPress login; install a reputable security/WAF plugin; schedule off-site site backups.
- **Effort / cost:** Low / low.

### REC-06 — Enforce full-disk encryption and device management
- **Addresses:** R-05
- **Type:** Technical + Physical + Procedural
- **Action:** Enable BitLocker on all Windows laptops with recovery keys escrowed; manage devices with Intune to enable remote wipe; enforce automatic screen lock; set a BYOD minimum-standard policy.
- **Effort / cost:** Medium / included (BitLocker) + Intune via Business Premium.

### REC-07 — Protect student/customer data (UK GDPR)
- **Addresses:** R-06
- **Type:** Procedural + Technical
- **Action:** Introduce a data classification & handling policy; apply least-privilege access; restrict external sharing in M365 (no open "anyone with the link"); define a retention/deletion schedule; maintain a Record of Processing Activities (ROPA).
- **Effort / cost:** Medium / low.

### REC-08 — Establish an incident response process
- **Addresses:** R-08
- **Type:** Procedural
- **Action:** Write a short incident response plan with roles, contacts, and steps; document the ICO 72-hour breach-reporting procedure; obtain cyber insurance; run an annual tabletop exercise.
- **Effort / cost:** Low–Medium / low.

### REC-09 — Confirm payment security posture
- **Addresses:** R-07
- **Type:** Technical + Procedural
- **Action:** Confirm card data is handled only by Stripe hosted checkout (never stored by BrightPath); enforce HTTPS site-wide; complete the PCI DSS **SAQ-A**; keep the checkout integration updated.
- **Effort / cost:** Low / included.

---

## 4. Priority 3 — Medium & ongoing (within 90+ days)

### REC-10 — Security awareness training
- **Addresses:** R-01, R-06, R-04
- **Type:** Procedural
- **Action:** Mandatory annual awareness training covering phishing, data handling, and reporting; quarterly simulated phishing.
- **Effort / cost:** Low / low.

### REC-11 — Secure online lesson delivery
- **Addresses:** R-10
- **Type:** Technical + Procedural
- **Action:** Unique links + passcodes per lesson; enable waiting rooms and host controls; restrict screen sharing; control storage and sharing of recordings; document a safeguarding policy.
- **Effort / cost:** Low / included.

---

## 5. Recommendation summary

| Rec | Control | Addresses | Type | Priority |
|-----|---------|-----------|------|----------|
| REC-01 | Enforce MFA | R-02, R-01, R-04 | T + P | 1 |
| REC-02 | Harden M365 admin/identity | R-02 | T + P | 1 |
| REC-03 | EDR + patching | R-04 | T | 1 |
| REC-04 | Tested 3-2-1 backups | R-09, R-04 | T + P | 1 |
| REC-05 | Secure WordPress | R-03 | T + P | 2 |
| REC-06 | Disk encryption + MDM | R-05 | T + Ph + P | 2 |
| REC-07 | Protect student data | R-06 | P + T | 2 |
| REC-08 | Incident response process | R-08 | P | 2 |
| REC-09 | Payment security (PCI SAQ-A) | R-07 | T + P | 2 |
| REC-10 | Awareness training | R-01, R-06, R-04 | P | 3 |
| REC-11 | Secure lesson delivery | R-10 | T + P | 3 |

**Control type key:** T = Technical · P = Procedural · Ph = Physical
