### Scenario 1 – Create New User
- **Method**: POST  
- **Endpoint**: https://gorest.co.in/public/v2/users  
- **Headers**:
  - Authorization: Bearer {{auth_token}}
  - Content-Type: application/json
- **Request Body**:
  - Dynamic email with timestamp is used.
  - Name, Gender, Email, Status (active)
- **Tests**:
  - HTTP status = 201
  - Response `id` is a number

---

### Scenario 2 – Verify First User Status
- **Method**: GET  
- **Endpoint**: https://gorest.co.in/public/v2/users  
- **Tests**:
  - HTTP status = 200
  - First user's `status` is either "active" or "inactive"
