# 16.0 Assignment Submission (Student) Screen Logic

## Assignment Submission UI Elements

### Filter Section

*   **Curriculum Filter**
    *   Dropdown filter for curriculums
    *   Shows only curriculums student is enrolled in
    *   Default: "All Curriculums"

*   **Status Filter**
    *   Dropdown filter by assignment status
    *   Options: All Status, Not Started, In Progress, Submitted, Graded
    *   Default: "All Status"

*   **Search Input**
    *   Real-time search filtering
    *   Searches by assignment title
    *   Case-insensitive search

### Assignment List Display

*   **Assignment Card**
    *   Displays assignment information in card layout
    *   Shows: Title, Description (truncated), Curriculum, Due Date, Status badge
    *   Days Until Due: Color-coded (red if overdue, yellow if due soon, green if plenty of time)
    *   Hover effect with elevation

*   **Status Badges**
    *   Not Started: Gray badge
    *   In Progress: Blue badge
    *   Submitted: Green badge
    *   Graded: Purple badge with grade displayed

*   **View Assignment Button**
    *   Navigate to assignment detail view
    *   Blue info button
    *   View full assignment details and instructions

*   **Submit Assignment Button**
    *   Opens submission form
    *   Primary button
    *   Only available if assignment not yet submitted or can be edited
    *   Disabled if assignment is closed or graded

### Assignment Detail View

*   **Assignment Information**
    *   Display full assignment title and description
    *   Show curriculum name and code
    *   Display due date and time
    *   Show days until due (or overdue indicator)

*   **Assignment Files**
    *   List of files attached by teacher
    *   Download button for each file
    *   Shows file name and size

*   **Submission Form**
    *   File upload input for submission files
    *   Multiple files supported
    *   Accepted formats: PDF, DOC, DOCX, images, ZIP
    *   Maximum file size: 10MB per file
    *   Shows list of selected files
    *   Submit button

*   **Validation**
    *   Prevents submission after due date
    *   Requires at least one file
    *   Validates file types and sizes
    *   Shows error messages for invalid submissions

### Submission History

*   **Submitted Assignment Display**
    *   Shows submission date and time
    *   Lists all submitted files with download links
    *   Displays grade received (if graded)
    *   Shows teacher feedback/comments

*   **Grade Display**
    *   Shows grade in large, prominent format
    *   Color-coded by grade level (A: green, B: blue, C: yellow, D/F: red)
    *   Shows letter grade equivalent if applicable

*   **Teacher Feedback**
    *   Display teacher's comments
    *   Formatted text area
    *   Shows feedback date

*   **Edit Submission Button**
    *   Allows editing submission before due date
    *   Only available if assignment not yet graded
    *   Replaces existing submission
    *   Shows warning about replacing previous submission

### Data Operations

*   **View Assignment**
    *   Display assignment details
    *   Download assignment files
    *   View instructions and requirements

*   **Submit Assignment**
    *   Upload submission files
    *   Validate files before submission
    *   Submit before due date
    *   Confirmation message on successful submission
    *   Status changes to "Submitted"

*   **Edit Submission**
    *   Replace existing submission
    *   Only allowed before due date and if not graded
    *   Removes previous files
    *   Uploads new files

*   **View Submission**
    *   View submitted files
    *   Download submitted files
    *   View grade and feedback (if graded)

### Notifications

*   **Submission Confirmation**
    *   Success message after submission
    *   Confirms files uploaded
    *   Shows submission date and time

*   **Grade Notification**
    *   Notification when assignment is graded
    *   Shows grade received
    *   Highlights if grade is available

*   **Due Date Reminders**
    *   Warning for assignments due soon
    *   Alert for overdue assignments
    *   Color-coded indicators

