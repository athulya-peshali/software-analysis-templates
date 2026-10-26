<!--
  Document   : API Specification Template
  Author     : Athulya Peshali
  Role       : Systems Analyst / Business Analyst
  Notice     : Prepared for portfolio verification.
-->

<div align="center">

# API Integration Specification

### `[Project Name]`

*Technical contract defining RESTful endpoints, request payloads, and response structures.*

</div>

---

## 1. Document Control

| Field | Details |
|---|---|
| **Document ID** | `API-[PROJ]-001` |
| **API Version** | `v1.0` |
| **Base URL** | `https://api.yourdomain.com/v1` |
| **Author** | Athulya Peshali, Systems Analyst |
| **Status** | Draft / Approved / Deprecated |

---

## 2. Authentication & Headers

All API requests must include a secure authorization token and specify the content type.

| Header Name | Required | Value / Format | Description |
| :--- | :---: | :--- | :--- |
| `Authorization` | Yes | `Bearer <JWT_TOKEN>` | JSON Web Token obtained via the `/auth/login` endpoint. |
| `Content-Type` | Yes | `application/json` | All payloads must be formatted as standard JSON. |

---

## 3. Endpoint Specifications

### 3.1 Create a New User
*Registers a new user in the system and returns a unique profile ID.*

* **URL:** `/users/register`
* **Method:** `POST`
* **Authentication Required:** No

**Request Payload (JSON):**
```json
{
  "first_name": "John",
  "last_name": "Doe",
  "email": "john.doe@example.com",
  "password": "securePassword123!"
}
