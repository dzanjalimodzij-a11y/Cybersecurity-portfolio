# Methodology — OWASP Juice Shop Assessment

## Overview

This assessment follows the OWASP Web Security Testing Guide (WSTG) v4.2 methodology, supplemented by the PTES (Penetration Testing Execution Standard) for report structure and severity rating.

---

## Phase 1: Reconnaissance and Information Gathering

**Objective:** Understand the application's structure, technology stack, and attack surface before active testing begins.

**Activities:**
- Review application pages and functionality as an unauthenticated user
- Identify technology stack (server, framework, client-side libraries) via HTTP headers, JavaScript, and source code review
- Map all application entry points: forms, URL parameters, API endpoints
- Review JavaScript source files for API routes, comments, and hardcoded values
- Identify user roles present in the application

**Tools:** Browser DevTools, Burp Suite (passive proxy), dirbusting tools

**Notes:**
> [PLACEHOLDER — Record reconnaissance findings here as testing progresses]

---

## Phase 2: Authentication and Session Management

**Objective:** Test the security of login mechanisms and session handling.

**Test cases:**
- Default / weak credentials
- Account lockout policy
- Password reset mechanism security
- Session token entropy and predictability
- Session fixation and hijacking
- JWT token validation (if applicable)
- Multi-factor authentication bypass

**Notes:**
> [PLACEHOLDER]

---

## Phase 3: Authorisation and Access Control

**Objective:** Test whether users can access resources or perform actions beyond their privilege level.

**Test cases:**
- Horizontal privilege escalation (accessing another user's data)
- Vertical privilege escalation (accessing admin functionality as a regular user)
- Insecure Direct Object References (IDOR) on API endpoints
- Forced browsing to restricted pages

**Notes:**
> [PLACEHOLDER]

---

## Phase 4: Input Validation and Injection

**Objective:** Test all user-controllable inputs for injection vulnerabilities.

**Test cases:**
- SQL Injection (error-based, blind, time-based)
- Cross-Site Scripting (reflected, stored, DOM-based)
- Command injection
- XML/JSON injection
- Template injection

**Notes:**
> [PLACEHOLDER]

---

## Phase 5: Sensitive Data Exposure

**Objective:** Identify sensitive data that is inadequately protected.

**Test cases:**
- Sensitive data in HTTP responses (API keys, credentials, PII)
- Sensitive data in JavaScript source files
- Sensitive data in error messages
- Unencrypted transmission of sensitive data
- Inadequate data storage protections

**Notes:**
> [PLACEHOLDER]

---

## Phase 6: API Security

**Objective:** Test the security of REST API endpoints.

**Test cases:**
- API endpoint enumeration
- Unauthenticated access to authenticated endpoints
- Mass assignment vulnerabilities
- Rate limiting
- API versioning exposure

**Notes:**
> [PLACEHOLDER]

---

## Severity Rating Criteria

Findings are rated using a combination of CVSS Base Score and business impact assessment:

| Severity | CVSS Range | Description |
|----------|-----------|-------------|
| Critical | 9.0 – 10.0 | Immediate exploitation risk; severe business impact |
| High | 7.0 – 8.9 | Significant exploitation risk; high business impact |
| Medium | 4.0 – 6.9 | Moderate risk; requires conditions to exploit |
| Low | 0.1 – 3.9 | Limited risk; minimal business impact |
| Informational | N/A | No direct risk; security improvement opportunity |
