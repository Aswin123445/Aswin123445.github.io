# Admin Customers Module

## 5. List All Customers

### Description
Allows the admin to retrieve a list of all registered customers in the system.

---

### Method: **GET**

**Endpoint**: `/admin/customers`

---

### Request

| Parameter Name | Description                  | Type     | Length |
|----------------|------------------------------|----------|--------|
| **token**      | Admin authentication token   | `String` | N/A    |
| **page**       | (Optional) Pagination page   | `Integer`| N/A    |
| **search**     | (Optional) Search by customer name or email | `String` | N/A |

> **Note:** The `token` should be passed in the request header for authorization.

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **200**     | Returns a paginated list of all customers           |
| **401**     | `{"error": "Unauthorized access, invalid token"}`   |
| **404**     | `{"error": "No customers found"}`                   |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
