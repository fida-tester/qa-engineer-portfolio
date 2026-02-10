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

. GET Single User
Request

GET /api/users/2

Expected Result

User details returned correctly

ID matches request

pm.test("User ID is correct", function () {
    let jsonData = pm.response.json();
    pm.expect(jsonData.data.id).to.eql(2);
});

3. POST Login (Positive)
Request

POST /api/login

Body
{
  "email": "eve.holt@reqres.in",
  "password": "cityslicka"
}

Expected

Status = 200

Token returned

pm.test("Token is returned", function () {
    let jsonData = pm.response.json();
    pm.expect(jsonData.token).to.exist;
});

4. POST Login (Negative)
Body (Missing Password)
{
  "email": "eve.holt@reqres.in"
}

Expected

Status = 400

Proper error message returned

5. DELETE User
Request

DELETE /api/users/2

Expected

Status = 204 No Content

Notes

API testing is essential for:

Microservices validation

Integration testing

Faster regression coverage

Supporting automation frameworks
