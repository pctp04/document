# 3.0 Teacher Management Screen Logic

## Teacher Management UI Elements

### Filter Section

*   **Search Input**
    *   Real-time search filtering
    *   Searches by teacher name, username, or assigned subject codes
    *   Case-insensitive search
    *   Updates results as user types

*   **Status Filter**
    *   Dropdown filter for Active/Inactive status
    *   Default: "All Status"
    *   Filters teachers based on IsActive property

*   **Sort By**
    *   Dropdown to sort teachers
    *   Options: Name (A-Z), Name (Z-A), ID (Low to High), ID (High to Low), Age (Low to High), Age (High to Low)
    *   Default: Name (A-Z)

*   **Items Per Page**
    *   Controls pagination size
    *   Options: 6, 12, 24, Show All
    *   Default: 12

*   **Export Report**
    *   Dropdown button with export options
    *   Formats: PDF, Excel, CSV, Image (JPG)
    *   Exports filtered results only

### Teacher List Display

*   **Teacher Card**
    *   Displays teacher information in list view
    *   Shows profile picture (or placeholder icon)
    *   Displays: Full Name, Username, ID, Age, Address, Assigned Subjects, Curriculum Count
    *   Shows Active/Inactive status badge
    *   Hover effect with elevation

*   **View Button**
    *   Navigate to `/Admin/Teachers/Details/{id}`
    *   Blue info button with eye icon

*   **Edit Button**
    *   Navigate to `/Admin/Teachers/Edit/{id}`
    *   Yellow warning button with edit icon

*   **Delete Button**
    *   Red danger button with trash icon
    *   Opens confirmation modal before deletion
    *   Modal shows teacher name and warning message

### Actions

*   **Add New Teacher Button**
    *   Navigate to `/Admin/Teachers/Create`
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

*   **No Teachers Found**
    *   Displayed when no teachers exist in system
    *   Shows icon, message, and "Add First Teacher" button

*   **No Results Match Search**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **Create Teacher**
    *   Navigate to create form
    *   Form includes: Username, Password, First Name, Middle Name, Last Name, Date of Birth, Address, Profile Picture, Subject Assignments, Active Status

*   **Edit Teacher**
    *   Navigate to edit form with pre-filled data
    *   Password field optional (only required if changing password)

*   **Delete Teacher**
    *   Soft delete (sets IsActive to false) or hard delete
    *   Requires confirmation
    *   Shows success/error message after operation

*   **View Details**
    *   Navigate to details page showing full teacher information
    *   Includes all assigned subjects and curriculums

