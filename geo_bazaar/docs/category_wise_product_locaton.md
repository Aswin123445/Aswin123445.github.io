# Product Location & Category Module

## 3. List Products by Category and Location

### Description
This endpoint retrieves a list of products within a specified category and location, allowing users to find products available in their region.

---

### Method: **GET**

**Endpoint**: `/products/category/{category_id}/location/{location_id}`

---

### Request

| Parameter Name  | Description                                    | Type     | Required |
|-----------------|------------------------------------------------|----------|----------|
| **category_id** | ID of the category to filter products           | `Integer`| Yes      |
| **location_id** | ID of the location to filter products           | `Integer`| Yes      |
| **token**       | (Optional) User authentication token            | `String` | No       |

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **200**     | Returns a list of products in the specified category and location |
| **400**     | `{"error": "Invalid category or location ID"}`         |
| **404**     | `{"error": "No products found for the given criteria"}`|
| **401**     | `{"error": "Unauthorized access, invalid token"}`     |

---


