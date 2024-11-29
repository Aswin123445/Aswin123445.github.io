# Admin Feedback Module

## 9. Feedback Section

### Description
Allows the admin to view and manage customer feedback. The admin can retrieve all feedback, respond to specific feedback, or delete feedback if necessary.

---

### Method: **GET, POST, DELETE**

---

### 1. **View Feedback**

**Endpoint**: `/admin/feedback`

**Method**: **GET**

---

#### Request

| Parameter Name  | Description                         | Type     | Length |
|-----------------|-------------------------------------|----------|--------|
| **token**       | Admin authentication token          | `String` | N/A    |
| **feedback_id** | (Optional) Specific feedback to view | `Integer`| N/A    |

> **Note:** If `feedback_id` is not provided, all feedback will be retrieved.

---

#### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | Returns feedback data                                 |
| **401**     | `{"error": "Unauthorized access, invalid token"}`     |
| **404**     | `{"error": "Feedback not found"}`                     |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
