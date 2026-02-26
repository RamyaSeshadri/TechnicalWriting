## Authentication & Authorization

Authentication is role-based and determined using the employee ID (empId) extracted from the access token.

The client only sends the authentication token in the request header. The system retrieves the associated empId from the token and validates the user's role (admin or emp) from the database.

### Authorization Flow
1. Client sends request with Bearer token.
2. System validates token authenticity.
3. empId is extracted from the token.
4. User role (admin/emp) is fetched from the database using empId.
5. Access is granted or denied based on role permissions.

### Role Definitions

| Role  | Permissions |
|--------|-------------|
| admin  | Create, Update, Delete users |
| emp    | Read (GET) user details only |

### Header Example
```

Authorization: Bearer <access_token>

```

> If the authenticated user does not have sufficient privileges, the system returns **403 Forbidden**.

|--------|-------------|
| admin  | Create, Update, Delete users |
| emp    | Read (GET) user details only |

### Header Example

### Header Example
```

Authorization: Bearer <access_token>
X-Employee-Id: EMP12345
X-Role: admin

````

> The system validates the empId and role before processing the request. If the role does not have sufficient privileges, the request is rejected with **403 Forbidden**.

---
