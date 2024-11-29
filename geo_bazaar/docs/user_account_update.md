# Update User Account Module

## Description
This endpoint allows authenticated users to update their account details, including their name, email, and profile picture.

---

### Method: **PUT**

**Endpoint**: `/user-account`

---

### Request

**Headers:**

| Header Name    | Description                   | Type     |
|----------------|-------------------------------|----------|
| **Authorization** | JWT Token for authentication | `String` |

**Request Body:**

| Parameter Name  | Description                          | Type     | Length      |
|-----------------|--------------------------------------|----------|-------------|
| **name**        | User's full name                     | `String` | 3-50 chars  |
| **email**       | User's email address                 | `String` | Valid email |
| **profile_picture** | URL for the user's profile picture | `String` | URL (optional) |

---

### Response

| Status Code | Description                                            |
|-------------|--------------------------------------------------------|
| **200**     | `{"message": "User details updated successfully"}`     |
| **400**     | `{"error": "Invalid data. Please check your input."}`  |
| **401**     | `{"error": "Unauthorized. Please provide a valid token."}` |
| **500**     | `{"error": "Server error. Please try again later."}`    |

---

### Example Request

**Headers:**

```http
Authorization: Bearer JWT_TOKEN
