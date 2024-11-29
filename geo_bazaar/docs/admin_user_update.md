# Admin Customers Module

## 11. Update Customer

### Description
Allows the admin to update details of an existing customer, such as name, email, phone number, and address.

---

### Method: **PUT**

**Endpoint**: `/admin/customers/{customer_id}`

---

### Request

| Parameter Name  | Description                             | Type     | Length |
|-----------------|-----------------------------------------|----------|--------|
| **customer_id** | ID of the customer to be updated        | `Integer`| N/A    |
| **token**       | Admin authentication token              | `String` | N/A    |
| **name**        | (Optional) New name of the customer     | `String` | 1-255  |
| **email**       | (Optional) New email address            | `String` | 1-255  |
| **phone**       | (Optional) New phone number             | `String` | 1-15   |
| **address**     | (Optional) New address                  | `String` | N/A    |

> **Note:** The `token` should be passed in the request header for authorization. At least one parameter (`name`, `email`, `phone`, or `address`) should be provided for updating the customer.

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **200**     | `"Customer updated successfully"`                   |
| **400**     | `{"error": "Invalid input, missing required fields"}`|
| **401**     | `{"error": "Unauthorized access, invalid token"}`   |
| **404**     | `{"error": "Customer not found"}`                   |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
