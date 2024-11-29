# Contact Module

## 4. Submit Contact Form

### Description
This endpoint allows users to submit inquiries, feedback, or support requests through a contact form.

---

### Method: **POST**

**Endpoint**: `/contact`

---

### Request

| Parameter Name | Description                   | Type      | Required |
|----------------|-------------------------------|-----------|----------|
| **name**       | User's full name              | `String`  | Yes      |
| **email**      | User's email address          | `String`  | Yes      |
| **subject**    | Subject of the message        | `String`  | Yes      |
| **message**    | The message body              | `String`  | Yes      |
| **token**      | (Optional) User authentication token | `String` | No       |

---

### Response

| Status Code | Description                                     |
|-------------|-------------------------------------------------|
| **201**     | `{"message": "Your inquiry has been submitted successfully"}` |
| **400**     | `{"error": "Invalid data provided"}`            |
| **500**     | `{"error": "Internal server error"}`            |

---


