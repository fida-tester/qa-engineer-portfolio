# Jira Bug Report Examples

These are professional defect reports written in a Jira-style format.

---

## BUG-101: Duplicate Order Created After Payment Retry

**Module:** Checkout / Payments  
**Severity:** Critical  
**Priority:** P0 (Immediate Fix Required)  
**Environment:** QA, Chrome, Windows 11  

### Preconditions
- User has items in cart
- User is on payment screen

### Steps to Reproduce
1. Proceed to checkout  
2. Enter valid payment details  
3. Simulate payment timeout  
4. Click "Retry Payment"  

### Actual Result
Two separate orders are created for the same transaction.

### Expected Result
Only one order should be created per payment attempt.

### Notes
Possible missing idempotency check on backend payment service.

---

## BUG-102: Discount Code Still Applied After Removing Eligible Product

**Module:** Cart / Promotions  
**Severity:** Major  
**Priority:** P1  

### Steps
1. Add promotional product to cart  
2. Apply discount code  
3. Remove promotional product  
4. Observe cart total  

### Actual Result
Discount remains active even though product is removed.

### Expected Result
Discount should be removed automatically.

---

## BUG-103: User Session Not Expired After Logout

**Module:** Authentication  
**Severity:** Major  
**Priority:** P1  

### Steps
1. Login successfully  
2. Click Logout  
3. Press browser Back button  

### Actual Result
User can still access account dashboard.

### Expected Result
User should be redirected to login page.

---

## BUG-104: Address Field Accepts Unsupported Characters

**Module:** Checkout Form Validation  
**Severity:** Minor  
**Priority:** P2  

### Steps
1. Go to shipping address page  
2. Enter only symbols: `@@@@@@`  
3. Click Continue  

### Actual Result
Form accepts invalid address.

### Expected Result
Validation error should be displayed.

---

## BUG-105: API Returns 200 OK for Invalid User ID

**Module:** API / User Service  
**Severity:** Major  
**Priority:** P1  

### Steps
1. Send GET request: `/api/users/999999`  
2. Observe response  

### Actual Result
Response status = 200 with empty body.

### Expected Result
Response should return 404 Not Found.

---

## Notes
These defects demonstrate real-world QA scenarios involving:
- Payments
- Promotio
