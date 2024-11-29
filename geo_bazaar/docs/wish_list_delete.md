# Delete Product from Wishlist

## Description
This endpoint allows users to remove a specific product from their wishlist.

---

## Endpoint: **DELETE** `/wishlist/{product_id}`

### Method: **DELETE**

---

### Request



**Path Parameters:**

| Parameter Name | Description                  | Type     |
|----------------|------------------------------|----------|
| **product_id** | Unique ID of the product in the wishlist | `Integer` |

---

### Response

| Status Code | Description                                                  |
|-------------|--------------------------------------------------------------|
| **200**     | `{"message": "Product successfully removed from wishlist"}`  |
| **404**     | `{"error": "Product not found in wishlist"}`                 |
| **401**     | `{"error": "Unauthorized. Please provide a valid token."}`   |
| **500**     | `{"error": "Server error. Please try again later."}`         |

---

### Example Request


