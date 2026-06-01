# Indicators of Compromise (IOCs) — Phishing Analysis

This document consolidates all IOCs extracted from simulated phishing email samples analysed during this project. These indicators can be used to create SIEM detection rules, email gateway blocklists, and DNS sinkholes in a real environment.

> **Note:** All IOCs below are from simulated or intentionally fictional samples created for lab purposes. They do not represent real threats.

---

## IOC Summary Table

| Type | Indicator | Confidence | Sample Reference | Notes |
|------|-----------|-----------|-----------------|-------|
| Email Address | `[PLACEHOLDER]` | High | Sample-01 | Spoofed sender |
| Domain | `[PLACEHOLDER]` | High | Sample-01 | Phishing domain |
| IP Address | `[PLACEHOLDER]` | Medium | Sample-02 | Email relay |
| URL | `[PLACEHOLDER]` | High | Sample-02 | Credential harvesting page |
| File Hash (MD5) | `[PLACEHOLDER]` | High | Sample-03 | Malicious attachment |
| File Hash (SHA256) | `[PLACEHOLDER]` | High | Sample-03 | Malicious attachment |
| File Name | `[PLACEHOLDER]` | Medium | Sample-03 | Attachment filename |
| Subject Line Pattern | `[PLACEHOLDER]` | Medium | Multiple | Common lure pattern |

---

## Detailed IOC Entries

### Sample-01 — Credential Harvesting Lure

**Email Metadata:**
- Sender (Display Name): `[PLACEHOLDER]`
- Sender (Actual): `[PLACEHOLDER]`
- Subject: `[PLACEHOLDER]`
- Date/Time: `[PLACEHOLDER]`
- Message-ID: `[PLACEHOLDER]`

**Authentication Results:**
- SPF: `[PASS / FAIL / SOFTFAIL]`
- DKIM: `[PASS / FAIL / NONE]`
- DMARC: `[PASS / FAIL / NONE]`

**Indicators:**
- Sending IP: `[PLACEHOLDER]`
- Phishing URL: `[PLACEHOLDER]`
- Redirect chain: `[PLACEHOLDER]`

---

### Sample-02 — Malicious Attachment

**Email Metadata:**
- Sender: `[PLACEHOLDER]`
- Subject: `[PLACEHOLDER]`
- Attachment Name: `[PLACEHOLDER]`
- Attachment Type: `[PLACEHOLDER — e.g., .docm / .xlsx / .pdf]`

**File Indicators:**
- MD5: `[PLACEHOLDER]`
- SHA1: `[PLACEHOLDER]`
- SHA256: `[PLACEHOLDER]`
- File Size: `[PLACEHOLDER]`

**Sandbox Analysis Summary:**
- Sandbox used: `[PLACEHOLDER]`
- Verdict: `[PLACEHOLDER]`
- Behaviours observed: `[PLACEHOLDER]`

---

### Sample-03 — [PLACEHOLDER — Add additional samples]

> *[PLACEHOLDER — Repeat above structure for each sample analysed]*

---

## Recommended Defensive Actions

Based on the IOCs identified, the following defensive measures are recommended for a real environment:

1. **Email Gateway** — Block sending domains and IPs identified above
2. **DNS Filtering** — Block phishing domains at DNS resolver level
3. **SIEM Rules** — Create detection rules for subject line patterns and known-bad sender addresses
4. **File Blocklist** — Add file hashes to EDR/AV blocklist
5. **User Alert** — Notify users to be vigilant for emails matching this pattern

---

## IOC Sharing Format (STIX/MISP)

> *[PLACEHOLDER — If you export IOCs in a structured format such as STIX 2.1 or MISP event, add the export file reference here]*
