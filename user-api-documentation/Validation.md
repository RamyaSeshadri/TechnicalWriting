
# Validation Rules

This document defines validation standards enforced by the User Management API.

---

# Input Validation Rules

| Field    | Validation Rules                     |
|----------|------------------------------------|
| name     | Required, string, max 50 characters |
| address  | Required, string, max 200 characters|
| phone    | Required, valid international format|
| email    | Required, valid email format        |
| gender   | Optional, values: Male, Female, Other |

## 1. Field-Level Validation

### Name
- Required field
- Minimum 2 characters
- Maximum 50 characters
- Alphabets and spaces only

### Address
- Required field
- Maximum 200 characters
- 
### Phone
- Required field
- Must contain exactly 10 digits
- Numeric values only
- No special characters or spaces

### Email
- Required field
- Must follow standard email format
- Example: user@example.com
- Must be unique in the system
### Gender
- Optional field
- Allowed values: Male, Female, Other

### ID
- System generated
- Cannot be modified
- Update requests attempting to modify ID will be rejected

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
  "errorCode": "INVALID_EMAIL",
  "message": "The provided email format is invalid."
}
