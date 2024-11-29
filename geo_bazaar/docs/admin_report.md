# Admin Reports Module

## 13. View Reports

### Description
Allows the admin to view various reports such as sales, orders, customers, and products.

---

### Method: **GET**

**Endpoint**: `/admin/reports`

---

### Request

| Parameter Name  | Description                         | Type     | Length |
|-----------------|-------------------------------------|----------|--------|
| **token**       | Admin authentication token          | `String` | N/A    |
| **report_type** | (Optional) Type of report to view   | `String` | N/A    |
| **start_date**  | (Optional) Start date for the report (YYYY-MM-DD) | `String` | N/A |
| **end_date**    | (Optional) End date for the report (YYYY-MM-DD)   | `String` | N/A |

**Supported `report_type` values:**

- `sales`
- `orders`
- `customers`
- `products`

> **Note:** The `token` should be passed in the request header for authorization. If `report_type` is not provided, a summary report will be returned.

---

### Response

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **200**     | Returns the requested report data                   |
| **401**     | `{"error": "Unauthorized access, invalid token"}`   |
| **400**     | `{"error": "Invalid report type or date range"}`    |
| **404**     | `{"error": "No data found for the selected report"}`|

---

### Example Request

**Headers:**

```http
Authorization: Bearer <admin_token>
