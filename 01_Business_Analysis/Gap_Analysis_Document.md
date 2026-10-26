<!--
  Document   : Gap Analysis Template
  Author     : Athulya Peshali
  Role       : Business Analyst
  Notice     : Prepared for portfolio verification.
-->

<div align="center">

# Gap Analysis Document

### `[Project Name]`

*Evaluating the delta between current capabilities and future operational goals.*

</div>

---

## 1. Document Control

| Field | Details |
|---|---|
| **Document ID** | `GAP-[PROJ]-001` |
| **Business Domain** | `[e.g., Sales Operations, Customer Success]` |
| **Author** | Athulya Peshali, Business Analyst |
| **Date Created** | `YYYY-MM-DD` |
| **Status** | Draft / In Review / Approved |

---

## 2. Executive Summary
*Provide a concise summary of the operational gap being addressed, the target state, and the primary recommendations required to bridge the divide.*

> **Summary:** The current `[System/Process]` lacks the capability to `[Core Deficiency]`, resulting in `[Impact]`. To achieve the target state of `[Target Goal]`, this analysis identifies critical gaps in `[Technology / Process / People]` and recommends `[High-level solution]`.

---

## 3. Current State Analysis ("As-Is")

### 3.1 Overview
*Describe the existing system architecture, operational workflow, or business process.*

### 3.2 Key Pain Points
* **Pain Point 1:** `[e.g., Data must be manually exported to Excel for weekly reporting, taking 6 hours.]`
* **Pain Point 2:** `[e.g., No real-time synchronization between the CRM and the inventory database.]`
* **Pain Point 3:** `[e.g., Current server architecture cannot support more than 500 concurrent users.]`

---

## 4. Target State Definition ("To-Be")

### 4.1 Overview
*Describe the desired future state, focusing on capabilities, performance metrics, and business outcomes.*

### 4.2 Success Criteria
* **Goal 1:** `[e.g., Fully automated weekly reporting dashboard generated in under 10 seconds.]`
* **Goal 2:** `[e.g., Bidirectional API sync between CRM and inventory resolving within 1 minute.]`
* **Goal 3:** `[e.g., Cloud-based infrastructure auto-scaling to support up to 5,000 concurrent users.]`

---

## 5. Gap Identification Matrix

| Category | Current State (As-Is) | Target State (To-Be) | Identified Gap | Severity |
| :--- | :--- | :--- | :--- | :--- |
| **Technology** | On-premise legacy database (SQL Server 2012). | Cloud-native, scalable relational database. | Missing cloud infrastructure and automated migration pipelines. | **High** |
| **Process** | Manual invoice generation via PDF templates. | One-click automated invoice generation and email dispatch. | No logic exists to trigger invoice creation upon order fulfillment. | **High** |
| **People/Skills** | Support team operates via shared email inbox. | Support team operates via unified ticketing system. | Staff lacks training on the new ticketing software. | **Medium** |
| **Data** | Customer records duplicated across 3 systems. | Single Source of Truth (SSOT) for customer profiles. | Missing data deduplication and standardization scripts. | **Critical** |

---

## 6. Action Plan & Recommendations

### 6.1 Recommended Initiatives
*List the specific projects, features, or organizational changes required to close the gaps identified above.*

1. **`[Initiative Name, e.g., Cloud Migration Phase 1]`**
   * **Description:** Migrate legacy SQL database to AWS RDS.
   * **Assigned To:** Data Engineering Team
2. **`[Initiative Name, e.g., Billing Automation Module]`**
   * **Description:** Develop microservice to listen for `order_fulfilled` events and trigger invoice generation.
   * **Assigned To:** Backend Engineering Team
3. **`[Initiative Name, e.g., Support Training]`**
   * **Description:** Conduct 2-day workshop on Zendesk ticketing workflows.
   * **Assigned To:** HR / Operations

---

<div align="center">

**© 2026 Athulya Peshali · All rights reserved**
*Prepared for portfolio verification. Not for unauthorised distribution or reproduction.*

</div>
