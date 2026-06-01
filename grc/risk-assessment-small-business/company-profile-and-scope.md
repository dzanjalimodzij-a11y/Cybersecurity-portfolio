# Company Profile and Assessment Scope

**Document Reference:** GRC-RA-CP-001
**Version:** 1.0
**Date:** 2026-06-01
**Prepared by:** Justin Dzanjalimodzi
**Classification:** Internal — Confidential

## 1. Company profile

| Attribute | Detail |
|-----------|--------|
| Organisation | BrightPath Tutoring Ltd |
| Sector | Education / online tutoring |
| Location | Manchester, United Kingdom (remote-first) |
| Size | ~10 people: 2 directors, 1 office administrator, 7 tutors (mix of employed and self-employed contractors) |
| Customers | Parents of secondary school students (ages 11–18) across the UK |
| Annual revenue | ~£300,000 |
| Service | Online 1:1 and small-group tutoring delivered over video, plus learning resources |

BrightPath Tutoring is a small, fast-growing business that delivers all of its teaching online. It has **no dedicated IT or security staff**; one of the directors administers Microsoft 365, and an external IT contractor is used on an ad-hoc basis. This is typical of a small UK SME and shapes the recommendations in this assessment — controls must be **low-cost, low-maintenance, and largely achievable with tools the business already pays for**.

---

## 2. Business context that drives risk

Three characteristics make BrightPath's risk profile higher than a typical 10-person business:

1. **It processes children's personal data.** Names, ages, schools, contact details, learning needs, and lesson recordings relate to minors. UK GDPR treats this as requiring heightened care, and a breach carries significant regulatory and reputational consequences.
2. **It takes online payments.** Parents pay for lessons online, bringing card-payment security and fraud into scope.
3. **It is highly dependent on a handful of cloud and web services.** Microsoft 365, a WordPress website, a video platform, and a payment provider are effectively the entire business. Loss of any one of them disrupts operations immediately.

---

## 3. Technology environment

| Component | Description |
|-----------|-------------|
| Microsoft 365 (Business Standard) | Email, Teams, SharePoint, OneDrive — core collaboration and storage |
| WordPress website | Public marketing site, blog, and lesson-booking/enquiry forms; self-hosted on a shared-hosting plan |
| Video conferencing | Zoom / Microsoft Teams used to deliver live lessons (some recorded) |
| Online payments | Stripe hosted checkout, embedded on the WordPress site; card data is not handled by BrightPath directly |
| Endpoints | ~10 Windows laptops — a mix of company-owned and personal (BYOD) devices used by tutors |
| Accounting | Xero (cloud) for invoicing and bookkeeping |
| Identity | Microsoft Entra ID (Azure AD) accounts for staff; customers self-register on the website |

---

## 4. Scope of this assessment

### In scope

- Microsoft 365 tenant and the data stored within it (email, OneDrive, SharePoint, Teams)
- The WordPress website and its booking/enquiry functionality
- The online payment flow (as it relates to BrightPath's responsibilities)
- Staff endpoints (laptops) used to access business data
- Student and parent personal data throughout its lifecycle
- Delivery of online lessons (access control and safeguarding aspects)
- Staff security behaviour and organisational processes (e.g., incident response)

### Out of scope

- The internal infrastructure of third-party providers (Stripe, Microsoft, Zoom, the WordPress host) — these are assessed only through their interface with BrightPath and via supplier assurance.
- Physical security of staff home offices beyond reasonable, proportionate measures.
- Detailed financial audit, HR processes, and non-security business operations.
- Penetration testing or active exploitation — this is a paper-based risk assessment, not a technical test.

---

## 5. Assumptions

- The business currently has **no formal security programme**, no documented policies, and no incident response plan.
- Microsoft 365 is on default configuration; multi-factor authentication (MFA) is **not** enforced for all users.
- The WordPress site is maintained informally, with plugin/theme updates applied irregularly.
- Backups exist (Microsoft 365 retention) but have **never been tested** through a restore.
- Staff have received **no formal security awareness training**.

These assumptions represent a realistic "before" state and define the baseline against which residual risk is measured.

---

## 6. Objectives

- Identify and classify BrightPath's information assets.
- Identify credible threats and the vulnerabilities that expose those assets.
- Assess and rate each risk using a consistent, repeatable methodology.
- Recommend prioritised, proportionate, and affordable controls.
- Map recommendations to the NIST Cybersecurity Framework.
- Communicate the results clearly to the directors.

---

## 7. Document control

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 1.0 | 2026-06-01 | Justin Dzanjalimodzi | Initial assessment |
