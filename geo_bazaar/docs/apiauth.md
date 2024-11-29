# Admin Authentication Module

## 1. Admin Login

### Description
Allows an admin to log in using their username and password.

---

### Method: **POST**

**Endpoint**: `/login`

---

### Request

| Parameter Name | Description        | Type     | Length  |
|----------------|--------------------|----------|---------|
| **username**   | Admin username     | `String` | N/A     |
| **password**   | Admin password     | `String` | N/A     |

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | `"Successfully Login to Admin panel"`                 |
| **501**     | `{"error": "Username and password invalid"}`          |

---

### Example Request

```json
{
  "username": "admin_user",
  "password": "securepassword"
}
