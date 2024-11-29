# Admin Dashboard Module

## 2. Admin Dashboard

### Description
Allows an admin to access the dashboard to view system statistics and manage platform data.

---

### Method: **GET**

**Endpoint**: `/admin_dashboard`

---

### Request

| Parameter Name | Description                  | Type     | Length |
|----------------|------------------------------|----------|--------|
| **token**      | Admin authentication token   | `String` | N/A    |

> **Note:** The `token` should be passed in the request header for authorization.

---

### Response

| Status Code | Description                                        |
|-------------|----------------------------------------------------|
| **200**     | Returns dashboard data (system stats, user counts) |
| **401**     | `{"error": "Unauthorized access, invalid token"}`  |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
