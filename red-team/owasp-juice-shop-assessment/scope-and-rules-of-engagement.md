# Scope and Rules of Engagement

**Assessment:** OWASP Juice Shop Web Application Security Assessment  
**Document Reference:** ROE-001  
**Version:** 1.0  
**Date:** [PLACEHOLDER]

---

## 1. Authorisation Statement

This assessment was conducted against OWASP Juice Shop — a deliberately vulnerable application provided by the OWASP Foundation for security training purposes. The application is designed to be tested and no additional authorisation beyond this documented agreement is required for educational use.

> *In a real engagement, this section would contain a signed authorisation letter from the client confirming permission to test.*

---

## 2. Scope

### In Scope

| Target | Type | Notes |
|--------|------|-------|
| `http://localhost:3000` | Web Application | Local instance of OWASP Juice Shop |
| Juice Shop REST API | API | Endpoints exposed by the application |
| Client-side JavaScript | Static Analysis | Source code review of frontend assets |

### Out of Scope

- Any systems other than the local Juice Shop instance
- Denial of Service (DoS) testing
- Physical security testing
- Social engineering
- Any production systems, real websites, or third-party infrastructure

---

## 3. Rules of Engagement

The following rules apply throughout this assessment:

1. **Authorised environment only** — Testing is performed exclusively on the local Juice Shop instance running in an isolated environment.
2. **No real data** — No real user data, payment details, or personal information is used or targeted.
3. **No destructive actions** — Findings are demonstrated with minimal impact; no intentional data destruction or service disruption.
4. **Documentation** — All testing activity is logged and documented.
5. **Ethical conduct** — All work is conducted in accordance with ethical standards and applicable law.
6. **No external connections** — The test environment has no connections to external systems or real infrastructure.

---

## 4. Testing Window

| Phase | Start | End |
|-------|-------|-----|
| Setup and Reconnaissance | [PLACEHOLDER] | [PLACEHOLDER] |
| Active Testing | [PLACEHOLDER] | [PLACEHOLDER] |
| Report Writing | [PLACEHOLDER] | [PLACEHOLDER] |

---

## 5. Methodology Reference

This assessment follows the OWASP Web Security Testing Guide (WSTG): https://owasp.org/www-project-web-security-testing-guide/

---

## 6. Reporting

Findings will be documented in:
- Individual finding records in the `findings/` folder
- A consolidated final report: [final-report.md](./final-report.md)

---

## Acknowledgement

> *In a real engagement, this section would contain signatures from both the tester and the client authorising the assessment. For this educational project, this section serves as a record that the tester understands and has agreed to the rules above.*

Tester: [Your name]  
Date: [PLACEHOLDER]
