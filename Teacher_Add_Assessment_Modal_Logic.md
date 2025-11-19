# 9.1 Add New Assessment Modal (Teacher) Screen Logic

## Add New Assessment Modal UI Elements

### Modal Header

*   **Modal Title**
    *   "Add New Assessment"
    *   Close button (X) in top-right corner
    *   Clicking outside modal or Cancel button closes modal

### Assessment Information Section

*   **Assessment Title**
    *   Required text input
    *   Maximum 200 characters
    *   Placeholder: "Enter assessment title"
    *   Auto-focus on modal open
    *   Validation: Required, cannot be empty

*   **Assessment Type**
    *   Required dropdown
    *   Options: Quiz, Exam, Assignment, Project, Other
    *   Default: No selection (user must choose)
    *   Validation: Required selection

*   **Subject Selection**
    *   Required dropdown
    *   Shows only subjects assigned to logged-in teacher
    *   Required selection
    *   Updates student list when subject changes
    *   Validation: Required selection

*   **Assessment Date**
    *   Required date input
    *   Date picker component
    *   Default: Today's date
    *   Cannot select future dates
    *   Validation: Required, must be valid date, cannot be future

*   **Description**
    *   Optional textarea
    *   Maximum 500 characters
    *   Placeholder: "Enter assessment description (optional)"
    *   Character counter display
    *   Auto-resize textarea

### Student Selection and Grade Entry Section

*   **Student Selection**
    *   Multi-select checkboxes or select all option
    *   Shows students enrolled in curriculum containing selected subject
    *   "Select All" checkbox for convenience
    *   Required: At least one student must be selected
    *   Validation: Minimum one student required

*   **Bulk Grade Entry Option**
    *   Checkbox: "Apply same grade to all students"
    *   When checked: Single grade input applies to all selected students
    *   When unchecked: Individual grade inputs for each student
    *   Toggle between bulk and individual entry modes

*   **Grade Entry List**
    *   For each selected student, displays:
        *   Student Name
        *   Student ID
        *   Grade Input (0-100, decimal supported)
        *   Remarks Textarea (optional)
    *   Scrollable list if many students
    *   Individual validation per student

*   **Grade Input**
    *   Number input for each student
    *   Range: 0-100
    *   Decimal values supported (e.g., 85.5)
    *   Required for each selected student
    *   Validation: Required, must be between 0-100, numeric only

*   **Remarks Input**
    *   Optional textarea for each student
    *   Maximum 200 characters per student
    *   Character counter per student
    *   Placeholder: "Enter remarks (optional)"

### Modal Footer Actions

*   **Save Button**
    *   Primary button
    *   Text: "Save Assessment"
    *   Validates all required fields before submission
    *   Shows loading state ("Saving...") during submission
    *   Disabled during submission
    *   On success: Closes modal and refreshes Assessment Records Page
    *   Shows success message

*   **Cancel Button**
    *   Secondary button
    *   Text: "Cancel"
    *   Closes modal without saving
    *   Discards all entered data
    *   No confirmation required

### Validation and Error Handling

*   **Field Validation**
    *   Real-time validation as user types
    *   Required fields highlighted if empty
    *   Error messages below each invalid field
    *   Red border on invalid inputs

*   **Form Validation**
    *   Validates on Save button click
    *   Checks all required fields
    *   Validates grade ranges
    *   Ensures at least one student selected
    *   Shows validation summary if errors exist

*   **Error Messages**
    *   Display below each invalid field
    *   Red text color
    *   Clear, specific error messages
    *   Scroll to first error on validation failure

### Data Operations

*   **Create Assessment**
    *   Save assessment with all details
    *   Save grades for all selected students
    *   Save optional remarks for each student
    *   Associate assessment with selected subject
    *   Create assessment record in database

*   **Close Modal**
    *   On successful save: Close modal and refresh parent page
    *   On cancel: Close modal without saving
    *   On error: Keep modal open and show error message

### User Experience

*   **Modal Behavior**
    *   Opens centered on screen
    *   Backdrop overlay (semi-transparent)
    *   Clicking backdrop closes modal (with confirmation if data entered)
    *   ESC key closes modal (with confirmation if data entered)
    *   Smooth open/close animations

*   **Data Persistence**
    *   Optionally save draft as user types (localStorage)
    *   Restore draft if modal reopened before completion
    *   Clear draft on successful save

*   **Success Feedback**
    *   Success message displayed
    *   Modal closes automatically
    *   Assessment Records Page refreshes
    *   New assessment appears in list
    *   Optional: Highlight newly created assessment

