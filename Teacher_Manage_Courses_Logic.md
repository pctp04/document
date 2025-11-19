# 9.0 Manage Courses (Teacher) Screen Logic

## Manage Courses UI Elements

### Filter Section

*   **Search Input**
    *   Real-time search filtering
    *   Searches by curriculum name or curriculum code
    *   Case-insensitive search
    *   Updates results as user types

*   **Academic Year Filter**
    *   Dropdown filter for academic years
    *   Shows available academic years for teacher's curriculums
    *   Default: "All Years"

*   **Grade Level Filter**
    *   Dropdown filter for grade levels
    *   Options: All Grades, Grade 7, Grade 8, Grade 9, Grade 10
    *   Default: "All Grades"

### Curriculum List Display

*   **Curriculum Card**
    *   Displays curriculum information in card layout
    *   Header shows: Curriculum Name, Curriculum Code badge
    *   Meta information: Academic Year, Semester, Grade Level
    *   Statistics: Subjects Count, Students Count
    *   Hover effect with elevation

*   **View Course Materials Button**
    *   Navigate to `/Teacher/Courses/{id}/Materials`
    *   Blue info button
    *   View available course materials and resources

*   **View Students Button**
    *   Navigate to `/Teacher/Courses/{id}/Students`
    *   Blue info button
    *   View list of enrolled students

*   **Manage Assignments Button**
    *   Navigate to `/Teacher/Assignments?curriculumId={id}`
    *   Primary button
    *   Manage assignments for this curriculum

*   **View Performance Button**
    *   Navigate to `/Teacher/Performance?curriculumId={id}`
    *   Primary button
    *   View student performance for this curriculum

### Empty States

*   **No Curriculums Assigned**
    *   Displayed when teacher has no assigned curriculums
    *   Shows icon, message, and contact admin information

*   **No Results Match Search**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **View Course Details**
    *   Navigate to detailed curriculum view
    *   Shows all subjects, enrolled students, and statistics

*   **Access Course Materials**
    *   View and manage course materials
    *   Upload, download, and organize materials by subject

*   **View Student List**
    *   Display all students enrolled in curriculum
    *   Shows student names, IDs, and basic information
    *   Link to individual student performance

