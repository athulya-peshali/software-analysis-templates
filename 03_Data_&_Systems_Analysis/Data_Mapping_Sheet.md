<!--
  Document   : Data Mapping & ETL Specification
  Author     : Athulya Peshali
  Role       : Systems Analyst / Business Analyst
  Notice     : Prepared for portfolio verification.
-->

<div align="center">

# Data Mapping Specification

### `[Project Name]`

*Field-by-field ETL (Extract, Transform, Load) translation rules for system integration.*

</div>

---

## 1. Document Control

| Field | Details |
|---|---|
| **Document ID** | `MAP-[PROJ]-001` |
| **Source System** | `[e.g., Legacy CRM v4.1 (SQL Server)]` |
| **Target System** | `[e.g., Salesforce Cloud (SOQL)]` |
| **Author** | Athulya Peshali, Systems Analyst |
| **Status** | Draft / In Review / Approved |

---

## 2. System Architecture Overview

* **Extraction Strategy:** Nightly batch export via secure FTP at 02:00 UTC.
* **Transformation:** Python middleware script applying logic defined in Section 3.
* **Load Strategy:** REST API `POST` requests to the Target System.

---

## 3. Field Mapping & Transformation Rules

### Entity: `Customer Profile`

| Source Field | Source Type | Target Field | Target Type | Transformation Logic / Fallback | Requirement |
| :--- | :--- | :--- | :--- | :--- | :---: |
| `Cust_ID` | `INT` | `Account_ID` | `VARCHAR(50)` | Cast as String; Prefix with `"LEG-"`. | Mandatory |
| `Full_Name` | `VARCHAR` | `FirstName` <br> `LastName` | `VARCHAR` <br> `VARCHAR` | Split string at first whitespace. | Mandatory |
| `DOB` | `DATETIME` | `BirthDate` | `DATE` | Strip timestamp; convert to `YYYY-MM-DD`. | Optional |
| `Phone_Num` | `VARCHAR(15)`| `MobilePhone` | `VARCHAR(15)` | Strip special characters `( ) -`. If null, drop record. | Mandatory |
| `Is_Active` | `BIT` (1/0) | `Status` | `ENUM` | If `1`, set to `"ACTIVE"`. If `0`, set to `"INACTIVE"`. | Mandatory |

---

## 4. Error Handling & Data Cleansing

| Error Condition | Action to Take | Logging Requirement |
| :--- | :--- | :--- |
| **Missing Mandatory Field** | Reject record from import batch. | Log `Source_ID` and "Missing Mandatory Field" to `etl_error.log`. |
| **Data Type Mismatch** | Attempt fallback cast. If failed, reject record. | Log `Source_ID` and "Cast Failure" to `etl_error.log`. |
| **Duplicate Target ID** | Overwrite existing target record (Upsert). | None. |

---

<div align="center">

**© 2026 Athulya Peshali · All rights reserved**
*Prepared for portfolio verification. Not for unauthorised distribution or reproduction.*

</div>
