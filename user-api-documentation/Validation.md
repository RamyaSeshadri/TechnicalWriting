
# Validation Rules

This document defines validation standards enforced by the User Management API.

---

# Input Validation Rules

| Field    | Validation Rules                     |
|----------|------------------------------------|
| name     | Required, string,min 2 characters, max 50 characters, Alphabets and spaces only |
| address  | Required, string, max 200 characters|
| phone    | Required, valid international format,Must contain 10 digits, Numeric values only|
| email    | Required, valid email format, Unique|
| gender   | Optional, values: Male, Female, Other |
| ID       | System generated, cannot be modified |

---

## 2. Update Restrictions

- Only email and phone can be updated.
- ID updates are not allowed.
- Partial updates must still follow validation rules.

---

If validation fails, the API returns:

Status Code: 400 Bad Request

Example:

{
  "errorCode": "INVALID_EMAIL",
  "message": "The provided email format is invalid."
}
