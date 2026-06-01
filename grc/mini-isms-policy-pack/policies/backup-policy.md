# Backup Policy

**Document Reference:** POL-005  
**Version:** 1.0  
**Effective Date:** [PLACEHOLDER]  
**Review Date:** [PLACEHOLDER]  
**Owner:** IT Manager  
**ISO 27001 Control:** 8.13  
**Classification:** Internal

---

## 1. Purpose

To ensure that company information is regularly backed up and can be reliably restored in the event of data loss, system failure, or a destructive security incident such as ransomware.

## 2. Scope

This policy applies to all company information assets, including data stored in cloud services, on-premises systems, and staff devices.

## 3. Backup Requirements

### 3.1 Backup Strategy

The company follows a **3-2-1 backup strategy:**

- **3** copies of data: the original plus two backups
- **2** different storage media / locations
- **1** copy stored offsite or in a geographically separate cloud region

### 3.2 Backup Schedule

| Data / System | Backup Frequency | Retention Period | Location |
|--------------|-----------------|-----------------|---------|
| Microsoft 365 (email, SharePoint, OneDrive) | Daily (automated) | 90 days minimum | M365 retention + cloud backup |
| Cloud accounting system | Daily (provider backup) | [As per provider SLA] | Provider infrastructure |
| On-premises NAS / file server | Daily (automated) | 30 days local; 90 days offsite | NAS + offsite cloud |
| Staff workstations | Weekly (key business files) | 30 days | Cloud backup |

### 3.3 Encryption

All backups must be encrypted, both in transit and at rest, using AES-256 or equivalent.

### 3.4 Offsite and Immutable Backups

At least one copy of all critical backups must be stored offsite or in a cloud location that is logically separated from the primary environment. Where possible, backups should be stored in an immutable format to prevent deletion or encryption by ransomware.

## 4. Backup Testing and Restoration

Backups are of no value unless they can be successfully restored. Backup restoration must be tested:

- **Monthly:** Test restoration of a sample of files from at least one backup set
- **Quarterly:** Full restoration test of at least one critical system or dataset
- **After any significant infrastructure change:** Verify backups are still completing successfully

Restoration test results must be documented in the backup test log.

## 5. Responsibilities

| Role | Responsibility |
|------|---------------|
| IT Manager | Configure and maintain backup systems; conduct and document restoration tests |
| All staff | Ensure business data is stored in backed-up locations (not solely on local device storage) |
| Managing Director | Review backup testing results annually; approve budget for backup infrastructure |

## 6. Exceptions

Any system or data set that cannot meet these requirements must have a documented exception approved by the Managing Director, with an accepted risk and compensating controls in place.

---

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [PLACEHOLDER] | [Your name] | Initial version |
