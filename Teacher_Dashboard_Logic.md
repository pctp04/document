# 7.0 Teacher Dashboard Screen Logic

## Teacher Dashboard UI Elements

### Statistics Cards

*   **Assigned Subjects (stat card)**
    *   Display count of subjects assigned to logged-in teacher
    *   Shows subject cards with details

*   **Total Students (stat card)**
    *   Display total count of students across all assigned subjects/curriculums
    *   Aggregated from all curriculums containing teacher's subjects

*   **Total Assessments (stat card)**
    *   Display total count of assessments recorded
    *   Shows all assessments across all subjects

*   **Recent Assessments (stat card)**
    *   Display count of assessments created in the last 7 days
    *   Shows recent activity indicator

### Subject Overview Cards

*   **Subject Card**
    *   Display subject name and code
    *   Show statistics: Students count, Assessments count, Average grade
    *   Click to navigate to Subject Information Page (8.0)
    *   Hover effect with elevation

### Upcoming Classes Section

*   **Class Schedule List**
    *   Display upcoming classes with date and time
    *   Organized by subject
    *   Shows class subject and location if available
    *   Highlights classes happening today

### Recent Assessments Section

*   **Assessment List**
    *   Display most recent assessments
    *   Show assessment title, date, and subject
    *   Click to navigate to Assessment Records Page (9.0)
    *   Shows last 5-10 recent assessments

### Quick Actions

*   **Subject Information Button**
    *   Redirect to `/Teacher/Subjects` screen (8.0)
    *   Primary button
    *   Navigate to Subject Information Page

*   **Assessment Records Button**
    *   Redirect to `/Teacher/Assessments` screen (9.0)
    *   Primary button
    *   Navigate to Assessment Records Page

### Navigation

*   **Logout Button**
    *   Clear session and redirect to `/Login` screen (unified login)

