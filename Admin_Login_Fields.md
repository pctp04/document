# 1.0 Login Screen Fields (Unified Role-Based)

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Username | string | 1 | 100 | Text Input | Yes | - | - | `admin`, `teacher01`, `student01` | Username field with user icon. Accepts alphanumeric characters and underscores. Auto-focus on page load. Works for Admin, Teacher, and Student roles. |
| 2 | Password | string | 8 | 100 | Password Input | Yes | - | - | `********` | Password field with lock icon. Hidden by default with toggle visibility button. Must contain at least one uppercase, one lowercase, one number, and one special character. Works for all user roles. |
| 3 | Remember Me | boolean | - | - | Checkbox | No | false | - | `checked` | Checkbox to remember user for 30 days. If unchecked, session expires in 2 hours. Applies to all user roles. |
| 4 | Sign In Button | - | - | - | Button | - | - | - | - | Submit button to authenticate user. Shows loading state during submission. System determines user role and redirects accordingly. |
| 5 | Theme Toggle | - | - | - | Button | - | - | - | - | Button to toggle between light and dark mode. Positioned at top-right corner. |

