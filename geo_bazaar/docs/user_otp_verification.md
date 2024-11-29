# OTP Verification Module

## Description
This endpoint allows users to verify their OTP (One-Time Password) for account activation or other secure actions like password reset. The OTP is typically sent to the user's registered email.

---

### Method: **POST**

**Endpoint**: `/otp-verification`

---

### Request

| Parameter Name | Description                       | Type     | Length  |
|----------------|-----------------------------------|----------|---------|
| **email**      | User's registered email           | `String` | Valid email |
| **otp**        | One-Time Password sent to the user| `String` | 6 chars  |

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | `{"message": "OTP verified successfully"}`            |
| **400**     | `{"error": "Invalid OTP or email"}`                   |
| **404**     | `{"error": "User not found"}`                         |
| **500**     | `{"error": "Server error. Please try again later."}`   |

---

### Example Request

**Headers:**

```http
Content-Type: application/json
