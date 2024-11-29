# Module 5: Delivery Partner Management

## Purpose
Allows administrators to manage delivery partners, assign orders efficiently, and track order progress to ensure timely deliveries.

## Features
- **Delivery Partner Management:**
  - Add new delivery partners with details such as:
    - Name, contact information, location, and ID proof.
  - Update delivery partner information.
  - Activate or deactivate delivery partner accounts.

- **Order Assignment:**
  - Assign specific orders to delivery partners based on:
    - Location proximity.

- **Order Tracking:**
  - Monitor the status of all orders in real-time:
    - Pending, dispatched, out for delivery, delivered, or returned.
  - View detailed order tracking, including timestamps for each delivery stage.
  - assign task to verify the product requested by user to sell 

- **Performance Monitoring:**
  - Track delivery partner performance metrics, such as:
    - Number of orders completed.
    - Average delivery time.
    - Delivery success rates.
  - Identify top-performing and underperforming delivery partners for feedback or rewards.

- **Reports:**
  - Generate reports on delivery operations, including:
    - Completed and pending deliveries.
    - Delivery times and delays.
    - Partner-specific performance analysis.

## Dependencies
- Django models for storing delivery partner and order data.
- Frontend components for an admin dashboard interface 
- Backend logic for assigning orders and managing delivery workflows.
