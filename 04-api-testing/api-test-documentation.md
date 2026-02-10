# API Testing Documentation (Postman)

## Purpose
API testing ensures backend services function correctly, independently of the UI.

It validates:
- Data correctness
- Status codes
- Authentication
- Error handling
- Integration between services

---

## Tools Used
- Postman
- Newman (CLI execution)
- JSON Assertions
- Environment Variables

---

## Public API Used for Demo
ReqRes API: https://reqres.in/

---

## Key Test Scenarios

---

## 1. GET Users List

### Request
GET `/api/users?page=2`

### Validations
- Status code = 200
- Response contains list of users
- Response time < 1000ms

### Postman Test Script
```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
