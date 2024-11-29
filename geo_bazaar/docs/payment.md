# Module 8: Checkout and Payments

## Purpose
Facilitates the purchase process by allowing users to confirm their orders, select a delivery address, and choose from various payment options.

## Features
  - Display saved addresses for selection.
  - Option to add a new delivery address during checkout.
  - Cash on Delivery (COD) option.
  - Digital payment methods (e.g., credit/debit cards, UPI, wallets).
  - Display the list of items in the order with quantity and price details.
  - Show total cost, including applicable taxes, discounts, and delivery charges.
  - Allow users to review all details and confirm the order.
  - Generate an order ID for tracking purposes.
  - Secure payment processing for digital payments.


## Dependencies
- Django models for orders, delivery addresses, and payment transactions.
- Integration with payment gateways (e.g., Razorpay, PayPal, Stripe).
- Backend logic for calculating final prices and applying discounts.
- Frontend components for a responsive checkout interface.
- Integration with the shopping cart module for transferring items to the order summary.
