# Update Cart Item Quantity

## Description
This endpoint allows users to update the quantity of items in their cart. It can also handle additional parameters such as size, color, or other product-specific options that might be associated with the cart item.

---

## Method: **PUT**

**Endpoint**: `/cart/update/{item_id}`

---


### Request Body

| Parameter Name  | Description                         | Type     | Required |
|-----------------|-------------------------------------|----------|----------|
| **product_id**  | ID of the product in the cart       | `Integer`| Yes      |
| **quantity**    | Quantity of the product             | `Integer`| Yes      |
| **size**        | Size of the product (if applicable) | `String` | No       |
| **color**       | Color of the product (if applicable)| `String` | No       |
| **note**        | Additional notes or requests        | `String` | No       |

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **200**     | `{"message": "Cart item updated successfully"}`     |
| **400**     | `{"error": "Invalid request parameters"}`           |
| **401**     | `{"error": "Unauthorized. Please provide a valid token."}` |
| **404**     | `{"error": "Cart item not found"}`                  |
| **500**     | `{"error": "Server error. Please try again later."}`|

---


