# Admin Selling Requests Module

## 10. View New Product Selling Requests

### Description
Allows the admin to view and manage new product selling requests submitted by users. Admin can review, approve, or reject the requests.

---

### Method: **GET**

**Endpoint**: `/admin/selling-requests`

---

### Request

| Parameter Name  | Description                         | Type     | Length |
|-----------------|-------------------------------------|----------|--------|
| **token**       | Admin authentication token          | `String` | N/A    |
| **request_id**  | (Optional) Specific request to view | `Integer`| N/A    |

> **Note:** If `request_id` is not provided, all pending selling requests will be listed.

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | Returns the list of selling requests                  |
| **401**     | `{"error": "Unauthorized access, invalid token"}`     |
| **404**     | `{"error": "No selling requests found"}`              |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
