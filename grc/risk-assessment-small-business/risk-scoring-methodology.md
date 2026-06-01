# Risk Scoring Methodology

**Document Reference:** GRC-RA-MS-001
**Version:** 1.0
**Date:** 2026-06-01
**Aligned to:** NIST SP 800-30, ISO/IEC 27005

---

## 1. Purpose

This document defines the method used to assess and rate risks in this assessment. Using a documented, repeatable methodology ensures that risk scores are **consistent, comparable, and defensible** rather than subjective. Every risk in the [risk register](./risk-register.md) is scored using the scales below.

---

## 2. Risk scoring formula

Each risk is scored on two dimensions — **likelihood** and **impact** — each rated on a scale of **1 to 5**. The overall risk score is the product of the two:

```
Risk Score = Likelihood (1–5) × Impact (1–5)
```

This produces a score between **1 and 25**, plotted on a 5×5 risk matrix.

---

## 3. Likelihood scale (1–5)

How likely the risk is to occur within a 12-month period, given the current control environment.

| Score | Rating | Description |
|-------|--------|-------------|
| 1 | Rare | Very unlikely to occur; no known precedent for a business of this type |
| 2 | Unlikely | Could occur but not expected; limited precedent |
| 3 | Possible | May occur; happens periodically to similar businesses |
| 4 | Likely | Probably will occur; common across the sector |
| 5 | Almost Certain | Expected to occur, potentially more than once |

---

## 4. Impact scale (1–5)

The severity of the consequences if the risk materialises, considering financial, operational, regulatory, and reputational effects.

| Score | Rating | Description |
|-------|--------|-------------|
| 1 | Negligible | Minimal disruption; no regulatory or financial consequence |
| 2 | Minor | Limited, short-lived disruption; absorbed internally |
| 3 | Moderate | Noticeable disruption; some cost; possible minor regulatory exposure |
| 4 | Major | Serious disruption; likely reportable data breach; reputational harm; significant cost |
| 5 | Catastrophic | Business-threatening; severe regulatory penalty, major financial loss, or loss of customer trust |

---

## 5. Risk-level bands

The risk score maps to a risk level that drives prioritisation and treatment urgency:

| Risk Score | Risk Level | Meaning |
|------------|-----------|---------|
| **1–4** | 🟢 **Low** | Acceptable; monitor. No immediate action required. |
| **5–9** | 🟡 **Medium** | Address within a reasonable timeframe; keep under review. |
| **10–16** | 🟠 **High** | Significant; prioritise treatment in the near term. |
| **17–25** | 🔴 **Critical** | Unacceptable; requires urgent action. |

---

## 6. 5×5 risk matrix

The matrix below shows the risk score (Likelihood × Impact) and the colour band for every combination.

| Likelihood ↓ / Impact → | 1 (Negligible) | 2 (Minor) | 3 (Moderate) | 4 (Major) | 5 (Catastrophic) |
|---|---|---|---|---|---|
| **5 (Almost Certain)** | 5 🟡 | 10 🟠 | 15 🟠 | 20 🔴 | 25 🔴 |
| **4 (Likely)** | 4 🟢 | 8 🟡 | 12 🟠 | 16 🟠 | 20 🔴 |
| **3 (Possible)** | 3 🟢 | 6 🟡 | 9 🟡 | 12 🟠 | 15 🟠 |
| **2 (Unlikely)** | 2 🟢 | 4 🟢 | 6 🟡 | 8 🟡 | 10 🟠 |
| **1 (Rare)** | 1 🟢 | 2 🟢 | 3 🟢 | 4 🟢 | 5 🟡 |

🟢 Low (1–4)  🟡 Medium (5–9)  🟠 High (10–16)  🔴 Critical (17–25)

---

## 7. Risk treatment options

Once a risk is scored, a treatment decision is recorded. This assessment uses the standard four options:

| Option | Description |
|--------|-------------|
| **Treat (Mitigate)** | Implement controls to reduce likelihood and/or impact |
| **Tolerate (Accept)** | Accept the risk as within appetite; monitor it |
| **Transfer (Share)** | Shift some risk to a third party (e.g., insurance, a compliant payment processor) |
| **Terminate (Avoid)** | Stop the activity that creates the risk |

---

## 8. Control types

Each recommended control is categorised by type, to ensure a balanced defence rather than over-reliance on technology alone:

| Control Type | Description | Examples |
|--------------|-------------|----------|
| **Technical** | Implemented in or by technology | MFA, encryption, EDR, email filtering, backups |
| **Procedural** (administrative) | Policies, processes, and people | Awareness training, incident response plan, access reviews |
| **Physical** | Protects physical assets and environments | Laptop locks, device storage, screen privacy |

---

## 9. Inherent vs residual risk

- **Inherent risk** is the risk score *before* recommended controls are applied (the current "before" state described in the [company profile](./company-profile-and-scope.md)).
- **Residual risk** is the expected risk score *after* the recommended controls are implemented and operating effectively.

The [risk register](./risk-register.md) records inherent scores; expected residual outcomes are discussed in the [conclusion](./conclusion.md).
