# 6.0 Curriculum Management Screen Logic

## Curriculum Management UI Elements

### Filter Section

*   **Search Input**
    *   Real-time search filtering
    *   Searches by curriculum name or curriculum code
    *   Case-insensitive search
    *   Updates results as user types

*   **Grade Level Filter**
    *   Dropdown filter for grade levels
    *   Options: All Grades, Grade 7, Grade 8, Grade 9, Grade 10
    *   Default: "All Grades"

*   **Status Filter**
    *   Dropdown filter for Active/Inactive status
    *   Default: "All Status"
    *   Filters curriculums based on IsActive property

*   **Academic Year Filter**
    *   Dropdown filter for academic years
    *   Shows last 5 years in format YYYY-YYYY
    *   Default: "All Years"

*   **Export Report**
    *   Dropdown button with export options
    *   Formats: PDF, Excel, CSV, Image (JPG)
    *   Exports filtered results only

### Curriculum List Display

*   **Curriculum Card**
    *   Displays curriculum information in card layout
    *   Header section shows: Curriculum Name, Curriculum Code badge, Status badge
    *   Meta information: Academic Year, Semester, Grade Level
    *   Body section shows statistics: Subjects Count, Teachers Count, Students Enrolled Count
    *   Displays description if available
    *   Hover effect with elevation

*   **Statistics Boxes**
    *   Three stat boxes showing:
        *   Subjects: Count of subjects in curriculum
        *   Teachers: Count of unique teachers assigned
        *   Students Enrolled: Count of enrolled students

*   **View Button**
    *   Navigate to `/Admin/Curriculums/Details/{id}`
    *   Blue info button with eye icon

*   **Edit Button**
    *   Navigate to `/Admin/Curriculums/Edit/{id}`
    *   Yellow warning button with edit icon

*   **Delete Button**
    *   Red danger button with trash icon
    *   Opens confirmation modal before deletion
    *   Modal shows curriculum name and warning about associated data removal

### Actions

*   **Create New Curriculum Button**
    *   Navigate to `/Admin/Curriculums/Create`
    *   Primary button in page header

*   **Reset Filters**
    *   Clears all filters and resets to default view
    *   Available in "No Results" empty state

### Empty States

*   **No Curriculums Found**
    *   Displayed when no curriculums exist in system
    *   Shows icon, message, and "Create First Curriculum" button

*   **No Results Match Search**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **Create Curriculum**
    *   Navigate to create form
    *   Form includes: Curriculum Name, Curriculum Code, Academic Year, Semester, Grade Level, Description (optional), Subject-Teacher Assignments, Student Enrollments, Active Status
    *   Subject-Teacher assignments: Add subjects and assign teacher for each
    *   Student enrollments: Multi-select checkboxes for students
    *   At least one subject must be assigned
    *   Curriculum code must be unique and uppercase

*   **Edit Curriculum**
    *   Navigate to edit form with pre-filled data
    *   All fields editable
    *   Can modify subject-teacher assignments and student enrollments
    *   Maintains existing assignments if not changed

*   **Delete Curriculum**
    *   Soft delete (sets IsActive to false) or hard delete
    *   Requires confirmation
    *   Warning about removing associated data (subject assignments, student enrollments)
    *   Shows success/error message after operation

*   **View Details**
    *   Navigate to details page showing full curriculum information
    *   Includes complete list of subjects with assigned teachers
    *   Shows all enrolled students
    *   Displays all metadata and statistics

