# Product Category Module

## 2. List Products by Category

### Description
This endpoint retrieves a list of products based on the specified category. It allows users to browse products within a particular category.

---

### Method: **GET**

**Endpoint**: `/products/category/{category_id}`

---

### Request

| Parameter Name  | Description                           | Type     | Required |
|-----------------|---------------------------------------|----------|----------|
| **category_id** | ID of the category to filter products | `Integer`| Yes      |
| **token**       | (Optional) User authentication token   | `String` | No       |

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | Returns a list of products in the specified category  |
| **400**     | `{"error": "Invalid category ID"}`                    |
| **404**     | `{"error": "Category not found"}`                     |
| **401**     | `{"error": "Unauthorized access, invalid token"}`     |

---


