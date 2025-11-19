# 14.0 Student Dashboard Screen Logic

## Student Dashboard UI Elements

### Statistics Cards

*   **Enrolled Curriculums (stat card)**
    *   Display count of curriculums student is enrolled in
    *   Shows curriculum cards with details

*   **Pending Assignments (stat card)**
    *   Display count of assignments not yet submitted
    *   Shows assignments with due dates approaching
    *   Highlights overdue assignments

*   **Recent Messages (stat card)**
    *   Display count of unread messages
    *   Shows messages from teachers

*   **Overall Grade Average (stat card)**
    *   Display average grade across all enrolled curriculums
    *   Shows percentage and letter grade equivalent
    *   Color-coded by performance level

### Enrolled Curriculums Section

*   **Curriculum Card**
    *   Display curriculum name and code
    *   Show: Academic Year, Semester, Grade Level
    *   Click to navigate to curriculum details
    *   Hover effect with elevation

### Upcoming Assignments Section

*   **Assignment List**
    *   Display upcoming assignments with due dates
    *   Show: Assignment Title, Due Date, Status, Days Until Due
    *   Color-coded by urgency (overdue: red, due soon: yellow, normal: green)
    *   Click to navigate to assignment submission page
    *   Badge showing status

*   **Assignment Status Badges**
    *   Not Started: Gray badge
    *   In Progress: Blue badge
    *   Submitted: Green badge
    *   Graded: Purple badge with grade displayed

### Attendance Summary Section

*   **Attendance Overview**
    *   Display overall attendance percentage
    *   Show breakdown: Present Days, Absent Days
    *   Progress bar visualization
    *   Color-coded by percentage (Green: >90%, Yellow: 75-90%, Red: <75%)

### Recent Messages Section

*   **Message Preview**
    *   Display recent unread messages
    *   Show sender name (teacher), subject, and timestamp
    *   Click to navigate to Messaging Center
    *   Badge showing unread count

### Quick Actions

*   **Course Materials Button**
    *   Redirect to `/Student/Materials` screen

*   **Assignment Submission Button**
    *   Redirect to `/Student/Assignments` screen

*   **Attendance Record Button**
    *   Redirect to `/Student/Attendance` screen

*   **Messaging Center Button**
    *   Redirect to `/Student/Messages` screen

### Navigation

*   **Logout Button**
    *   Clear session and redirect to `/Student/Account/Login` screen

