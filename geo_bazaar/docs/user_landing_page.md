# User Landing Page Module

## 1. Landing Page (Homepage)

### Description
This endpoint serves the homepage (landing page) of the website where users can find general information, navigation to other sections, and products or services offered by the platform.

---

### Method: **GET**

**Endpoint**: `/landing-page`

---

### Request

| Parameter Name  | Description                         | Type     | Length |
|-----------------|-------------------------------------|----------|--------|
| **token**       | (Optional) User authentication token | `String` | N/A    |

> **Note:** The `token` parameter is optional for accessing the public landing page, but may be used for personalized content or user-specific data.

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | Returns the content for the homepage                  |
| **401**     | `{"error": "Unauthorized access, invalid token"}`     |
| **404**     | `{"error": "Page not found"}`                          |

---

### Example Request

**Query Parameters:**

```http
GET /landing-page
