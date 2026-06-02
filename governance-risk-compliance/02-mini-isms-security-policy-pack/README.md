# Mini ISMS / Security Policy Pack for a Small Company

> **Project category:** Governance, Risk & Compliance (GRC) / Security Governance
> **Scenario:** BrightBox Retail Ltd - small UK online retail business
> **Reference influences:** ISO 27001-style ISMS structure, NIST CSF 2.0 governance concepts, NCSC small business guidance

This is a simulated portfolio project using BrightBox Retail Ltd as the case study. The company, policy pack, registers, risks, and evidence examples are illustrative and are not a certified ISMS or a claim of ISO 27001 certification.

---

## 1. Project overview

This project creates a small, practical information security management system (ISMS) structure for BrightBox Retail Ltd. The aim is to show how a basic set of governance documents, security policies, registers, and review processes could be organised for a small company with limited internal security resource.

The work focuses on sensible controls for a 15-person online retail business using Microsoft 365, Shopify, cloud file storage, Windows laptops, shared business email accounts, and a small office network.

---

## 2. Skills demonstrated

| Skill | Where it appears |
|-------|------------------|
| ISMS scoping | [02-isms-scope.md](./docs/02-isms-scope.md) |
| Governance design | [03-governance-structure.md](./docs/03-governance-structure.md) |
| Policy writing | [policies/](./policies/) |
| Asset and risk awareness | [asset-register.md](./registers/asset-register.md), [risk-register.md](./registers/risk-register.md) |
| Control mapping | [06-control-mapping.md](./docs/06-control-mapping.md) |
| Review and improvement planning | [07-review-and-improvement-plan.md](./docs/07-review-and-improvement-plan.md) |
| Security roles and responsibilities | [roles-and-responsibilities.md](./registers/roles-and-responsibilities.md) |
| Evidence planning | [evidence/README.md](./evidence/README.md) |

---

## 3. Business scenario summary

BrightBox Retail Ltd sells consumer products online. The company has around 15 employees working across management, operations, customer service, finance, fulfilment, and marketing. It relies on cloud services and outsourced IT support rather than a dedicated security team.

Key security concerns include account compromise, phishing, weak access control, inconsistent handling of customer information, laptop loss, supplier dependency, and limited incident response planning.

---

## 4. What an ISMS means here

For this project, an ISMS means a simple management structure for keeping security responsibilities, policies, risks, assets, and reviews organised. It is not treated as a formal certification exercise. The focus is on what a small company could realistically operate and maintain.

---

## 5. What the policy pack includes

| Area | Contents |
|------|----------|
| Context and scope | Company context, ISMS scope, governance structure |
| Policies | Core policies covering acceptable use, access control, MFA, data handling, backups, incidents, suppliers, remote working, and awareness |
| Registers | Asset register, risk register, policy register, roles and responsibilities |
| Control mapping | Simple mapping to ISO 27001-style and NIST CSF-style outcomes |
| Review process | Review triggers, metrics, evidence, and improvement actions |

---

## 6. Methodology

1. Define the business context and technology environment.
2. Set a realistic ISMS scope for a small online retailer.
3. Identify the main assets and risks.
4. Write a short set of usable policies.
5. Assign ownership across business roles.
6. Map the policy pack to practical control outcomes.
7. Define evidence and review activities that the company could maintain.

---

## 7. Folder structure

```text
02-mini-isms-security-policy-pack/
|-- README.md
|-- docs/
|   |-- 01-company-context.md
|   |-- 02-isms-scope.md
|   |-- 03-governance-structure.md
|   |-- 04-policy-framework.md
|   |-- 05-asset-and-risk-overview.md
|   |-- 06-control-mapping.md
|   |-- 07-review-and-improvement-plan.md
|   `-- 08-management-summary.md
|-- policies/
|-- registers/
`-- evidence/
```

---

## 8. Key outputs

### Core documents

- [Company Context](./docs/01-company-context.md)
- [ISMS Scope](./docs/02-isms-scope.md)
- [Governance Structure](./docs/03-governance-structure.md)
- [Policy Framework](./docs/04-policy-framework.md)
- [Asset and Risk Overview](./docs/05-asset-and-risk-overview.md)
- [Control Mapping](./docs/06-control-mapping.md)
- [Review and Improvement Plan](./docs/07-review-and-improvement-plan.md)
- [Management Summary](./docs/08-management-summary.md)
- [Asset Register](./registers/asset-register.md)
- [Risk Register](./registers/risk-register.md)
- [Policy Register](./registers/policy-register.md)
- [Roles and Responsibilities](./registers/roles-and-responsibilities.md)

### Policies

- [Information Security Policy](./policies/information-security-policy.md)
- [Acceptable Use Policy](./policies/acceptable-use-policy.md)
- [Access Control Policy](./policies/access-control-policy.md)
- [Password and MFA Policy](./policies/password-and-mfa-policy.md)
- [Data Classification and Handling Policy](./policies/data-classification-and-handling-policy.md)
- [Backup Policy](./policies/backup-policy.md)
- [Incident Response Policy](./policies/incident-response-policy.md)
- [Supplier Security Policy](./policies/supplier-security-policy.md)
- [Remote Working Policy](./policies/remote-working-policy.md)
- [Security Awareness Policy](./policies/security-awareness-policy.md)
