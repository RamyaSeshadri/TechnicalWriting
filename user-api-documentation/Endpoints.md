## 1. Create User (Admin Only)
- **POST /users**
- **Access:** Admin
- **Description:** Adds a new user to the system.

### Request Body
```json
{
  "name": "John Doe",
  "address": "123 Main St, City, Country",
  "phone": "+911234567890",
  "email": "john.doe@example.com",
  "gender": "Male"
}
````

### Success Response (201 Created)

```json
{
  "id": 101,
  "message": "User created successfully"
}
```

### Error Responses

**400 Bad Request – Invalid Email**

```json
{
  "errorCode": "INVALID_EMAIL_FORMAT",
  "message": "The email address provided is not in a valid format."
}
```

**400 Bad Request – Invalid Phone**

```json
{
  "errorCode": "INVALID_PHONE_FORMAT",
  "message": "Phone number must be in valid international format (e.g., +91XXXXXXXXXX)."
}
```

**401 Unauthorized**

```json
{
  "errorCode": "UNAUTHORIZED",
  "message": "Authentication token is missing or invalid."
}
```

---

## 2. Get User

* **GET /users/{id}**
* **Access:** Authenticated Users
* **Description:** Fetch details of a user by ID.

### Success Response (200 OK)

```json
{
  "id": 101,
  "name": "John Doe",
  "address": "123 Main St, City, Country",
  "phone": "+911234567890",
  "email": "john.doe@example.com",
  "gender": "Male"
}
```

**404 Not Found**

```json
{
  "errorCode": "USER_NOT_FOUND",
  "message": "No user found with the provided ID."
}
```

---

## 3. Update User (Admin Only)

* **PUT /users/{id}**
* **Access:** Admin
* **Description:** Updates existing user details (ID is immutable).

### Request Body

```json
{
  "name": "John Doe",
  "address": "456 Park Avenue",
  "phone": "+919876543210",
  "email": "john.updated@example.com",
  "gender": "Male"
}
```

### Success Response (200 OK)

```json
{
  "id": 101,
  "message": "User updated successfully"
}
```

### Error Responses

**400 Bad Request – Validation Failure**

```json
{
  "errorCode": "VALIDATION_ERROR",
  "message": "One or more fields failed validation checks."
}
```

**401 Unauthorized**

```json
{
  "errorCode": "UNAUTHORIZED",
  "message": "Admin privileges required to perform this operation."
}
```

**404 Not Found**

```json
{
  "errorCode": "USER_NOT_FOUND",
  "message": "No user found with the provided ID."
}
```

---

## 4. Delete User (Admin Only)

* **DELETE /users/{id}**
* **Access:** Admin
* **Description:** Removes a user from the system.

### Success Response (200 OK)

```json
{
  "message": "User deleted successfully"
}
```

**401 Unauthorized**

```json
{
  "errorCode": "UNAUTHORIZED",
  "message": "Admin privileges required to perform this operation."
}
```

**404 Not Found**

```json
{
  "errorCode": "USER_NOT_FOUND",
  "message": "No user found with the provided ID."
}
```

````
