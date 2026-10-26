<!--
  Document   : Risk Register Template
  Author     : Athulya Peshali
  Role       : Project Manager
  Notice     : Prepared for portfolio verification.
-->

<div align="center">

# Risk Register

### `[Project Name]`

*Identification, evaluation, and mitigation planning for project risks.*

</div>

---

## 1. Document Control

| Field | Details |
|---|---|
| **Document ID** | `RISK-[PROJ]-001` |
| **Project Manager** | Athulya Peshali |
| **Date Created** | `YYYY-MM-DD` |
| **Last Updated** | `YYYY-MM-DD` |

---

## 2. Risk Scoring Matrix

Risk priority is calculated by multiplying **Probability (P)** by **Impact (I)** on a scale of 1 to 5.

* **High Risk (15 - 25):** Requires immediate mitigation strategy and executive visibility.
* **Medium Risk (8 - 14):** Requires active monitoring and contingency planning.
* **Low Risk (1 - 7):** Accepted risk; monitor periodically.

---

## 3. Active Risk Log

| Risk ID & Category | Risk Description | Score (P $\times$ I) | Mitigation Plan | Owner & Status |
| :--- | :--- | :--- | :--- | :--- |
| **RSK-01** <br> *Technical* | Cloud database migration fails, causing data loss. | **P:** 2, **I:** 5 <br> **Score: 10 (Med)** | Perform migration on a staging replica first; ensure daily backups are verified. | Data Lead <br> *Open* |
| **RSK-02** <br> *Resource* | Senior UI Developer goes on planned medical leave mid-sprint. | **P:** 4, **I:** 4 <br> **Score: 16 (High)** | Cross-train junior developers immediately; negotiate contractor budget with sponsor. | PM <br> *Mitigating* |
| **RSK-03** <br> *Scope* | Stakeholders request additional features after freeze. | **P:** 4, **I:** 3 <br> **Score: 12 (Med)** | Enforce strict Change Request (CR) process; require sponsor signature for new scope. | BA <br> *Open* |
| **RSK-04** <br> *Vendor* | Third-party payment API documentation is outdated. | **P:** 3, **I:** 2 <br> **Score: 6 (Low)** | Allocate extra buffer time in the sprint schedule for API exploration and testing. | Dev Lead <br> *Closed* |

---

## 4. Issue Log (Realized Risks)

*Risks that have actually occurred and transition into active issues requiring immediate resolution.*

| Issue ID | Linked Risk | Issue Description | Resolution Steps | Status |
| :--- | :--- | :--- | :--- | :--- |
| **ISS-01** | RSK-04 | Payment API deprecated endpoint v1, causing test failures. | Dev team updating payloads to endpoint v2. Expect 1-day delay to testing milestone. | In Progress |

---

<div align="center">

**© 2026 Athulya Peshali · All rights reserved**
*Prepared for portfolio verification. Not for unauthorised distribution or reproduction.*

</div>
