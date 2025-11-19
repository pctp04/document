# 5.0 Subject Management Screen Logic

## Subject Management UI Elements

### Filter Section

*   **Search Input**
    *   Real-time search filtering
    *   Searches by subject code or subject name
    *   Case-insensitive search
    *   Updates results as user types

*   **Code Filter**
    *   Dropdown filter for subject code prefixes
    *   Options: All Codes, 701, 801, 901, 1001
    *   Default: "All Codes"
    *   Filters by code prefix matching

*   **Status Filter**
    *   Dropdown filter for Active/Inactive status
    *   Default: "All Status"
    *   Filters subjects based on IsActive property

*   **Sort By**
    *   Dropdown to sort subjects
    *   Options: Code (A-Z), Code (Z-A), Name (A-Z), Name (Z-A)
    *   Default: Code (A-Z)

*   **Export Report**
    *   Dropdown button with export options
    *   Formats: PDF, Excel, CSV, Image (JPG)
    *   Exports filtered results only

### Subject List Display

*   **Subject Card**
    *   Displays subject information in list view
    *   Shows subject code as primary badge
    *   Displays: Subject Code, Subject Name, Description (if available)
    *   Shows Active/Inactive status badge
    *   Hover effect with elevation

*   **View Button**
    *   Navigate to `/Admin/Subjects/Details/{id}`
    *   Blue info button with eye icon

*   **Edit Button**
    *   Navigate to `/Admin/Subjects/Edit/{id}`
    *   Yellow warning button with edit icon

*   **Delete Button**
    *   Red danger button with trash icon
    *   Opens confirmation modal before deletion
    *   Modal shows subject code and name

### Actions

*   **Add New Subject Button**
    *   Navigate to `/Admin/Subjects/Create`
    *   Primary button in page header

*   **Reset Filters**
    *   Clears all filters and resets to default view
    *   Available in "No Results" empty state

### Empty States

*   **No Subjects Found**
    *   Displayed when no subjects exist in system
    *   Shows icon, message, and "Add First Subject" button

*   **No Results Match Search**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **Create Subject**
    *   Navigate to create form
    *   Form includes: Subject Code (auto-uppercase), Subject Name, Description (optional), Active Status
    *   Subject code must be unique
    *   Subject code automatically converted to uppercase

*   **Edit Subject**
    *   Navigate to edit form with pre-filled data
    *   All fields editable except Subject ID
    *   Subject code uniqueness validated on save

*   **Delete Subject**
    *   Soft delete (sets IsActive to false) or hard delete
    *   Requires confirmation
    *   Shows success/error message after operation
    *   May prevent deletion if subject is assigned to teachers or curriculums

*   **View Details**
    *   Navigate to details page showing full subject information
    *   Includes list of assigned teachers and curriculums if any

