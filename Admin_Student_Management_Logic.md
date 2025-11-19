# 4.0 Student Management Screen Logic

## Student Management UI Elements

### Filter Section

*   **Search Input**
    *   Real-time search filtering
    *   Searches by student name
    *   Case-insensitive search
    *   Updates results as user types

*   **Grade Level Filter**
    *   Dropdown filter for grade levels
    *   Options: All Grades, Grade 7, Grade 8, Grade 9, Grade 10
    *   Default: "All Grades"

*   **Status Filter**
    *   Dropdown filter for Active/Inactive status
    *   Default: "All Status"
    *   Filters students based on IsActive property

*   **Sort By**
    *   Dropdown to sort students
    *   Options: Name (A-Z), Name (Z-A), Grade Level (Low to High), Grade Level (High to Low), Age (Low to High), Age (High to Low)
    *   Default: Name (A-Z)

*   **Items Per Page**
    *   Controls pagination size
    *   Options: 6, 12, 24, Show All
    *   Default: 12

*   **Export Report**
    *   Dropdown button with export options
    *   Formats: PDF, Excel, CSV, Image (JPG)
    *   Exports filtered results only

### Student List Display

*   **Student Card**
    *   Displays student information in list view
    *   Shows profile picture (or placeholder icon with graduation cap)
    *   Displays: Full Name, Grade Level, ID, Age, Address
    *   Shows Active/Inactive status badge
    *   Hover effect with elevation

*   **View Button**
    *   Navigate to `/Admin/Students/Details/{id}`
    *   Blue info button with eye icon

*   **Edit Button**
    *   Navigate to `/Admin/Students/Edit/{id}`
    *   Yellow warning button with edit icon

*   **Delete Button**
    *   Red danger button with trash icon
    *   Opens confirmation modal before deletion
    *   Modal shows student name and warning message

### Actions

*   **Add New Student Button**
    *   Navigate to `/Admin/Students/Create`
    *   Primary button in page header

*   **Reset Filters**
    *   Clears all filters and resets to default view
    *   Available in "No Results" empty state

### Pagination

*   **Page Navigation**
    *   Shows page numbers with ellipsis for large page counts
    *   Previous and Next buttons
    *   Current page highlighted
    *   Disabled state for first/last page

### Empty States

*   **No Students Found**
    *   Displayed when no students exist in system
    *   Shows icon, message, and "Add First Student" button

*   **No Results Match Search**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **Create Student**
    *   Navigate to create form
    *   Form includes: First Name, Middle Name, Last Name, Date of Birth, Grade Level, Address, Profile Picture, Active Status
    *   Age calculated automatically from date of birth

*   **Edit Student**
    *   Navigate to edit form with pre-filled data
    *   All fields editable except Student ID

*   **Delete Student**
    *   Soft delete (sets IsActive to false) or hard delete
    *   Requires confirmation
    *   Shows success/error message after operation

*   **View Details**
    *   Navigate to details page showing full student information
    *   Includes enrolled curriculums if any

