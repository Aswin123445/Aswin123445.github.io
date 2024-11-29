# Delete Item from Cart

## Description
This endpoint allows users to remove a specific item from their cart. No authentication or headers are required for this operation.

---

### Method: **DELETE**

**Endpoint**: `/cart/item/{item_id}`

---

### Request

**Parameters:**

| Parameter Name | Description               | Type     | Required |
|----------------|---------------------------|----------|----------|
| **item_id**    | ID of the cart item to delete | `Integer` | Yes      |

---

### Response

| Status Code | Description                                      |
|-------------|--------------------------------------------------|
| **200**     | `{"message": "Item removed from cart successfully"}` |
| **404**     | `{"error": "Item not found"}`                    |
| **500**     | `{"error": "Server error. Please try again later."}` |

---

### Example Request

**Endpoint**: `/cart/item/123`

---

