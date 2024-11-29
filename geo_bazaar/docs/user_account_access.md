# User Account Management Module

## Description
This endpoint allows users to view and update their account details, such as their name, email, and other profile information.

---

## 1. Get User Account Details

### Method: **GET**

**Endpoint**: `/user-account`

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
| **200**     | `{"message": "User details fetched successfully", "data": {user details}}` |
| **401**     | `{"error": "Unauthorized. Please provide a valid token."}` |
| **500**     | `{"error": "Server error. Please try again later."}`     |

---

### Example Request

**Headers:**

```http
Authorization: Bearer JWT_TOKEN
