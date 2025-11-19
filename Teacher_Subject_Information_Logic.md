# 8.0 Subject Information Page (Teacher) Screen Logic

## Subject Information UI Elements

### Filter Section

*   **Search Input**
    *   Real-time search filtering
    *   Searches by subject name or subject code
    *   Case-insensitive search
    *   Updates results as user types

*   **Subject Filter**
    *   Dropdown filter for subjects
    *   Shows all subjects assigned to logged-in teacher
    *   Default: "All Subjects"

*   **Curriculum Filter**
    *   Dropdown filter for curriculums
    *   Shows curriculums where teacher is assigned
    *   Default: "All Curriculums"
    *   Filters subjects by their associated curriculum

### Subject List Display

*   **Subject Card**
    *   Displays subject information in card layout
    *   Header shows: Subject Code badge, Subject Name
    *   Description: Subject description if available
    *   Curriculum Information: Curriculum Name, Code, Academic Year, Semester, Grade Level
    *   Statistics: Enrolled Students Count
    *   Class Schedule: Display if available
    *   Hover effect with elevation

*   **View Students Button**
    *   Navigate to student list view for this subject
    *   Blue info button
    *   Shows all students enrolled in the curriculum that includes this subject
    *   Displays student names, IDs, and basic information

*   **View Assessment Records Button**
    *   Navigate to Assessment Records Page (9.0) filtered by this subject
    *   Primary button
    *   Opens Assessment Records with subject filter pre-applied
    *   Shows all assessments for this subject

### Empty States

*   **No Subjects Assigned**
    *   Displayed when teacher has no assigned subjects
    *   Shows icon, message, and contact admin information

*   **No Results Match Search**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **View Subject Details**
    *   Display complete subject information
    *   Show curriculum context
    *   Display enrolled students count
    *   Show class schedule if available

*   **View Student List**
    *   Display all students enrolled in curriculum containing this subject
    *   Show student names, IDs, and basic information
    *   Link to individual student details if available

*   **Navigate to Assessments**
    *   Open Assessment Records Page
    *   Pre-filter by selected subject
    *   Show all assessments related to this subject

