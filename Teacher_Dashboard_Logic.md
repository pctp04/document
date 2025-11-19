# 8.0 Teacher Dashboard Screen Logic

## Teacher Dashboard UI Elements

### Statistics Cards

*   **Assigned Curriculums (stat card)**
    *   Display count of curriculums assigned to logged-in teacher
    *   Shows curriculum cards with details

*   **Total Students (stat card)**
    *   Display total count of students across all assigned curriculums
    *   Aggregated from all curriculums teacher is assigned to

*   **Pending Assignments (stat card)**
    *   Display count of assignments awaiting grading
    *   Shows assignments that have submissions but not yet graded

*   **Recent Messages (stat card)**
    *   Display count of unread messages
    *   Shows messages from students and parents

### Curriculum Overview Cards

*   **Curriculum Card**
    *   Display curriculum name and code
    *   Show statistics: Students count, Average grade, Total grades
    *   Click to navigate to detailed curriculum view
    *   Hover effect with elevation

### Upcoming Classes Section

*   **Class Schedule List**
    *   Display upcoming classes with date and time
    *   Organized by curriculum
    *   Shows class subject and location if available
    *   Highlights classes happening today

### Pending Assignments Section

*   **Assignment List**
    *   Display assignments that need grading
    *   Show assignment title, due date, and submission count
    *   Click to navigate to assignment grading page
    *   Color-coded by urgency (overdue, due soon, normal)

### Recent Messages Section

*   **Message Preview**
    *   Display recent unread messages
    *   Show sender name, subject, and timestamp
    *   Click to navigate to Communication Center
    *   Badge showing unread count

### Quick Actions

*   **Manage Courses Button**
    *   Redirect to `/Teacher/Courses` screen

*   **Manage Assignments Button**
    *   Redirect to `/Teacher/Assignments` screen

*   **Student Performance Button**
    *   Redirect to `/Teacher/Performance` screen

*   **Communication Center Button**
    *   Redirect to `/Teacher/Communication` screen

### Navigation

*   **Logout Button**
    *   Clear session and redirect to `/Teacher/Account/Login` screen

