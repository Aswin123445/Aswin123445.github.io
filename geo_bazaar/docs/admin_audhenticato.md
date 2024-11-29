# Module 1: Admin Authentication

## Purpose
Allows administrators to securely sign in and access the platform's admin system for management purposes.

## Features
- **Admin Login:**
  - Secure login system for administrators using email and password.
  - Email verification for first-time login or account activation.
- **Admin Authentication:**
  - Enable secure sign-in to the system with session management to prevent unauthorized access.
  - Support for password reset via email.
- **Basic Account Security:**
  - Notify admins via email for suspicious login attempts.

## Dependencies
- Django's built-in authentication system for admin login/logout functionality.
- Email service for account verification and password resets.
- Middleware for session management and security features.
- Frontend components for the admin login interface (e.g., Bootstrap or React for custom designs).
- (planning to do it as single window one system for every user)

