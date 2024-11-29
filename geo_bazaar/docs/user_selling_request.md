# User Product Selling Request Module

## 4. Request to Sell a Product

### Description
This endpoint allows users to submit a request to sell a product. The request will be sent to the admin for review.

---

### Method: **POST**

**Endpoint**: `/sell-product/request`

---

### Request

| Parameter Name  | Description                              | Type      | Required |
|-----------------|------------------------------------------|-----------|----------|
| **product_name**| Name of the product                      | `String`  | Yes      |
| **category_id** | ID of the category the product belongs to | `Integer` | Yes      |
| **price**       | Selling price proposed by the user        | `Float`   | Yes      |
| **description** | Description of the product               | `String`  | Yes      |
| **location_id** | ID of the location where the product is   | `Integer` | Yes      |
| **images**      | Product images                           | `File[]`  | No       |
| **token**       | User authentication token                | `String`  | Yes      |

---

### Response

| Status Code | Description                                           |
|-------------|-------------------------------------------------------|
| **201**     | `{"message": "Selling request submitted successfully"}` |
| **400**     | `{"error": "Invalid data provided"}`                  |
| **401**     | `{"error": "Unauthorized access, invalid token"}`     |

---


