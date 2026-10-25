<!--
  Document   : Use Case Specification Template
  Author     : Athulya Peshali
  Role       : Business Analyst
  Standards  : UML / IEEE 830 Standard Alignment
  Notice     : Prepared for portfolio verification.
-->

<div align="center">

# Use Case Specification

### `[UC-01: Use Case Title]`

*Detailed functional interaction model between actors and the system.*

</div>

---

## 1. Document Control

| Field | Details |
|---|---|
| **Use Case ID** | `UC-[PROJ]-001` |
| **Use Case Name** | `[e.g., Process Customer Checkout]` |
| **Primary Actor** | `[e.g., Registered Customer]` |
| **Secondary Actors** | `[e.g., Payment Gateway, Email Service]` |
| **Author** | Athulya Peshali, Business Analyst |
| **Status** | Draft / In Review / Approved |
| **Version** | `1.0` |

---

## 2. Overview & Context

### 2.1 Brief Description
*Provide a concise 2–3 sentence description of what this use case accomplishes.*

> Example: This use case describes the process by which a registered customer submits payment for items in their shopping cart, generates an order record, and receives confirmation.

### 2.2 Preconditions
1. The user must be logged into a valid customer account.
2. The user's shopping cart must contain at least one item.

### 2.3 Postconditions
* **Success (Guaranteed):** The order is saved in the database with status `PENDING_PAYMENT`, inventory is reserved, and an order confirmation email is sent.
* **Failure:** No charge is made, the shopping cart contents remain unchanged, and an error message is displayed.

### 2.4 Trigger
* The user clicks the **"Proceed to Checkout"** button on the cart summary page.

---

## 3. Execution Flows

```mermaid
sequenceDiagram
    autonumber
    actor User as Primary Actor
    participant System as System
    participant PG as Payment Gateway

    User->>System: 1. Initiates Checkout
    System->>User: 2. Displays Payment Form
    User->>System: 3. Submits Payment Details
    System->>PG: 4. Authorizes Payment
    PG-->>System: 5. Returns Success
    System-->>User: 6. Displays Order Receipt
