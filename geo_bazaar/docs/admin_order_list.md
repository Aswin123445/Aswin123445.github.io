# Admin Orders Module

## 3. Orders List

### Description
Allows the admin to retrieve a list of all orders, including details such as order status, total amount, and customer information.

---

### Method: **GET**

**Endpoint**: `/admin/orders`

---

### Request

| Parameter Name | Description                  | Type     | Length |
|----------------|------------------------------|----------|--------|
| **token**      | Admin authentication token   | `String` | N/A    |
| **status**     | (Optional) Filter by status  | `String` | N/A    |
| **page**       | (Optional) Pagination page   | `Integer`| N/A    |

> **Note:** The `token` should be passed in the request header for authorization.

---

### Response

| Status Code | Description                                   |
|-------------|-----------------------------------------------|
| **200**     | Returns a paginated list of all orders        |
| **401**     | `{"error": "Unauthorized access, invalid token"}` |
| **404**     | `{"error": "No orders found"}`               |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
