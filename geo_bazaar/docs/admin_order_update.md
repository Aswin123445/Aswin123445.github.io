# Admin Orders Module

## 2. Update Order

### Description
Allows the admin to update the status or details of a specific order, including user and product details.

---

### Method: **PUT**

**Endpoint**: `/admin/orders/{order_id}`

---

### Request

#### Headers

| Parameter Name     | Description                  | Type     |
|--------------------|------------------------------|----------|
| **Authorization**  | Bearer token for admin auth  | `String` |

#### Body Parameters

| Parameter Name     | Description                              | Type     | Length |
|--------------------|------------------------------------------|----------|--------|
| **order_id**       | ID of the order to be updated            | `Integer`| N/A    |
| **status**         | New status of the order                  | `String` | N/A    |
| **notes**          | (Optional) Admin notes                   | `String` | N/A    |
| **user_name**      | Name of the user who placed the order    | `String` | N/A    |
| **product_name**   | Name of the product in the order         | `String` | N/A    |
| **address**        | Delivery address for the order           | `String` | N/A    |
| **contact_number** | Contact number of the user               | `String` | N/A    |
| **quantity**       | Quantity of the product ordered          | `Integer`| N/A    |
| **total_price**    | Total price of the order                 | `Float`  | N/A    |

> **Note:** The `order_id` is passed as a URL path parameter. The `Authorization` header contains the admin token for authentication.

---

### Response

| Status Code | Description                                      |
|-------------|--------------------------------------------------|
| **200**     | `"Order updated successfully"`                   |
| **400**     | `{"error": "Invalid status value"}`              |
| **401**     | `{"error": "Unauthorized access, invalid token"}`|
| **404**     | `{"error": "Order not found"}`                   |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
