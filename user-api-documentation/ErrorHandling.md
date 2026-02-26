# Error Handling Standards

The API follows a structured error response format to ensure consistency and clarity.

---

## Standard Error Response Format

All errors follow this JSON structure:

{
  "errorCode": "ERROR_IDENTIFIER",
  "message": "Human readable error description"
}

---

## HTTP Status Codes Used

### 400 - Bad Request
Returned when input validation fails.

Example:
{
  "errorCode": "INVALID_PHONE",
  "message": "Phone number must contain exactly 10 digits."
}

---

### 401 - Unauthorized
Returned when:
- Bearer token is missing
- Token is invalid
- Token is expired

Example:
{
  "errorCode": "AUTH_REQUIRED",
  "message": "Authentication token is missing or invalid."
}

---

### 403 - Forbidden
Returned when:
- User is authenticated but does not have sufficient privileges

Example:
{
  "errorCode": "ACCESS_DENIED",
  "message": "Admin privileges required to perform this action."
}

---

### 404 - Not Found
Returned when the requested user does not exist.

Example:
{
  "errorCode": "USER_NOT_FOUND",
  "message": "No user found with the provided ID."
}

---

### 500 - Internal Server Error
Returned for unexpected system failures.

Example:
{
  "errorCode": "INTERNAL_ERROR",
  "message": "An unexpected error occurred. Please try again later."
}
