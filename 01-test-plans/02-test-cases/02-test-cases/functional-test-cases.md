# Functional Test Cases – E-Commerce Application

## Module: User Authentication + Product Purchase Flow

---

## Test Cases

| ID | Scenario | Steps | Expected Result | Priority |
|----|----------|------|----------------|----------|
| FT-001 | Login with valid credentials | Enter valid email + password → Click Login | User is logged in and redirected to dashboard | High |
| FT-002 | Login with invalid password | Enter valid email + wrong password → Login | Error message displayed, login denied | High |
| FT-003 | Login with empty fields | Leave email/password empty → Login | Validation messages shown | Medium |
| FT-004 | Search product by name | Enter product name in search bar | Correct products displayed | High |
| FT-005 | Apply category filter | Select category filter | Product list updates correctly | Medium |
| FT-006 | Add product to cart | Click “Add to Cart” on product page | Product added with correct quantity and price | High |
| FT-007 | Update cart quantity | Increase quantity in cart | Total price updates correctly | High |
| FT-008 | Remove item from cart | Click “Remove” button | Product removed successfully | Medium |
| FT-009 | Checkout with valid details | Proceed to checkout → Enter shipping info → Confirm | Order placed successfully | High |
| FT-010 | Checkout with missing address | Leave address blank → Continue | Error shown, user cannot proceed | High |
| FT-011 | Payment with invalid card | Enter invalid card details → Pay | Payment rejected with proper error | High |
| FT-012 | Order confirmation email | Complete purchase successfully | Confirmation email is sent to user | Medium |

---

## Notes
These test cases cover core business-critical flows and are designed for regression execution in Agile releases.
