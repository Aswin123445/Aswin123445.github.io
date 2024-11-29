# User Signin and OTP Verification Module

## 3. User Signin

### Description
This endpoint allows users to sign in by providing their credentials. If the credentials are correct, the server returns an authentication token. Optionally, users may require OTP verification for added security.

---

### Method: **POST**

**Endpoint**: `/signin`

---

### Request

| Parameter Name | Description              | Type     | Length     |
|----------------|--------------------------|----------|------------|
| **email**      | User's registered email  | `String` | Valid email|
| **password**   | User's password          | `String` | 6-20 chars |

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | `{"message": "Signin successful", "token": "JWT_TOKEN"}` |
| **401**     | `{"error": "Invalid email or password"}`              |
| **403**     | `{"error": "Account not verified. Please verify your OTP."}` |
| **500**     | `{"error": "Server error. Please try again later."}`   |

---

### Example Request

**Headers:**

```http
Content-Type: application/json
