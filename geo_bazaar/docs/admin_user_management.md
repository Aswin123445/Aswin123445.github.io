# Module 2: Admin User Management

## Purpose
Allows administrators to manage platform users, including viewing user details, tracking activities, and adding new users.

## Features

### **User Listing and Search**
- View a paginated list of all users.
- Search users by:
  - Name
  - Email
  - Role (e.g., Customer, Vendor, Admin)
  - Status (Active/Inactive)

### **User Details**
- View detailed information such as:
  - Name, email, role, account status.
  - Registration date and last login time.
  - Recent activities (e.g., orders, actions).

### **User Activity Log**
- Display user-specific activities like:
  - Login history.
  - Actions performed on the platform.
- Filter activities by date or type.

### **Add New User**
- Create users with fields for:
  - Name, email, password, and role.
- Send account activation emails upon creation.

### **User Account Management**
- Activate/deactivate accounts.
- Reset passwords and send reset links.
- Modify user roles or permissions.

## Dependencies
- Django’s user model for role-based management.
- QuerySet for user listing and search.
- Email service for notifications and account setup.
- Responsive frontend for user management interface.


