# Data Classification Policy

**Document Reference:** POL-006  
**Version:** 1.0  
**Effective Date:** [PLACEHOLDER]  
**Review Date:** [PLACEHOLDER]  
**Owner:** Managing Director  
**ISO 27001 Controls:** 5.12, 5.13  
**Classification:** Internal

---

## 1. Purpose

To ensure that company information is classified according to its sensitivity and value, and that appropriate handling controls are applied consistently across the organisation.

## 2. Scope

This policy applies to all information created, received, stored, or processed by Acorn Solutions Ltd, in any format — digital or physical.

## 3. Classification Levels

### CONFIDENTIAL

**Definition:** Information whose unauthorised disclosure could cause serious harm to the business, clients, or individuals. This is the highest classification level.

**Examples:**
- Client personal data (names, financial details, tax records)
- Company financial accounts and forecasts
- Employee salary and HR records
- Passwords, encryption keys, and authentication credentials
- Legal advice and privileged communications

**Handling requirements:**
- Access restricted to specifically authorised individuals only
- Must be encrypted when stored digitally
- Must be transmitted only via encrypted channels
- Must not be shared externally without explicit authorisation
- Physical copies must be stored in locked filing cabinets and shredded when no longer needed
- Must not be discussed in public areas or on public transport

---

### INTERNAL

**Definition:** Information intended for use within the organisation that is not suitable for public release, but whose disclosure would cause limited harm.

**Examples:**
- Internal policies and procedures
- Project plans and meeting notes
- Staff contact directories
- Supplier contracts and pricing

**Handling requirements:**
- Access limited to company staff and authorised third parties
- Must not be shared publicly or posted on unsecured external platforms
- Reasonable care must be taken with physical copies

---

### PUBLIC

**Definition:** Information that has been approved for public release. Disclosure presents no significant risk to the organisation.

**Examples:**
- Company website content
- Published marketing materials
- Public job advertisements

**Handling requirements:**
- No restrictions on distribution
- Must be approved by an appropriate manager before publication

---

## 4. Handling Rules Summary

| Requirement | Confidential | Internal | Public |
|-------------|-------------|---------|--------|
| Encryption at rest | Required | Recommended | Not required |
| Encryption in transit | Required | Required | Not required |
| Access controls | Strictly restricted | Staff and approved third parties | Unrestricted |
| Physical security | Locked storage | Secure handling | Unrestricted |
| Disposal | Secure shredding / secure wipe | Secure shredding / deletion | Standard disposal |
| Sharing externally | Explicit authorisation required | Managerial approval | Freely shareable |

## 5. Classification Responsibilities

- **All staff** are responsible for classifying information they create and handling it according to this policy
- **Managers** are responsible for ensuring their teams understand and apply the classification scheme
- **IT Manager** is responsible for implementing technical controls that support classification (e.g., DLP, access controls)
- When in doubt, classify at a higher level and seek guidance

## 6. Data Retention and Disposal

Information must be retained only as long as there is a legitimate business or legal reason. When information is no longer required:

- **Digital data:** Securely deleted or wiped using approved tools
- **Physical documents:** Cross-cut shredded or placed in confidential waste bins
- **Devices:** Data wiped to NCSC or NIST 800-88 standard before reuse or disposal

Refer to the company's data retention schedule for specific retention periods.

---

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [PLACEHOLDER] | [Your name] | Initial version |
