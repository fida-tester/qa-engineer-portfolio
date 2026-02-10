# Boundary Value Analysis (BVA) Examples

## Purpose
Boundary Value Analysis is a test design technique used to test edge conditions.
Defects often occur at the minimum and maximum limits of input ranges.

---

## Example 1: Password Length Validation

### Requirement
Password must be between **8 and 20 characters**

| Test Case | Input Length | Expected Result |
|----------|-------------|----------------|
| BVA-001 | 7 characters | Rejected (too short) |
| BVA-002 | 8 characters | Accepted (minimum valid) |
| BVA-003 | 9 characters | Accepted |
| BVA-004 | 19 characters | Accepted |
| BVA-005 | 20 characters | Accepted (maximum valid) |
| BVA-006 | 21 characters | Rejected (too long) |

---

## Example 2: Product Quantity Limits

### Requirement
User can order between **1 and 10 items**

| Test Case | Quantity | Expected Result |
|----------|----------|----------------|
| BVA-007 | 0 | Error message shown |
| BVA-008 | 1 | Accepted |
| BVA-009 | 5 | Accepted |
| BVA-010 | 10 | Accepted |
| BVA-011 | 11 | Rejected |

---

## Example 3: Age Field Validation

### Requirement
Age must be between **18 and 65**

| Test Case | Age | Expected Result |
|----------|-----|----------------|
| BVA-012 | 17 | Rejected |
| BVA-013 | 18 | Accepted |
| BVA-014 | 30 | Accepted |
| BVA-015 | 65 | Accepted |
| BVA-016 | 66 | Rejected |

---

## Notes
BVA is especially useful for:
- Form validation
- Payment limits
- Quantity/order rules
- Input constraints in business-critical workflows
