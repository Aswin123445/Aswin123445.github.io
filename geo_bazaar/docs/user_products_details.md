# Product Details Module

## 4. Product Details

### Description
This endpoint retrieves detailed information about a specific product, including its description, price, availability, and other metadata.

---

### Method: **GET**

**Endpoint**: `/products/{product_id}`

---

### Request

| Parameter Name  | Description                        | Type     | Required |
|-----------------|------------------------------------|----------|----------|
| **product_id**  | ID of the product to retrieve      | `Integer`| Yes      |
| **token**       | (Optional) User authentication token | `String` | No       |

---

### Response

| Status Code | Description                                      |
|-------------|--------------------------------------------------|
| **200**     | Returns detailed information about the product   |
| **404**     | `{"error": "Product not found"}`                 |
| **401**     | `{"error": "Unauthorized access, invalid token"}`|

---


