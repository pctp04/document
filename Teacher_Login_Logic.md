# 7.0 Teacher Login Screen Logic

## Teacher Login UI Elements

*   **Username Field**
    *   Text input with user icon on the left
    *   Placeholder: "Enter your username"
    *   Auto-focus on page load
    *   Required field validation
    *   Accepts alphanumeric characters and underscores only

*   **Password Field**
    *   Password input with lock icon on the left
    *   Eye icon on the right to toggle visibility
    *   Placeholder: "Enter your password"
    *   Required field validation
    *   Password strength requirements: minimum 8 characters, must contain uppercase, lowercase, number, and special character

*   **Remember Me Checkbox**
    *   Checkbox with label "Remember me for 30 days"
    *   If checked: session persists for 30 days
    *   If unchecked: session expires in 2 hours

*   **Sign In Button**
    *   Full-width button with gradient background
    *   Text: "Sign In"
    *   Shows loading state ("Signing in...") on form submission
    *   Disabled during submission to prevent double-submission

*   **Theme Toggle Button**
    *   Positioned at top-right corner
    *   Toggles between light and dark mode
    *   Preference saved in browser localStorage
    *   Icon changes between moon (light mode) and sun (dark mode)

*   **Validation Messages**
    *   Display validation errors below each field
    *   Show model-level validation errors at top of form
    *   Red text color for error messages

*   **Form Submission**
    *   On successful login: redirect to `/Teacher/Dashboard`
    *   On failed login: display error message and remain on login page
    *   Clear password field on failed attempt

