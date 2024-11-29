# Wishlist Module

## Description
This endpoint allows users to view a list of products they have added to their wishlist.

---

### Method: **GET**

**Endpoint**: `/wishlist`

---

### Request


---

### Response

| Status Code | Description                                                 |
|-------------|-------------------------------------------------------------|
| **200**     | `{"message": "Wishlist fetched successfully", "data": [wishlist items]}` |
| **401**     | `{"error": "Unauthorized. Please provide a valid token."}`  |
| **500**     | `{"error": "Server error. Please try again later."}`        |

---

