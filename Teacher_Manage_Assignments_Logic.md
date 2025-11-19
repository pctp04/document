# 10.0 Manage Assignments (Teacher) Screen Logic

## Manage Assignments UI Elements

### Filter Section

*   **Curriculum Filter**
    *   Dropdown filter for curriculums
    *   Shows only curriculums assigned to logged-in teacher
    *   Default: "All Curriculums"

*   **Status Filter**
    *   Dropdown filter for assignment status
    *   Options: All Status, Draft, Published, Closed
    *   Default: "All Status"

*   **Search Input**
    *   Real-time search filtering
    *   Searches by assignment title or description
    *   Case-insensitive search

### Assignment List Display

*   **Assignment Card**
    *   Displays assignment information in card layout
    *   Shows: Title, Description (truncated), Due Date, Curriculum, Status badge
    *   Statistics: Submissions Count, Total Students, Graded Count
    *   Progress indicator showing submission percentage
    *   Hover effect with elevation

*   **Create Assignment Button**
    *   Navigate to `/Teacher/Assignments/Create`
    *   Primary button in page header
    *   Opens form to create new assignment

*   **Edit Assignment Button**
    *   Navigate to `/Teacher/Assignments/Edit/{id}`
    *   Yellow warning button
    *   Only available for Draft status assignments

*   **View Submissions Button**
    *   Navigate to `/Teacher/Assignments/{id}/Submissions`
    *   Blue info button
    *   View all student submissions for assignment

*   **Publish Button**
    *   Changes assignment status from Draft to Published
    *   Green success button
    *   Makes assignment visible to students
    *   Requires confirmation

*   **Close Assignment Button**
    *   Changes assignment status to Closed
    *   Red danger button
    *   Prevents new submissions
    *   Requires confirmation

*   **Delete Assignment Button**
    *   Delete assignment permanently
    *   Red danger button
    *   Only available for Draft status
    *   Requires confirmation modal

### Create/Edit Assignment Form

*   **Assignment Title**
    *   Required text input
    *   Maximum 200 characters
    *   Placeholder: "Enter assignment title"

*   **Assignment Description**
    *   Optional textarea
    *   Maximum 1000 characters
    *   Rich text editor support (optional)

*   **Due Date**
    *   Required datetime input
    *   Date and time picker
    *   Must be in the future
    *   Validation prevents past dates

*   **Curriculum Selection**
    *   Required dropdown
    *   Shows only curriculums assigned to teacher
    *   Pre-selected if navigated from curriculum page

*   **Attached Files**
    *   File upload input
    *   Multiple files supported
    *   Accepted formats: PDF, DOC, DOCX, images
    *   Maximum file size: 10MB per file

*   **Status**
    *   Default: Draft
    *   Can be changed to Published on save
    *   Or saved as Draft for later editing

### Submission Management

*   **View Submissions**
    *   List of all student submissions
    *   Shows: Student Name, Submission Date, Files, Status (Submitted/Graded)
    *   Filter by status (Submitted, Graded, Missing)
    *   Sort by name, date, or grade

*   **Grade Submission**
    *   Input grade (numeric or letter)
    *   Textarea for feedback/comments
    *   Save grade and feedback
    *   Notification sent to student when graded

### Data Operations

*   **Create Assignment**
    *   Create new assignment with all details
    *   Assign to selected curriculum
    *   Automatically visible to all students in curriculum
    *   Status set to Draft by default

*   **Edit Assignment**
    *   Modify assignment details
    *   Only allowed for Draft status
    *   Published assignments cannot be edited (only closed)

*   **Publish Assignment**
    *   Change status from Draft to Published
    *   Makes assignment visible to students
    *   Sends notification to students
    *   Cannot be unpublished

*   **Close Assignment**
    *   Change status to Closed
    *   Prevents new submissions
    *   Existing submissions can still be graded
    *   Cannot be reopened

*   **Delete Assignment**
    *   Permanently delete assignment
    *   Only allowed for Draft status
    *   Deletes all associated submissions
    *   Requires confirmation

