# Threat Register — BrightPath Tutoring Ltd

**Document Reference:** GRC-RA-TR-001
**Version:** 1.0
**Date:** 2026-06-01
**Methodology:** Threat actor analysis + STRIDE
**Classification:** Internal — Confidential

The threats below reflect common issues faced by small online education providers.

---

## 1. Purpose

This threat register identifies the credible threats facing BrightPath Tutoring Ltd's [assets](./asset-register.md). It combines a **threat actor analysis** (who would attack and why) with a **STRIDE** breakdown (what kinds of threats apply) to feed the [risk register](./risk-register.md).

---

## 2. Threat actors

| Threat actor | Motivation | Capability | Relevance to BrightPath |
|--------------|-----------|-----------|-------------------------|
| Opportunistic cybercriminals | Financial gain — ransomware, fraud, automated attacks | Low–Medium (off-the-shelf tools, phishing kits) | **High** — SMEs are prime automated targets |
| Targeted fraudsters (BEC) | Trick staff into transferring money or data | Medium | **Medium–High** — small finance teams are vulnerable |
| Web attackers / bots | Compromise the WordPress site, deface, host malware, harvest data | Low–Medium (automated vulnerability scanners) | **High** — WordPress is constantly scanned |
| Malicious insider | Grievance, personal gain | Low | Low–Medium |
| Accidental insider (human error) | None (unintentional) | N/A | **High** — most common cause of breaches |
| Disruptive individuals | Harassment / "Zoom-bombing" of lessons | Low | Medium — safeguarding concern with minors |

---

## 3. Threat register

| Threat ID | Threat | Source | Assets affected | Relevance |
|-----------|--------|--------|-----------------|-----------|
| T-01 | Phishing / business email compromise | External attacker | DA-01, DA-02, DA-06, PE-01–03 | High |
| T-02 | Credential theft / account takeover | External attacker | SY-01, DA-01, DA-02 | High |
| T-03 | WordPress exploitation (plugin/theme/CMS vulnerabilities) | Web attacker / bots | SY-02, DA-01, DA-02 | High |
| T-04 | Ransomware / malware infection | Cybercriminals | SY-05, SY-01, DA-01–07 | High |
| T-05 | Loss or theft of a device | Physical theft / loss | PH-01, DA-01, DA-03 | Medium–High |
| T-06 | Accidental data disclosure / misconfiguration | Human error | DA-01, DA-02, DA-03 | High |
| T-07 | Payment fraud / interception | Fraudsters | DA-04, SY-03 | Medium |
| T-08 | Unauthorised access to live lessons | Disruptive individuals | SY-04, DA-03, PE-03 | Medium |
| T-09 | Supplier/third-party breach | Third-party compromise | SY-01, SY-03, SY-04 | Medium |
| T-10 | Backup failure / data loss | System failure / human error | DA-01–07 | Medium–High |

---

## 4. STRIDE analysis

STRIDE is used to confirm coverage across the six standard threat categories.

### S — Spoofing
| Threat | Target | Example |
|--------|--------|---------|
| Phishing / impersonation | Staff inboxes | Attacker impersonates a director requesting an urgent payment or data export |
| Credential stuffing | Microsoft 365 accounts | Reused/leaked passwords tried against company logins (no MFA) |

### T — Tampering
| Threat | Target | Example |
|--------|--------|---------|
| Website defacement / injection | WordPress site | Attacker exploits an outdated plugin to inject malicious code or skimming scripts |
| Ransomware encryption | Laptops, OneDrive | Files encrypted and held to ransom |

### R — Repudiation
| Threat | Target | Example |
|--------|--------|---------|
| Insufficient logging | M365 / WordPress | Account misuse cannot be traced because audit logging is not reviewed |

### I — Information Disclosure
| Threat | Target | Example |
|--------|--------|---------|
| Accidental disclosure | Student data | Spreadsheet of students emailed to the wrong parent |
| Oversharing | OneDrive/SharePoint | Lesson recordings shared via an open "anyone with the link" URL |
| Device theft | Unencrypted laptop | Stolen laptop exposes student records |

### D — Denial of Service
| Threat | Target | Example |
|--------|--------|---------|
| Ransomware outage | Business systems | Operations halt because data is inaccessible |
| Website downtime | WordPress site | Site offline during peak enrolment, losing bookings |

### E — Elevation of Privilege
| Threat | Target | Example |
|--------|--------|---------|
| Admin account compromise | M365 Global Admin | Phished director account gives attacker tenant-wide control |
| WordPress admin takeover | Website backend | Weak admin credentials allow full site control |

---

## 5. Review

| Review date | Reviewer | Changes |
|------------|---------|---------|
| 2026-06-01 | Justin Dzanjalimodzi | Initial version |
