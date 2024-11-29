# Add Item to Cart

## Description
This endpoint allows users to add a product to their cart. The user can specify the product and the desired quantity.

---

## Method: **POST**

**Endpoint**: `/cart`

---

### Request Body

| Parameter Name  | Description              | Type     | Length   |
|-----------------|--------------------------|----------|----------|
| **product_id**  | ID of the product        | `Integer`| Required |
| **quantity**    | Quantity of the product  | `Integer`| Required |

---

### Response

| Status Code | Description                                      |
|-------------|--------------------------------------------------|
| **201**     | `{"message": "Item added to cart successfully"}` |
| **400**     | `{"error": "Invalid product or quantity"}`      |
| **404**     | `{"error": "Product not found"}`                 |
| **500**     | `{"error": "Server error. Please try again later."}` |

---

### Example Request Body

```json
{
  "product_id": 101,
  "quantity": 2
}
