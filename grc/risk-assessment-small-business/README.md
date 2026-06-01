# Cyber Risk Assessment — Small UK Online Tutoring Business

> **Project category:** Governance, Risk & Compliance (GRC) / Cyber Risk Management
> **Scenario:** BrightPath Tutoring Ltd — small UK online tutoring business
> **Frameworks used:** NIST SP 800-30, NIST Cybersecurity Framework (CSF) 2.0, ISO/IEC 27001:2022, UK GDPR / Data Protection Act 2018

> ⚠️ *BrightPath Tutoring Ltd is a fictional small UK online tutoring business used for this independent practice assessment. No real organisation is represented.*

---

## 1. What this project is

This project was completed as an independent cybersecurity practice exercise. It is a complete, end-to-end **cyber risk assessment** for **BrightPath Tutoring Ltd** and works through the full risk-management lifecycle used in a practical GRC assessment:

1. Understanding the business and defining the assessment scope
2. Agreeing a repeatable risk-scoring methodology
3. Building an asset register
4. Identifying credible threats (threat register)
5. Analysing and rating risks in a risk register
6. Recommending prioritised, proportionate controls
7. Mapping controls to the **NIST Cybersecurity Framework**
8. Communicating findings to non-technical decision-makers

The business is deliberately small, online-first, and handles **children's personal data**, online payments, and a public WordPress website — a realistic profile for the kind of SME that is heavily targeted but rarely has dedicated security staff.

---

## 2. Why it matters

Small businesses are the most common victims of cyber attacks, yet they are the least likely to have a structured view of their own risk. An online tutoring business is a particularly interesting case study because it combines several high-stakes exposures in one small organisation:

- **Children's personal data**, attracting heightened obligations under UK GDPR and safeguarding expectations.
- **Online payments** from parents, bringing PCI DSS and fraud considerations.
- A **public-facing WordPress site** used for marketing and bookings — a frequent attack target.
- A **remote, cloud-first workforce** using Microsoft 365 and personal/company laptops, with no dedicated IT team.

This project explores how to translate that messy real-world picture into a clear, prioritised, defensible set of recommendations that a non-technical director can act on.

---

## 3. Skills practised

| Skill | Where it appears |
|-------|------------------|
| Business and scope analysis | [company-profile-and-scope.md](./company-profile-and-scope.md) |
| Risk methodology design (5×5 likelihood × impact) | [risk-scoring-methodology.md](./risk-scoring-methodology.md) |
| Asset identification & classification | [asset-register.md](./asset-register.md) |
| Threat identification & threat actor analysis | [threat-register.md](./threat-register.md) |
| Risk analysis, scoring & treatment decisions | [risk-register.md](./risk-register.md) |
| Control selection (technical / procedural / physical) | [control-recommendations.md](./control-recommendations.md) |
| Framework mapping (NIST CSF 2.0) | [nist-csf-mapping.md](./nist-csf-mapping.md) |
| Executive / stakeholder communication | [executive-summary.md](./executive-summary.md) |
| Regulatory awareness (UK GDPR, PCI DSS) | throughout |
| Professional documentation & referencing | [references.md](./references.md) |

---

## 4. Deliverables included

| File | Description |
|------|-------------|
| [executive-summary.md](./executive-summary.md) | One-page, non-technical summary for the directors |
| [company-profile-and-scope.md](./company-profile-and-scope.md) | Business description, environment, assumptions, and assessment scope |
| [risk-scoring-methodology.md](./risk-scoring-methodology.md) | Likelihood/impact scales, scoring formula, and risk-level bands |
| [asset-register.md](./asset-register.md) | Inventory of data, system, people, and physical assets with classifications |
| [threat-register.md](./threat-register.md) | Threats, threat actors, and STRIDE analysis |
| [risk-register.md](./risk-register.md) | 10 scored risks with vulnerabilities, ratings, controls, and control types |
| [control-recommendations.md](./control-recommendations.md) | Prioritised, costed control recommendations |
| [nist-csf-mapping.md](./nist-csf-mapping.md) | Mapping of recommended controls to NIST CSF 2.0 functions |
| [conclusion.md](./conclusion.md) | Overall conclusion, residual risk, and next steps |
| [references.md](./references.md) | Standards, frameworks, and sources used |
| [evidence/screenshots-placeholder.md](./evidence/screenshots-placeholder.md) | Placeholder describing supporting evidence/diagrams |

---

## 5. How to read this project

The suggested reading order is:

1. **Start with the [executive summary](./executive-summary.md)** — this is how the work would land on a decision-maker's desk. It should be readable in two minutes and make the priorities obvious.
2. **Read the [company profile and scope](./company-profile-and-scope.md)** to see how the business context and boundaries were established before any analysis began.
3. **Review the [risk-scoring methodology](./risk-scoring-methodology.md)** to confirm the assessment is repeatable and defensible, not arbitrary.
4. **Work through the [asset register](./asset-register.md) → [threat register](./threat-register.md) → [risk register](./risk-register.md)** to follow the analytical chain from "what do we have" to "what could go wrong" to "how bad is it".
5. **Finish with the [control recommendations](./control-recommendations.md) and [NIST CSF mapping](./nist-csf-mapping.md)** to judge whether the proposed actions are proportionate, prioritised, and tied to a recognised framework.

**What this project focuses on:** practising the process of running a structured risk assessment for a real-world SME, balancing security against cost and practicality, communicating clearly to non-technical stakeholders, and aligning recommendations to recognised standards.

---

## 6. Status

✅ **Documentation complete.** Diagrams and screenshots referenced in `evidence/` are placeholders to be added when supporting visuals are produced.
