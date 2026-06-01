# OWASP Juice Shop — Web Application Security Assessment

## 1. Project Overview

This project documents a structured penetration test against OWASP Juice Shop, a deliberately vulnerable web application maintained by the OWASP Foundation specifically for security training and education. The assessment follows a professional penetration testing methodology and produces outputs consistent with a real client engagement.

OWASP Juice Shop is an open-source project available at: https://owasp.org/www-project-juice-shop/

---

## 2. Scenario

A simulated client ("Juice Shop Ltd") has commissioned a web application security assessment of their e-commerce platform prior to a planned public launch. The scope covers the web application and its API. The goal is to identify security vulnerabilities, assess their potential business impact, and provide prioritised remediation advice.

---

## 3. Objectives

- Identify vulnerabilities across the OWASP Top 10 categories
- Test authentication, authorisation, and session management controls
- Assess input validation and injection vulnerability exposure
- Identify sensitive data exposure risks
- Document all findings with clear evidence and severity ratings
- Produce a professional penetration test report

---

## 4. Tools Used

| Tool | Purpose |
|------|---------|
| Burp Suite Community/Pro | Web proxy, request interception, scanning |
| OWASP ZAP | Supplementary automated scanning |
| Firefox DevTools | Manual browser-based testing |
| curl / httpie | API endpoint testing |
| JWT.io | JSON Web Token analysis |
| CyberChef | Encoding/decoding analysis |

*[Update with specific tools used in your assessment]*

---

## 5. Methodology

This assessment followed the OWASP Testing Guide (OTG) methodology:

1. **Reconnaissance** — Identify application structure, technologies, and entry points
2. **Authentication Testing** — Test login mechanisms, password policies, account lockout
3. **Authorisation Testing** — Test access controls, horizontal and vertical privilege escalation
4. **Input Validation** — Test for injection vulnerabilities (SQL, XSS, command injection)
5. **Session Management** — Analyse session token generation, expiry, and fixation risks
6. **API Testing** — Enumerate and test API endpoints
7. **Sensitive Data Exposure** — Identify unprotected sensitive data in responses, comments, or storage
8. **Reporting** — Document all findings and produce final report

See [methodology.md](./methodology.md) for detailed methodology notes.

---

## 6. Evidence / Screenshots

> 📁 Screenshots stored in [`screenshots/`](./screenshots/)  
> 📁 Findings documented in [`findings/`](./findings/)

| Screenshot | Description |
|-----------|-------------|
| `[PLACEHOLDER]` | Burp Suite interception setup |
| `[PLACEHOLDER]` | SQL injection finding — proof of concept |
| `[PLACEHOLDER]` | Broken access control — accessing admin panel |
| `[PLACEHOLDER]` | Sensitive data in API response |

---

## 7. Key Findings

> ⚠️ *To be completed on project conclusion. Findings will be documented individually in the `findings/` folder.*

**Finding severity summary (placeholder):**

| Severity | Count |
|----------|-------|
| Critical | [X] |
| High | [X] |
| Medium | [X] |
| Low | [X] |
| Informational | [X] |

---

## 8. Lessons Learned

> *To be completed on project conclusion.*

---

## 9. Employer Relevance

This project demonstrates practical web application penetration testing skills relevant to:
- Junior Penetration Tester / Security Consultant roles
- Application Security Engineer positions
- SOC Analyst roles requiring web threat understanding

Specific transferable skills include professional finding documentation, severity rating methodology, and client-ready report writing.

---

## 10. Status

🔄 **In Progress**
