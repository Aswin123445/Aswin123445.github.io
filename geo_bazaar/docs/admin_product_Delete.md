# Admin Products Module

## 3. Delete Product

### Description
Allows the admin to delete a specific product from the system.

---

### Method: **DELETE**

**Endpoint**: `/admin/products/{product_id}`

---

### Request

| Parameter Name | Description                  | Type     | Length |
|----------------|------------------------------|----------|--------|
| **product_id** | ID of the product to be deleted| `Integer`| N/A    |
| **token**      | Admin authentication token   | `String` | N/A    |

> **Note:** The `token` should be passed in the request header for authorization.

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **200**     | `"Product deleted successfully"`                    |
| **401**     | `{"error": "Unauthorized access, invalid token"}`   |
| **404**     | `{"error": "Product not found"}`                    |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
