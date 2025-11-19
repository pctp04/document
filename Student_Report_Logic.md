# 13.0 Student Report Screen Logic

## Student Report UI Elements

### Top Navigation Bar

*   **Back Arrow**
    *   Left-pointing arrow icon
    *   Navigate back to Student Dashboard

*   **Student Portal Button**
    *   Button with house icon and "Student Portal" text
    *   Navigate to dashboard/home

*   **Notifications Icon**
    *   Bell icon for notifications
    *   Shows badge if unread

*   **Profile Picture**
    *   Circular profile picture
    *   Navigate to Student Profile

### Student Report Banner

*   **Report Header**
    *   Small dark gray text: "Report for [Student Name]"
    *   Large bold text: "Student Report"
    *   Positioned below navigation

### Report Controls Section

*   **Term Selection**
    *   Label: "Select Term"
    *   Dropdown menu showing "All Periods" with down arrow
    *   Options: All Periods, Prelim, Midterm, Semifinal, Final
    *   Filters report data by selected term
    *   Default: "All Periods"

*   **Generate Report Button**
    *   Prominent purple button
    *   Label: "Generate Report"
    *   Positioned to the right of term selection
    *   Generates/refreshes report based on selected term
    *   Updates table with filtered data

### Report Table

*   **Table Structure**
    *   White background table
    *   Six columns: Course, Prelim, Midterm, Semifinal, Final, Teacher
    *   Header row with column names
    *   Data rows for each enrolled course

*   **Course Column**
    *   Displays course name (e.g., "Mathematics 10")
    *   Course code displayed below or next to name (e.g., "MATH1001")
    *   Bold text for course name

*   **Grade Period Columns**
    *   Prelim, Midterm, Semifinal, Final columns
    *   Display grade value for each period
    *   Shows dash "-" if grade not yet entered
    *   Numeric grades (0-100) with decimal support

*   **Teacher Column**
    *   Displays teacher's full name
    *   Shows teacher assigned to each course
    *   Text format

*   **Table Rows**
    *   One row per enrolled course
    *   All courses listed regardless of term filter
    *   Grade columns show filtered values based on term selection
    *   Alternating row colors for readability (optional)

### Data Operations

*   **Filter by Term**
    *   Select term from dropdown
    *   Click "Generate Report" button
    *   Updates table to show grades for selected term
    *   "All Periods" shows all grade columns with values

*   **Generate Report**
    *   Process selected term filter
    *   Retrieve grade data from database
    *   Populate table with course and grade information
    *   Display all enrolled courses
    *   Show grades for selected term or all terms

*   **Export Report (Optional)**
    *   Export functionality if implemented
    *   Formats: PDF, Excel, CSV
    *   Includes all table data
    *   Preserves term filter selection

### Empty States

*   **No Grades Available**
    *   Displayed when no courses have grades
    *   Shows message in table
    *   All grade columns show dash "-"

*   **No Results for Term**
    *   Displayed when selected term has no grades
    *   Shows message or empty table
    *   Suggests selecting different term

### Grade Display Logic

*   **Grade Format**
    *   Numeric values (0-100)
    *   Decimal values supported (e.g., 85.5)
    *   Dash "-" displayed if grade not entered
    *   Consistent formatting across all periods

*   **Term Filtering**
    *   "All Periods": Shows all grade columns with values
    *   Specific term: Highlights or filters to show only that term's column
    *   Other columns may show dash or be hidden

*   **Course Listing**
    *   Lists all enrolled courses
    *   Shows course name and code
    *   Displays assigned teacher
    *   Maintains consistent order

