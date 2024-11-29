# Admin Products Module

## 1. List All Products

### Description
Allows the admin to retrieve a list of all available products in the system.

---

### Method: **GET**

**Endpoint**: `/admin/products`

---

### Request

| Parameter Name | Description                  | Type     | Length |
|----------------|------------------------------|----------|--------|
| **token**      | Admin authentication token   | `String` | N/A    |
| **page**       | (Optional) Pagination page   | `Integer`| N/A    |
| **category**   | (Optional) Filter by product category | `String` | N/A  |

> **Note:** The `token` should be passed in the request header for authorization.

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **200**     | Returns a paginated list of all products            |
| **401**     | `{"error": "Unauthorized access, invalid token"}`   |
| **404**     | `{"error": "No products found"}`                    |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
