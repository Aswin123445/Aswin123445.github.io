# Admin Products Module

## 4. Add Product

### Description
Allows the admin to add a new product to the system, including details like name, category, price, stock quantity, and more.

---

### Method: **POST**

**Endpoint**: `/admin/products`

---

### Request

| Parameter Name  | Description                             | Type     | Length |
|-----------------|-----------------------------------------|----------|--------|
| **token**        | Admin authentication token              | `String` | N/A    |
| **name**         | Name of the product                     | `String` | 1-255  |
| **category**     | Category of the product                 | `String` | 1-100  |
| **price**        | Price of the product                    | `Float`  | N/A    |
| **stock**        | Available stock quantity                | `Integer`| N/A    |
| **description**  | (Optional) Description of the product   | `String` | N/A    |
| **image_url**    | (Optional) Image URL for the product    | `String` | N/A    |

> **Note:** The `token` should be passed in the request header for authorization. All parameters are required unless marked as optional.

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **201**     | `"Product added successfully"`                      |
| **400**     | `{"error": "Invalid input, missing required fields"}`|
| **401**     | `{"error": "Unauthorized access, invalid token"}`   |
| **409**     | `{"error": "Product already exists"}`               |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
