<!--
  Document   : Data Dictionary Template
  Author     : Athulya Peshali
  Role       : Systems Analyst / Business Analyst
  Notice     : Prepared for portfolio verification.
-->

<div align="center">

# Data Dictionary

### `[Project Name]`

*Comprehensive specification of database entities, attributes, and constraints.*

</div>

---

## 1. Document Control

| Field | Details |
|---|---|
| **Document ID** | `DD-[PROJ]-001` |
| **Target Database** | `[e.g., PostgreSQL 15, MongoDB]` |
| **Author** | Athulya Peshali, Systems Analyst |
| **Date Created** | `YYYY-MM-DD` |
| **Status** | Draft / In Review / Approved |

---

## 2. Entity-Relationship Overview
*Provide a brief summary of the core entities and how they relate to one another.*

> **Example:** The `Users` table has a one-to-many relationship with the `Orders` table. Each `Order` has a one-to-many relationship with `Order_Items`, which links to the `Products` table via a Foreign Key.

---

## 3. Data Schema Specifications

### Table: `users`
**Description:** Stores core authentication and profile data for registered customers.

| Column Name | Data Type | Length | Constraints | Default | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `user_id` | UUID | 36 | PK, Not Null, Unique | `uuid_generate_v4()` | Unique identifier for the user. |
| `email` | VARCHAR | 255 | Not Null, Unique | None | User's primary email address (used for login). |
| `password_hash` | VARCHAR | 255 | Not Null | None | Bcrypt hashed password. Never stored in plain text. |
| `is_active` | BOOLEAN | - | Not Null | `TRUE` | Indicates if the account is currently active. |
| `created_at` | TIMESTAMP | - | Not Null | `CURRENT_TIMESTAMP` | Date and time the account was registered. |

### Table: `orders`
**Description:** Records transactional purchase data linked to a specific user.

| Column Name | Data Type | Length | Constraints | Default | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `order_id` | INT | - | PK, Not Null, Auto-Inc| None | Sequential unique identifier for the order. |
| `user_id` | UUID | 36 | FK (users.user_id) | None | Links the order to the purchasing user. |
| `total_amount` | DECIMAL | 10,2 | Not Null | `0.00` | Total monetary value of the order, including tax. |
| `status` | ENUM | - | Not Null | `'PENDING'` | Allowed values: `PENDING`, `PAID`, `SHIPPED`, `CANCELLED`. |
| `updated_at` | TIMESTAMP | - | Not Null | `CURRENT_TIMESTAMP` | Timestamp of the last status change. |

---

## 4. Constraint Definitions

*   **PK (Primary Key):** A unique identifier for a record within a table.
*   **FK (Foreign Key):** A field that uniquely identifies a row of another table, establishing a link.
*   **Not Null:** The field cannot be left blank; it must contain a valid value.
*   **Unique:** No two rows can have the same value for this specific column.
*   **Auto-Inc (Auto-Increment):** The database automatically generates a sequential numeric value for each new record.

---

<div align="center">

**© 2026 Athulya Peshali · All rights reserved**
*Prepared for portfolio verification. Not for unauthorised distribution or reproduction.*

</div>
