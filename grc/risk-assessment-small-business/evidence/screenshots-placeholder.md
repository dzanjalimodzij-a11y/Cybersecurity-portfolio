# Evidence

I created the visuals in this section to support the written risk assessment and present the main findings in a clearer format. They cover the risk profile, system context, data flows, NIST CSF control mapping, and an illustrative Secure Score-style example.

BrightPath Tutoring Ltd is introduced as the case organisation in the main project README, and these visuals should be read alongside the written assessment files.

---

## Visual evidence files

| Filename | Description |
|----------|-------------|
| [`risk-matrix.png`](./risk-matrix.png) | 5x5 risk heat map with all 10 risks plotted using the likelihood, impact, and score values from the [risk register](../risk-register.md). |
| [`risk-profile-chart.png`](./risk-profile-chart.png) | Bar chart summarising the risk profile from the risk register: 2 Critical, 7 High, 1 Medium, and 0 Low. |
| [`system-architecture.png`](./system-architecture.png) | High-level diagram of BrightPath's environment, including public users, staff laptops, Microsoft 365, WordPress, Stripe, video platform, and cloud file storage. |
| [`data-flow-diagram.png`](./data-flow-diagram.png) | Data flow diagram showing student, parent/customer, tutor, booking, payment-status, and lesson-access data across public, internal, and third-party trust boundaries. |
| [`nist-csf-coverage.png`](./nist-csf-coverage.png) | Bar chart showing the number of mapped project controls and actions across the six NIST CSF 2.0 functions. |
| [`m365-secure-score.png`](./m365-secure-score.png) | Illustrative Secure Score-style example showing how security posture improvements could be prioritised. |

---

## Notes on use

- The charts are based on the current Project 1 documentation and should be regenerated if risk scores or mappings change.
- The Secure Score-style image is an illustrative example based on the assessment scenario.
