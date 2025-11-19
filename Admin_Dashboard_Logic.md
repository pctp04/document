# 2.0 Admin Dashboard Screen Logic

## Admin Dashboard UI Elements

### Statistics Cards

*   **Total Teachers (stat card)**
    *   Display count of all teachers in system
    *   Show active teachers count with green checkmark icon
    *   Show inactive teachers count with red X icon (if any inactive)
    *   Clicking card could navigate to Teacher Management screen (optional enhancement)

*   **Total Students (stat card)**
    *   Display count of all students in system
    *   Show active students count with green checkmark icon
    *   Show inactive students count with red X icon (if any inactive)
    *   Clicking card could navigate to Student Management screen (optional enhancement)

*   **Total Subjects (stat card)**
    *   Display count of all subjects in system
    *   Show active subjects count with green checkmark icon
    *   Show inactive subjects count with red X icon (if any inactive)
    *   Clicking card could navigate to Subject Management screen (optional enhancement)

*   **Total Curriculums (stat card)**
    *   Display count of all curriculums in system
    *   Show active curriculums count with green checkmark icon
    *   Show inactive curriculums count with red X icon (if any inactive)
    *   Clicking card could navigate to Curriculum Management screen (optional enhancement)

### Grade Distribution Chart

*   **Student Distribution by Grade Level**
    *   Display horizontal bar chart showing student count for each grade level (7, 8, 9, 10)
    *   Each bar shows grade level name and student count
    *   Bars are proportional to the maximum count
    *   Visual representation with percentage-based width

### System Status Panel

*   **System Running Smoothly**
    *   Display green checkmark icon
    *   Show "All services operational" message

*   **Database Connected**
    *   Display blue database icon
    *   Show "Last backup: Today" message

*   **Active Users**
    *   Display green users icon
    *   Show total count of active teachers and students

### Quick Actions

*   **Add New Teacher (button)**
    *   Redirect to `/Admin/Teachers/Create` screen

*   **Add New Student (button)**
    *   Redirect to `/Admin/Students/Create` screen

*   **Add New Subject (button)**
    *   Redirect to `/Admin/Subjects/Create` screen

*   **Create Curriculum (button)**
    *   Redirect to `/Admin/Curriculums/Create` screen

### Navigation

*   **Logout (button)**
    *   Clear session and redirect to `/Admin/Account/Login` screen

