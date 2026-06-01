# Password Policy

**Document Reference:** POL-002  
**Version:** 1.0  
**Effective Date:** [PLACEHOLDER]  
**Review Date:** [PLACEHOLDER]  
**Owner:** IT Manager  
**ISO 27001 Controls:** 5.17, 8.5  
**Classification:** Internal

---

## 1. Purpose

To establish requirements for the creation, management, and protection of passwords and authentication credentials used to access company systems, ensuring that credentials provide an appropriate level of protection.

## 2. Scope

This policy applies to all accounts — staff, contractor, service, and administrator — that access company systems, applications, or data.

## 3. Password Requirements

### 3.1 Minimum Standards

| Account Type | Minimum Length | Complexity | MFA Required |
|-------------|---------------|-----------|-------------|
| Standard user account | 12 characters | Yes | Yes |
| Privileged / admin account | 16 characters | Yes | Yes (hardware token preferred) |
| Service account | 20+ characters (randomly generated) | Yes | N/A (managed) |
| Shared account (where unavoidable) | 16 characters | Yes | Documented exception required |

**Complexity requirements:** Passwords must include a mix of uppercase letters, lowercase letters, numbers, and special characters. Alternatively, a passphrase of 4+ random words (minimum 15 characters total) is acceptable.

### 3.2 Password Restrictions

Passwords must NOT:
- Be the same as, or similar to, any of the last 10 passwords used
- Contain the user's name, username, or easily guessable personal information
- Be a dictionary word or common phrase without modification
- Be shared with any other person, including IT support staff
- Be reused across different systems or services

## 4. Password Management

### 4.1 Password Manager

All staff are required to use the company-approved password manager ([PLACEHOLDER — specify tool, e.g., Bitwarden for Teams]) to generate, store, and manage unique passwords for all systems. The password manager master password must comply with the minimum standards above.

### 4.2 Default Passwords

All default passwords on new systems, devices, and accounts must be changed before deployment or first use.

### 4.3 Password Reset

Passwords must be reset immediately if there is any suspicion of compromise. Passwords must not be reset to a recently used password.

### 4.4 Sharing Credentials

Sharing of login credentials is prohibited. Where multiple users require access to a shared resource, a shared account must be formally approved, documented, and managed through the access control process.

## 5. Multi-Factor Authentication (MFA)

MFA is mandatory for:
- All Microsoft 365 accounts (email, Teams, SharePoint)
- All cloud-based systems and SaaS applications
- Any system accessible from outside the corporate network
- All privileged and administrator accounts

MFA must use an authenticator app or hardware token. SMS-based MFA is permitted only where no alternative is available and must be reviewed for upgrade.

## 6. Service Accounts

Service account passwords must be:
- Randomly generated (minimum 20 characters)
- Stored in the approved password vault
- Known only to authorised administrators
- Rotated annually or immediately following personnel changes

## 7. Responsibilities

| Role | Responsibility |
|------|---------------|
| All staff | Comply with this policy; protect credentials; report suspected compromise |
| IT Manager | Enforce technical controls; manage password systems; conduct audits |
| Managing Director | Approve exceptions; ensure policy is resourced and enforced |

---

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [PLACEHOLDER] | [Your name] | Initial version |
