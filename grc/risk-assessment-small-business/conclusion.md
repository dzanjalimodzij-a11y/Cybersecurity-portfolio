# Conclusion

**Document Reference:** GRC-RA-CO-001
**Version:** 1.0
**Date:** 2026-06-01

This conclusion summarises the main risk themes, residual risk position, and practical next steps for BrightPath Tutoring Ltd.

---

## 1. Summary of findings

This assessment evaluated the cyber risk facing BrightPath Tutoring Ltd, a small UK online tutoring business that processes children's personal data, takes online payments, and depends on a small set of cloud services and a WordPress website, with no dedicated IT or security staff.

Ten risks were identified and scored. The risk profile is:

| Risk level | Count |
|-----------|:-----:|
| Critical | 2 |
| High | 7 |
| Medium | 1 |
| Low | 0 |

The two **critical** risks — weak Microsoft 365 account security (R-02) and ransomware (R-04) — together represent the most likely route to a serious, reportable breach of children's data.

---

## 2. Key conclusions

1. **The biggest risks are also the cheapest to fix.** Enforcing MFA, separating admin accounts, enabling endpoint protection, and testing backups would meaningfully reduce the two critical risks using tools BrightPath already licenses.
2. **People and process are as important as technology.** Phishing (R-01), insecure data handling (R-06), and the absence of an incident response process (R-08) all stem from missing procedures and awareness rather than missing products.
3. **Regulatory exposure is high.** Because BrightPath processes children's data, even a modest breach could trigger UK GDPR obligations, ICO involvement, and reputational damage with parents.
4. **The control set is balanced.** Mapping to the [NIST CSF](./nist-csf-mapping.md) confirms strong coverage in IDENTIFY and PROTECT, with DETECT and RESPOND as the next maturity step.

---

## 3. Expected residual risk

If the Priority 1 and Priority 2 controls in the [control recommendations](./control-recommendations.md) are implemented and operating effectively, the expected outcome is:

| Risk | Inherent score | Expected residual | Expected level |
|------|:--------------:|:-----------------:|----------------|
| R-02 Weak M365 security | 20 | ~6 | Medium |
| R-04 Ransomware | 20 | ~8 | Medium |
| R-01 Phishing | 16 | ~8 | Medium |
| R-08 No incident response | 16 | ~6 | Medium |
| Other High risks (R-03, R-05, R-06, R-07, R-09) | 10–12 | ~4–6 | Low–Medium |

No residual risk is expected to remain Critical, and most would fall to Low or Medium. Residual risk would be re-scored after implementation.

---

## 4. Recommended next steps

1. **Approve and assign.** Directors approve the risk register and assign an owner and date to each Priority 1 action.
2. **Fix the critical risks within 30 days** (MFA, admin hardening, EDR, tested backups).
3. **Complete Priority 2 within 90 days** (WordPress hardening, encryption, data handling, incident response, payment confirmation).
4. **Embed ongoing practices** — awareness training, simulated phishing, and periodic access reviews.
5. **Consider a formal baseline.** Once foundational controls are in place, BrightPath should pursue **Cyber Essentials** certification as an affordable, recognised mark of assurance, with **ISO/IEC 27001** as a longer-term option if larger contracts require it.
6. **Re-assess in six months** to confirm risks have reduced and to update the register.

---

## 5. Closing statement

BrightPath Tutoring Ltd currently carries significant cyber risk, driven mainly by missing foundational controls rather than by anything unusual about the business. With a focused, low-cost programme of work, the organisation can move from a high-risk posture to a well-managed one within a single quarter — protecting its students, its customers, and its reputation.
