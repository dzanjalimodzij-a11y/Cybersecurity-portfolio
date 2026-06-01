# Risk Register — BrightPath Tutoring Ltd

**Document Reference:** GRC-RA-RR-001
**Version:** 1.0
**Date:** 2026-06-01
**Owner:** Director
**Classification:** Internal — Confidential

Scores reflect the "before controls" (inherent risk) state described in the [company profile](./company-profile-and-scope.md).

---

## 1. Scoring summary

Risks are scored using the [risk-scoring methodology](./risk-scoring-methodology.md):

**Risk Score = Likelihood (1–5) × Impact (1–5)**

| Score | Level |
|-------|-------|
| 1–4 | Low |
| 5–9 | Medium |
| 10–16 | High |
| 17–25 | Critical |

**Control types:** Technical (T) · Procedural (P) · Physical (Ph)

---

## 2. Risk register (summary table)

| Risk ID | Risk | Asset(s) | Likelihood | Impact | Score | Level |
|---------|------|----------|:----------:|:------:|:-----:|-------|
| R-01 | Phishing attack against staff | DA-06, SY-01, PE-01–03 | 4 | 4 | **16** | High |
| R-02 | Weak Microsoft 365 account security | SY-01, DA-01, DA-02 | 4 | 5 | **20** | Critical |
| R-03 | WordPress website compromise | SY-02, DA-01, DA-02 | 4 | 3 | **12** | High |
| R-04 | Ransomware infection | SY-05, SY-01, DA-01–07 | 4 | 5 | **20** | Critical |
| R-05 | Loss or theft of a staff laptop | PH-01, DA-01, DA-03 | 3 | 4 | **12** | High |
| R-06 | Insecure handling of student/customer data | DA-01, DA-02, DA-03 | 3 | 4 | **12** | High |
| R-07 | Payment-related security risk | DA-04, SY-03 | 2 | 5 | **10** | High |
| R-08 | Lack of an incident response process | All assets | 4 | 4 | **16** | High |
| R-09 | Untested / unreliable backups | DA-01–07, SY-01 | 3 | 4 | **12** | High |
| R-10 | Unauthorised access to online lessons | SY-04, DA-03, PE-03 | 3 | 3 | **9** | Medium |

---

## 3. Detailed risk entries

### R-01 — Phishing attack against staff
| Field | Detail |
|-------|--------|
| **Asset affected** | Email (DA-06), Microsoft 365 (SY-01), staff (PE-01–03) |
| **Threat** | External attacker sending phishing / business email compromise (BEC) emails (T-01) |
| **Vulnerability** | No security awareness training; basic email filtering; no MFA to limit the impact of stolen credentials |
| **Likelihood** | 4 — Likely (phishing is the most common attack on SMEs) |
| **Impact** | 4 — Major (credential theft, fraud, or a reportable data breach) |
| **Risk score** | **16 — High** |
| **Recommended controls** | Enforce MFA on all accounts; enable Microsoft Defender for Office 365 anti-phishing; deliver security awareness training; run simulated phishing; configure SPF/DKIM/DMARC |
| **Control type** | Technical + Procedural |

### R-02 — Weak Microsoft 365 account security
| Field | Detail |
|-------|--------|
| **Asset affected** | Microsoft 365 tenant (SY-01); student & parent data within it (DA-01, DA-02) |
| **Threat** | Account takeover via credential stuffing / password reuse (T-02) |
| **Vulnerability** | MFA not enforced; no Conditional Access; weak/reused passwords; legacy authentication enabled; global admin used for daily work |
| **Likelihood** | 4 — Likely |
| **Impact** | 5 — Catastrophic (full access to children's data and email; potential large UK GDPR breach) |
| **Risk score** | **20 — Critical** |
| **Recommended controls** | Enforce MFA for all users; Conditional Access policies; disable legacy auth; separate admin accounts; enforce strong password policy; enable unified audit log |
| **Control type** | Technical + Procedural |

### R-03 — WordPress website compromise
| Field | Detail |
|-------|--------|
| **Asset affected** | WordPress website (SY-02); data captured via enquiry forms (DA-01, DA-02) |
| **Threat** | Web attackers/bots exploiting vulnerable plugins, themes, or weak admin credentials (T-03) |
| **Vulnerability** | Irregular updates; no MFA on WordPress admin; no web application firewall (WAF); shared hosting |
| **Likelihood** | 4 — Likely (WordPress is continuously scanned by bots) |
| **Impact** | 3 — Moderate (defacement, downtime, malware/skimming, possible data exposure) |
| **Risk score** | **12 — High** |
| **Recommended controls** | Automatic plugin/theme/core updates; remove unused plugins; strong admin credentials + MFA; WAF/security plugin; regular off-site backups; vulnerability monitoring |
| **Control type** | Technical + Procedural |

### R-04 — Ransomware infection
| Field | Detail |
|-------|--------|
| **Asset affected** | Laptops (SY-05), Microsoft 365 (SY-01), all data (DA-01–07) |
| **Threat** | Ransomware delivered via phishing or malicious download (T-04) |
| **Vulnerability** | No endpoint detection & response (EDR); unpatched devices; no MFA; untested backups |
| **Likelihood** | 4 — Likely |
| **Impact** | 5 — Catastrophic (business unable to operate; data loss; potential breach) |
| **Risk score** | **20 — Critical** |
| **Recommended controls** | Deploy Microsoft Defender / EDR; enforce OS and application patching; tested 3-2-1 backups; MFA; least-privilege accounts; user awareness training |
| **Control type** | Technical + Procedural |

### R-05 — Loss or theft of a staff laptop
| Field | Detail |
|-------|--------|
| **Asset affected** | Laptops (PH-01); student data and recordings stored locally (DA-01, DA-03) |
| **Threat** | Physical theft or accidental loss of a device (T-05) |
| **Vulnerability** | No full-disk encryption; no device management/remote wipe; sensitive data stored locally; BYOD with no baseline |
| **Likelihood** | 3 — Possible |
| **Impact** | 4 — Major (reportable UK GDPR breach involving children's data) |
| **Risk score** | **12 — High** |
| **Recommended controls** | Enforce BitLocker full-disk encryption; Microsoft Intune for management and remote wipe; automatic screen lock; store data in the cloud rather than locally; physical care/lock when travelling |
| **Control type** | Technical + Physical + Procedural |

### R-06 — Insecure handling of student/customer data
| Field | Detail |
|-------|--------|
| **Asset affected** | Student data (DA-01), parent data (DA-02), lesson recordings (DA-03) |
| **Threat** | Accidental disclosure, oversharing, or improper access (T-06) |
| **Vulnerability** | No data classification; no access controls / least privilege; "anyone with the link" sharing; no retention policy; no staff data-handling guidance |
| **Likelihood** | 3 — Possible |
| **Impact** | 4 — Major (UK GDPR breach involving minors; reputational damage) |
| **Risk score** | **12 — High** |
| **Recommended controls** | Data classification & handling policy; least-privilege access; restrict external sharing in M365; data retention & deletion schedule; UK GDPR/safeguarding training; record of processing activities (ROPA) |
| **Control type** | Procedural + Technical |

### R-07 — Payment-related security risk
| Field | Detail |
|-------|--------|
| **Asset affected** | Payment data (DA-04); payment service (SY-03) |
| **Threat** | Payment fraud, card-data interception, or skimming (T-07) |
| **Vulnerability** | Risk of storing card data improperly; reliance on website security; no PCI DSS self-assessment; potential script injection on the checkout page |
| **Likelihood** | 2 — Unlikely (Stripe hosted checkout removes most exposure) |
| **Impact** | 5 — Catastrophic (financial loss, PCI penalties, loss of trust) |
| **Risk score** | **10 — High** |
| **Recommended controls** | Use Stripe hosted checkout so card data never touches BrightPath systems; never store card details; enforce HTTPS/TLS; complete PCI DSS SAQ-A; keep checkout integration patched; monitor for fraud |
| **Control type** | Technical + Procedural |

### R-08 — Lack of an incident response process
| Field | Detail |
|-------|--------|
| **Asset affected** | Whole organisation / all assets |
| **Threat** | Slow or ineffective response amplifies the impact of any incident (T-01–T-10) |
| **Vulnerability** | No documented incident response plan; no defined roles; no awareness of the ICO 72-hour breach reporting duty; no logging/monitoring |
| **Likelihood** | 4 — Likely (an incident of some kind is highly probable) |
| **Impact** | 4 — Major (a mishandled breach increases regulatory and reputational harm) |
| **Risk score** | **16 — High** |
| **Recommended controls** | Documented incident response plan with roles and contacts; breach notification procedure (ICO within 72 hours); enable and review audit logs; cyber insurance; annual tabletop exercise |
| **Control type** | Procedural |

### R-09 — Untested / unreliable backups
| Field | Detail |
|-------|--------|
| **Asset affected** | All data (DA-01–07); Microsoft 365 (SY-01) |
| **Threat** | Data loss from ransomware, accidental deletion, or system failure (T-10) |
| **Vulnerability** | Reliance on default M365 retention only; backups never tested by a restore; no independent off-site copy |
| **Likelihood** | 3 — Possible |
| **Impact** | 4 — Major (permanent loss of student records and business data) |
| **Risk score** | **12 — High** |
| **Recommended controls** | Implement a 3-2-1 backup strategy including a third-party M365 backup; schedule and document regular restore tests; protect backups from deletion (immutability) |
| **Control type** | Technical + Procedural |

### R-10 — Unauthorised access to online lessons
| Field | Detail |
|-------|--------|
| **Asset affected** | Video platform (SY-04); lesson recordings (DA-03); tutors and students (PE-03) |
| **Threat** | Disruptive individuals joining lessons ("Zoom-bombing"); a safeguarding concern with minors (T-08) |
| **Vulnerability** | Meeting links reused/shared publicly; no waiting room or passcodes; recordings shared insecurely |
| **Likelihood** | 3 — Possible |
| **Impact** | 3 — Moderate (safeguarding incident, reputational harm) |
| **Risk score** | **9 — Medium** |
| **Recommended controls** | Unique links + passcodes per lesson; enable waiting rooms and host controls; restrict who can share screens; secure storage and controlled sharing of recordings; safeguarding policy |
| **Control type** | Technical + Procedural |

---

## 4. Risk profile summary

| Risk level | Count | Risk IDs |
|-----------|:-----:|----------|
| Critical | 2 | R-02, R-04 |
| High | 7 | R-01, R-03, R-05, R-06, R-07, R-08, R-09 |
| Medium | 1 | R-10 |
| Low | 0 | — |
| **Total** | **10** | |

All risks are recorded with a treatment decision of **Treat (Mitigate)**, except the payment risk (R-07), which is partially **Transferred** to a PCI-compliant processor. See the [control recommendations](./control-recommendations.md).

---

## 5. Review

| Review date | Reviewer | Changes |
|------------|---------|---------|
| 2026-06-01 | Justin Dzanjalimodzi | Initial version |
