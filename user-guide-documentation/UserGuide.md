# User Guide: User Management Application

## Overview

The User Management Application enables organizations to manage user records securely and efficiently.  

The system supports role-based access:

- **Admin** – Can create, update, and delete users.
- **Employee** – Can view user information only.

Access permissions are automatically determined after login.

---

## Getting Started

### System Requirements

- Web browser (Chrome, Edge, Firefox)
- Active employee credentials
- Internet connection

---

## 1. Logging In

1. Open the application in your browser.
2. Enter your **Employee ID**.
3. Enter your password.
4. Click **Login**.

If login is successful, you will be redirected to the dashboard.

If login fails, verify your credentials or contact your system administrator.

---

## 2. Dashboard Overview

After logging in, the dashboard displays:

- Navigation panel
- User list
- Search bar
- Action buttons (Admin only)

Employees will not see edit or delete options.

---

## 3. Searching for a User

1. Use the **Search bar** at the top of the dashboard.
2. Enter name, email, or phone number.
3. Matching results will appear instantly.

Tip: Search is case-insensitive.

---

## 4. Creating a New User (Admin Only)

1. Click **Add User**.
2. Enter the required details:
   - Name (Minimum 2 characters)
   - Email (example@domain.com format)
   - Phone (10 digits)
   - Gender (Optional)
3. Click **Save**.

If the information passes validation, the user will be added successfully.

If validation fails, an error message will indicate the issue.

---

## 5. Viewing User Details

1. Select a user from the list.
2. Click on the user record.
3. The system displays complete user details.

Employees have read-only access.

---

## 6. Updating User Information (Admin Only)

1. Select the user.
2. Click **Edit**.
3. Update email or phone number.
4. Click **Update**.

Important:
- User ID cannot be modified.
- Invalid email or phone formats will trigger validation errors.

---

## 7. Deleting a User (Admin Only)

1. Select the user.
2. Click **Delete**.
3. Confirm the action.

Warning:
Deleted records cannot be recovered.

---

## Error Messages and Troubleshooting

### Invalid Email
Ensure the email follows this format:
`example@domain.com`

### Invalid Phone Number
Phone number must contain exactly 10 digits.

### Access Denied
Employees attempting admin actions will receive an authorization error.

### Session Expired
If your session expires:
1. Log out.
2. Log in again.

---

## Security Best Practices

- Do not share your login credentials.
- Always log out after completing your session.
- Admin users should verify user information before saving changes.
- Report suspicious activity to your system administrator.

---

## Contact Support

For assistance, contact your system administrator or IT support team.
