# Regression Test Suite – E-Commerce Application

## Purpose
This regression suite covers business-critical flows impacted frequently by releases (auth, cart, checkout, payment, orders).  
It is designed to be executed every sprint and before production releases.

---

## Coverage Areas
- Authentication & Session Management
- Product Listing / Search / Filters
- Cart & Pricing
- Checkout & Address Validation
- Payments (success/failure/retry)
- Order Creation & Confirmation
- Notifications (email)
- Basic Accessibility / UI sanity
- Cross-browser sanity (Chrome/Firefox/Edge)

---

## Regression Test Suite (High Priority)

| ID | Area | Scenario | Expected Result |
|---|---|---|---|
| REG-001 | Auth | Login → logout → back button | User remains logged out, no access to protected pages |
| REG-002 | Auth | Session timeout while idle | User redirected to login, cart state handled correctly |
| REG-003 | Search | Search with special characters (e.g. `!@#`) | App handles input safely, shows “no results” or validation |
| REG-004 | Filters | Apply multiple filters + sort | Results consistent, no duplicates/missing items |
| REG-005 | Cart | Add same item twice | Quantity increases correctly, price totals accurate |
| REG-006 | Cart | Remove item when cart has discounts | Totals recalculated correctly, discount rules correct |
| REG-007 | Pricing | VAT / tax calculation by country | Correct tax rules applied based on shipping country |
| REG-008 | Checkout | Address: long text + special chars | Validation works, accepted format stored correctly |
| REG-009 | Checkout | Change address at last step | Shipping cost recalculated correctly |
| REG-010 | Payment | Payment success | Order created once, confirmation shown |
| REG-011 | Payment | Payment failure | Order not created, error shown, user can retry |
| REG-012 | Payment | Retry payment after timeout | No duplicate orders, single transaction recorded |
| REG-013 | Orders | Order history shows latest order | Correct status, amount, and items displayed |
| REG-014 | Email | Confirmation email content | Correct order ID, items, price, delivery address |
| REG-015 | UI | Responsive layout checkout (mobile) | No broken UI, buttons visible, fields usable |
| REG-016 | Browser | Cross-browser checkout sanity | Core flow works on Chrome/Firefox/Edge |

---

## Execution Notes
- Run Smoke suite on every deployment to QA.
- Run full regression before release.
- Log defects with clear severity + priority and link test case ID (e.g., REG-012).
