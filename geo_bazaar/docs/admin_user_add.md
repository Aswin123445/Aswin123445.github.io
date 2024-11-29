# Admin Customers Module

## 12. Add New Customer

### Description
Allows the admin to add a new customer to the system by providing all necessary details.

---

### Method: **POST**

**Endpoint**: `/admin/customers`

---

### Request

| Parameter Name  | Description                             | Type     | Length |
|-----------------|-----------------------------------------|----------|--------|
| **token**       | Admin authentication token              | `String` | N/A    |
| **name**        | Name of the new customer                | `String` | 1-255  |
| **email**       | Email address of the new customer       | `String` | 1-255  |
| **phone**       | Phone number of the new customer        | `String` | 1-15   |
| **address**     | Address of the new customer             | `String` | N/A    |
| **password**    | Password for the new customer account   | `String` | 6-128  |

> **Note:** The `token` should be passed in the request header for authorization.

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **201**     | `"Customer added successfully"`                     |
| **400**     | `{"error": "Invalid input, missing required fields"}`|
| **401**     | `{"error": "Unauthorized access, invalid token"}`   |
| **409**     | `{"error": "Customer with this email already exists"}`|

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
