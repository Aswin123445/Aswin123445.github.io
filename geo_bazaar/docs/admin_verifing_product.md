# Admin Product Validation Module

## 11. Product Validation Form

### Description
This endpoint allows the admin to review the details of a product submitted by a user and validate its authenticity and quality. Admin can approve or reject the product after reviewing.

---

### Method: **GET, POST**

---

### 1. **View Product Validation Form**

**Endpoint**: `/admin/validate-product/{request_id}`

**Method**: **GET**

---

#### Request

| Parameter Name  | Description                         | Type     | Length |
|-----------------|-------------------------------------|----------|--------|
| **token**       | Admin authentication token          | `String` | N/A    |
| **request_id**  | ID of the product selling request   | `Integer`| N/A    |

---

#### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | Returns the product details for validation            |
| **401**     | `{"error": "Unauthorized access, invalid token"}`     |
| **404**     | `{"error": "Product request not found"}`              |

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
