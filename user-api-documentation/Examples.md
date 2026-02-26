# API Usage Examples

This document provides example requests and responses for the User Management API.

Base URL:
`/api/v1/users`

---

## 1️⃣ Create User (Admin Only)

### Request

**POST** `/api/v1/users`

**Headers**
Authorization: Bearer <token>

**Request Body**
```json
{
  "name": "Ram Kumar",
  "email": "ram.kumar@example.com",
  "phone": "9876543210",
  "gender": "Male"
}
```

### Success Response

**Status Code:** 201 Created

```json
{
  "id": 101,
  "name": "Ram Kumar",
  "email": "ram.kumar@example.com",
  "phone": "9876543210",
  "gender": "Male"
}
```

---

## 2️⃣ Get User (Admin / Employee)

### Request

**GET** `/api/v1/users/101`

**Headers**
Authorization: Bearer <token>

### Success Response

**Status Code:** 200 OK

```json
{
  "id": 101,
  "name": "Ram Kumar",
  "email": "ram.kumar@example.com",
  "phone": "9876543210",
  "gender": "Male"
}
```

---

## 3️⃣ Update User Email or Phone (Admin Only)

### Request

**PUT** `/api/v1/users/101`

**Headers**
Authorization: Bearer <token>

**Request Body**
```json
{
  "email": "ram.new@example.com",
  "phone": "9123456789"
}
```

### Success Response

**Status Code:** 200 OK

```json
{
  "message": "User updated successfully."
}
```

---

## Notes

- Role is derived from the database using empId extracted from the token.
- ID modification is not allowed.
- Only Admin users can create, update, or delete users.
- Employees have read-only access.
