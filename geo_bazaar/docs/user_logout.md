# User Authentication Module

## 5. User Logout/Admin logout

### Description
This endpoint allows users to log out of their session. It will invalidate their session or authentication token, depending on how the user is authenticated.

---

### Method: **POST**

**Endpoint**: `/logout`

---

### Request

| Parameter Name | Description                     | Type     | Required |
|----------------|---------------------------------|----------|----------|
| **token**      | (Optional) User authentication token (if using token-based authentication) | `String` | No       |

---

### Response

| Status Code | Description                                      |
|-------------|--------------------------------------------------|
| **200**     | `{"message": "User logged out successfully"}`    |
| **400**     | `{"error": "Invalid request or token"}`          |
| **401**     | `{"error": "Unauthorized access, please login"}` |
| **500**     | `{"error": "Internal server error"}`             |

---


