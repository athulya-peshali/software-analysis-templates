<!--
  Document   : Change Request Form Template
  Author     : Athulya Peshali
  Role       : Project Manager
  Notice     : Prepared for portfolio verification.
-->

<div align="center">

# Change Request Form

### `[Project Name]`

*Formal assessment and approval of modifications to project scope, schedule, or budget.*

</div>

---

## 1. Request Details

| Field | Details |
|---|---|
| **CR ID** | `CR-[PROJ]-001` |
| **Requested By** | `[Stakeholder Name & Title]` |
| **Date Requested** | `YYYY-MM-DD` |
| **Priority** | Critical / High / Medium / Low |
| **Status** | Submitted / Under Review / Approved / Rejected |

---

## 2. Change Description

### 2.1 Proposed Change
*Clearly describe exactly what needs to be changed, added, or removed from the original project scope.*

> **Example:** Add a "Social Media Single Sign-On (SSO)" option allowing users to log in using Google and Apple accounts, in addition to the standard email/password login.

### 2.2 Business Justification
*Why is this change necessary right now? What happens if we do not implement it?*

> **Example:** Marketing analytics show a 40% drop-off rate at the current account creation screen. Implementing SSO is projected to increase user registration conversions by 25%.

---

## 3. Impact Analysis

*(To be completed by the Project Manager and Technical Leads).*

| Category | Impact Assessment | Estimated Delta |
| :--- | :--- | :--- |
| **Scope Impact** | Requires integration of Google and Apple OAuth APIs and updates to the database user schema. | +2 User Stories |
| **Schedule Impact** | Requires additional development and security testing time. | **+4 Days** |
| **Budget Impact** | 32 hours of backend developer time at $50/hr. | **+$1,600** |
| **Risk Impact** | Potential delay to the overall UAT phase if Apple API approval takes longer than 48 hours. | Medium Risk |

---

## 4. Alternative Options

| Option | Description | Recommendation |
|---|---|---|
| **Option A** | Implement Google SSO only to save 2 days of development time. | **Not Recommended** |
| **Option B** | Defer this feature to Phase 2 (post-launch update). | **Alternative** |

---

## 5. Formal Decision & Sign-Off

**Decision:** [ ] **Approved** &emsp; [ ] **Rejected** &emsp; [ ] **Deferred**

| Role | Name | Signature | Date |
|---|---|---|---|
| **Project Sponsor** | `[Name]` | | |
| **Change Control Board** | `[Name]` | | |
| **Project Manager** | Athulya Peshali | | |

*If approved, the Project Manager will update the project baseline schedule, budget, and Requirements Traceability Matrix (RTM) to reflect this change.*

---

<div align="center">

**© 2026 Athulya Peshali · All rights reserved**
*Prepared for portfolio verification. Not for unauthorised distribution or reproduction.*

</div>
