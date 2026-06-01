# Asset Register — BrightPath Tutoring Ltd

**Document Reference:** GRC-RA-AR-001
**Version:** 1.0
**Date:** 2026-06-01
**Owner:** Director (acting Information Asset Owner)
**Classification:** Internal — Confidential

This asset register defines the information, system, people, and physical assets considered in the assessment.

---

## 1. Purpose

This asset register inventories the information assets of BrightPath Tutoring Ltd. Identifying and classifying assets is the foundation of the risk assessment: threats and risks in the [threat register](./threat-register.md) and [risk register](./risk-register.md) are evaluated against these assets.

---

## 2. Asset classification scheme

| Classification | Description |
|---------------|-------------|
| **Critical** | Loss or compromise would cause severe disruption, a serious UK GDPR breach, or major financial/reputational harm |
| **High** | Loss or compromise would cause significant operational impact and potential regulatory exposure |
| **Medium** | Loss or compromise would cause moderate, recoverable disruption |
| **Low** | Loss or compromise would cause minor inconvenience only |

---

## 3. Asset register

### Category 1 — Data assets

| Asset ID | Asset | Description | Classification | Owner | Location |
|----------|-------|-------------|---------------|-------|----------|
| DA-01 | Student personal data | Names, ages, schools, contact details, learning needs of minors | **Critical** | Director | M365 (SharePoint/OneDrive), WordPress enquiry forms |
| DA-02 | Parent/customer data | Parent contact details and account information | **Critical** | Director | M365, WordPress, Stripe |
| DA-03 | Lesson recordings | Recorded video lessons featuring minors | **Critical** | Director | Zoom cloud / OneDrive |
| DA-04 | Payment-related data | Transaction records and references (card data handled by Stripe, not stored by BrightPath) | High | Director | Stripe dashboard, Xero |
| DA-05 | Staff & contractor data | Tutor personal data, contracts, payroll details | High | Director | M365, Xero |
| DA-06 | Email & messages | Internal and customer correspondence | High | Director | Microsoft 365 |
| DA-07 | Learning resources | Worksheets, lesson materials, IP | Medium | Tutors | OneDrive / SharePoint |
| DA-08 | Website content | Public marketing content and blog | Low | Director | WordPress |

---

### Category 2 — System & application assets

| Asset ID | Asset | Description | Classification | Owner | Location |
|----------|-------|-------------|---------------|-------|----------|
| SY-01 | Microsoft 365 tenant | Email, Teams, SharePoint, OneDrive, identity (Entra ID) | **Critical** | Director | Cloud (Microsoft) |
| SY-02 | WordPress website | Marketing site + booking/enquiry forms | High | Director | Shared web hosting |
| SY-03 | Stripe payment service | Hosted checkout for online payments | High | Director | Cloud (Stripe) |
| SY-04 | Video platform (Zoom/Teams) | Live and recorded lesson delivery | High | Director | Cloud |
| SY-05 | Staff laptops | ~10 Windows devices (company-owned + BYOD) | High | Tutors / Director | Remote / home offices |
| SY-06 | Xero accounting | Invoicing and bookkeeping | Medium | Director | Cloud |
| SY-07 | Domain & DNS | Company domain name and DNS records | High | Director | Domain registrar |

---

### Category 3 — People assets

| Asset ID | Asset | Description | Classification | Owner |
|----------|-------|-------------|---------------|-------|
| PE-01 | Directors | Own the business; M365 global admin held here | **Critical** | Board |
| PE-02 | Office administrator | Handles bookings, customer data, payments | High | Director |
| PE-03 | Tutors / contractors | Deliver lessons; access student data and recordings | High | Director |

---

### Category 4 — Physical assets

| Asset ID | Asset | Description | Classification | Owner | Location |
|----------|-------|-------------|---------------|-------|----------|
| PH-01 | Laptops & mobile devices | Physical endpoints used to access business data | High | Tutors / Director | Home offices, in transit |
| PH-02 | Printed materials | Any printed student information | Medium | Staff | Home offices |

---

## 4. Asset register review

| Review date | Reviewer | Changes |
|------------|---------|---------|
| 2026-06-01 | Justin Dzanjalimodzi | Initial version |
