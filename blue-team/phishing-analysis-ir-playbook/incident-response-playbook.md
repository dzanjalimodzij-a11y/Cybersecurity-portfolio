# Incident Response Playbook — Phishing Email

**Document Reference:** IR-PB-001  
**Version:** 1.0  
**Last Reviewed:** [PLACEHOLDER — Date]  
**Owner:** [PLACEHOLDER — Security Team / SOC]  
**Classification:** Internal Use

---

## Purpose

This playbook provides a structured, repeatable process for responding to phishing email incidents. It is intended for use by security analysts, SOC staff, and IT administrators. Following this playbook ensures a consistent, evidence-based response that minimises risk and supports post-incident review.

---

## Scope

This playbook applies to:
- Phishing emails reported by users
- Phishing emails detected by email security tooling
- Suspected business email compromise (BEC) incidents

---

## Severity Classification

| Severity | Criteria |
|----------|---------|
| **Critical** | User clicked link and submitted credentials / Malware executed on endpoint |
| **High** | User clicked link but no credential submission / Attachment opened |
| **Medium** | Email received and reported; no user interaction with malicious content |
| **Low** | Suspicious email identified by gateway; not delivered to user |

---

## Phase 1: Detection and Reporting

**Trigger:** User report, email gateway alert, or SIEM detection rule

**Steps:**

1. Receive phishing report via [ticketing system / email / hotline]
2. Log incident in the ticketing system with initial details:
   - Reporting user name and department
   - Date/time email was received
   - Whether user interacted with email (clicked link, opened attachment, submitted credentials)
3. Assign severity based on the classification table above
4. Assign to analyst for triage

**Decision point:** If user has already submitted credentials or executed an attachment → escalate immediately to **Phase 3** (Containment)

---

## Phase 2: Triage and Analysis

**Objective:** Confirm the email is malicious and understand its nature and scope.

**Steps:**

1. Obtain a copy of the suspicious email (full .eml with headers)
2. **Do not** click any links or open attachments on a production machine
3. Perform header analysis:
   - Check SPF, DKIM, DMARC results
   - Trace email relay path
   - Identify sending IP and originating domain
4. Analyse email content:
   - Social engineering techniques used
   - Urgency, authority, or fear-based lures
   - Sender spoofing indicators
5. Investigate any URLs:
   - Extract URLs from email body
   - Check in VirusTotal, URLScan.io
   - Review destination page (in sandbox if needed)
6. Investigate any attachments:
   - Record file hash (MD5, SHA256)
   - Submit to sandbox (Any.run, Joe Sandbox)
   - Review sandbox report for malicious behaviours
7. Determine scope:
   - Was this email delivered to other users?
   - Search email gateway logs for same sender/subject/URL
   - Identify all affected recipients
8. Document all findings and IOCs in the investigation record

---

## Phase 3: Containment

**Objective:** Prevent further harm by blocking the threat and isolating affected systems.

**Steps:**

1. **Email containment:**
   - Remove phishing email from all user inboxes (email admin action)
   - Block sending domain and IP at email gateway
   - Block malicious URLs at proxy/web filter

2. **Endpoint containment (if malware executed):**
   - Isolate affected endpoint from the network
   - Preserve volatile memory and disk image if possible
   - Engage endpoint response process

3. **Account containment (if credentials submitted):**
   - Force password reset for affected user immediately
   - Revoke active sessions / tokens
   - Enable MFA if not already active
   - Check for suspicious login activity in the past 72 hours

4. **Notify affected users** with clear, calm guidance on what happened and what they should do

---

## Phase 4: Eradication

**Objective:** Remove all traces of the threat from the environment.

**Steps:**

1. Confirm all copies of phishing email removed from mail system
2. Confirm malicious URLs and domains blocked across all gateway tools
3. If malware was executed: conduct full malware removal and system reimaging if required
4. Verify no persistence mechanisms were established on affected endpoints
5. Review email filtering rules and update as needed

---

## Phase 5: Recovery

**Objective:** Restore normal operations safely.

**Steps:**

1. Reconnect any isolated endpoints after confirmed clean
2. Confirm user can access systems with new credentials
3. Verify MFA is active on affected accounts
4. Monitor affected accounts and endpoints for 72 hours post-recovery

---

## Phase 6: Post-Incident Review

**Objective:** Learn from the incident and improve defences.

**Steps:**

1. Complete incident report within [5 business days] of closure
2. Conduct lessons learned review with relevant stakeholders
3. Identify and implement improvements to:
   - Email filtering rules
   - User awareness training
   - Detection capabilities
   - This playbook (update version and date)
4. Brief users/department as appropriate

---

## Communication Templates

### User Notification (Initial)

> Subject: Action Required — Suspicious Email Alert
>
> Dear [Name],
>
> Our security team has identified a suspicious email that may have been delivered to your inbox. We are currently investigating.
>
> **Please do not click any links or open attachments** from [description of email].
>
> If you have already clicked a link or opened an attachment, please contact [IT Security contact] immediately.
>
> We will update you shortly. Thank you for your cooperation.
>
> [Security Team]

---

## Escalation Contacts

| Role | Contact | When to Escalate |
|------|---------|-----------------|
| Security Lead | [PLACEHOLDER] | Critical severity incidents |
| IT Management | [PLACEHOLDER] | Credential compromise / data breach suspected |
| Legal/Compliance | [PLACEHOLDER] | Potential data breach with regulatory implications |
| [CISO / DPO] | [PLACEHOLDER] | Executive notification required |

---

## Playbook Review Log

| Version | Date | Changes | Reviewed By |
|---------|------|---------|------------|
| 1.0 | [PLACEHOLDER] | Initial version | [Your name] |
