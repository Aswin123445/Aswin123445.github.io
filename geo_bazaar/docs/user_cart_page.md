# Cart Page Module

## Description
This endpoint allows users to view and manage the items in their shopping cart. It includes functionality to view the cart, add items, remove items, and update quantities.

---

## 1. View Cart

### Method: **GET**

**Endpoint**: `/cart`

---

### Request

**Headers:**

| Header Name    | Description                   | Type     |
|----------------|-------------------------------|----------|
| **Authorization** | JWT Token for authentication | `String` |

---

### Response

| Status Code | Description                                             |
|-------------|---------------------------------------------------------|
| **200**     | `{"message": "Cart details fetched successfully", "data": {cart items}}` |
| **401**     | `{"error": "Unauthorized. Please provide a valid token."}` |
| **404**     | `{"error": "Cart not found"}` |
| **500**     | `{"error": "Server error. Please try again later."}`     |

---

### Example Request

**Headers:**

```http
Authorization: Bearer JWT_TOKEN
