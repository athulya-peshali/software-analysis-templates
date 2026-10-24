<!--
  Document   : Requirements Traceability Matrix (RTM) Template
  Author     : Athulya Peshali
  Role       : Business Analyst
  Notice     : Prepared for portfolio verification. 
-->

<div align="center">

# Requirements Traceability Matrix (RTM)

### `[Project Name]`

*Ensuring complete coverage from business requirements to testing and deployment.*

</div>

---

## Document Control

| Field | Details |
|---|---|
| **Document Title** | Requirements Traceability Matrix: `[Project Name]` |
| **Document ID** | `RTM-[PROJ]-001` |
| **Version** | `0.1 (Draft)` |
| **Author** | Athulya Peshali, Business Analyst |
| **Date Created** | `YYYY-MM-DD` |
| **Last Updated** | `YYYY-MM-DD` |

---

## 1. Introduction

### 1.1 Purpose
The Requirements Traceability Matrix (RTM) ensures that all approved business and stakeholder requirements defined in the SRS are traced to their corresponding functional requirements, system components, and test cases. It serves as a single source of truth to guarantee that no scope is missed during development and QA.

### 1.2 Status Definitions
* **Draft:** Requirement is defined but not yet implemented.
* **In Progress:** Currently under development.
* **In Testing:** Development complete, currently with QA.
* **Pass:** Tested and verified successfully.
* **Fail:** Failed testing; awaiting bug fix.

---

## 2. Traceability Matrix

| Business Req ID | Stakeholder / Source | User Story / Description | Functional Req ID (SRS) | Technical Component / UI | Test Case ID | Status | Release |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BR-01** | STK-01 (Sponsor) | US-01: As a user, I want to securely log into the system. | FR-001, FR-002 | `Login UI`, `Auth API` | TC-001, TC-002 | Pass | v1.0 |
| **BR-02** | STK-02 (End User) | US-02: As a user, I want to request a password reset link. | FR-010 | `Forgot Password UI` | TC-015 | In Progress| v1.1 |
| **BR-03** | Compliance | NFR-S-01: Passwords must be hashed using bcrypt. | N/A | `Database Schema` | TC-050 | Draft | v1.0 |
| **BR-04** | STK-03 (Marketing) | US-03: As an admin, I want to export customer lists to CSV. | FR-045, FR-046 | `Admin Dashboard` | TC-088 | In Testing | v2.0 |

---

## 3. Coverage Summary

| Metric | Count | Percentage |
| :--- | :--- | :--- |
| **Total Business Requirements** | `[Total Count]` | 100% |
| **Requirements with Test Cases** | `[Count]` | `[%]` |
| **Requirements Passed** | `[Count]` | `[%]` |
| **Requirements Pending / Failed** | `[Count]` | `[%]` |

---

<div align="center">

**© 2026 Athulya Peshali · All rights reserved**
*Prepared for portfolio verification. Not for unauthorised distribution or reproduction.*

</div>
