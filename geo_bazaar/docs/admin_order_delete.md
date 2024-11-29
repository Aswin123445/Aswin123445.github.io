# Admin Orders Module

## 5. Delete Order

### Description
Allows the admin to delete a specific order from the system.

---

### Method: **DELETE**

**Endpoint**: `/admin/orders/{order_id}`

---

### Request

| Parameter Name | Description                  | Type     | Length |
|----------------|------------------------------|----------|--------|
| **order_id**   | ID of the order to be deleted| `Integer`| N/A    |
| **token**      | Admin authentication token   | `String` | N/A    |

> **Note:** The `token` should be passed in the request header for authorization.

---

### Response

| Status Code | Description                                      |
|-------------|--------------------------------------------------|
| **200**     | `"Order deleted successfully"`                   |
| **401**     | `{"error": "Unauthorized access, invalid token"}`|
| **404**     | `{"error": "Order not found"}`                   |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
