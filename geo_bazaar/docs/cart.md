# Module 6: Shopping Cart

## Purpose
Manages selected products, allowing users to review, update quantities, and proceed to checkout while providing options for applying promo codes or coupons.

## Features
- Display selected products with:
  - Product name, image, and price.
  - Quantity selector for each product.
  - Subtotal calculation for each product based on quantity.
- Show the total cost of all selected products.
- Provide an input field for applying promo codes or coupons.
  - Validate promo codes and apply discounts dynamically.
- Allow users to remove items from the cart.
- Display estimated taxes and shipping charges (if applicable).
- Include a "Proceed to Checkout" button for the next step in the purchase process.

## Dependencies
- Django models for managing cart items and promo codes.
- Frontend components for a dynamic cart interface (e.g., Bootstrap, React).
- Backend logic for applying discounts and recalculating the total cost.
- Integration with the product details page and checkout module.
