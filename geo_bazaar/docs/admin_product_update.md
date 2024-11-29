# Admin Products Module

## 2. Update Product

### Description
Allows the admin to update the details of an existing product, including name, price, stock, and category.

---

### Method: **PUT**

**Endpoint**: `/admin/products/{product_id}`

---

### Request

| Parameter Name  | Description                             | Type     | Length |
|-----------------|-----------------------------------------|----------|--------|
| **product_id**  | ID of the product to be updated         | `Integer`| N/A    |
| **token**        | Admin authentication token              | `String` | N/A    |
| **name**         | (Optional) New name of the product      | `String` | N/A    |
| **category**     | (Optional) New category of the product  | `String` | N/A    |
| **price**        | (Optional) New price of the product     | `Float`  | N/A    |
| **stock**        | (Optional) New stock quantity          | `Integer`| N/A    |

> **Note:** The `token` should be passed in the request header for authorization. At least one parameter (`name`, `category`, `price`, or `stock`) should be provided to update the product.

---

### Response

| Status Code | Description                                      |
|-------------|--------------------------------------------------|
| **200**     | `"Product updated successfully"`                 |
| **400**     | `{"error": "Invalid input, some parameters missing or invalid"}`|
| **401**     | `{"error": "Unauthorized access, invalid token"}`|
| **404**     | `{"error": "Product not found"}`                 |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
