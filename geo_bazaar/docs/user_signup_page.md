# User Signup Module

## 2. User Signup

### Description
This endpoint allows a new user to sign up by providing necessary information such as username, email, and password. It registers the user in the system and can optionally send a verification email.

---

### Method: **POST**

**Endpoint**: `/signup`

---

### Request

| Parameter Name  | Description                             | Type     | Length     |
|-----------------|-----------------------------------------|----------|------------|
| **username**    | Username chosen by the user             | `String` | 3-20 chars |
| **phone_number**       | Email address of the user               | `String` | Valid email|
| **password**    | Password for the account                | `String` | 6-20 chars |
| **confirm_password** | Confirmation of the chosen password  | `String` | 6-20 chars |
| **first_name**  | (Optional) User's first name            | `String` | 1-50 chars |
| **last_name**   | (Optional) User's last name             | `String` | 1-50 chars |

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **201**     | `"User successfully registered"`                      |
| **400**     | `{"error": "Bad request. Please check your inputs."}` |
| **409**     | `{"error": "Email or username already exists"}`       |
| **422**     | `{"error": "Password and confirm password do not match"}` |
| **500**     | `{"error": "Server error. Please try again later."}`   |

---

### Example Request

**Headers:**

```http
Content-Type: application/json
