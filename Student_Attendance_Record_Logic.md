# 17.0 Attendance Record (Student) Screen Logic

## Attendance Record UI Elements

### Filter Section

*   **Curriculum Filter**
    *   Dropdown filter for curriculums
    *   Shows only curriculums student is enrolled in
    *   Default: "All Curriculums"

*   **Date Range Filter**
    *   Date range picker
    *   Filter attendance records by date range
    *   Default: Current academic period
    *   Shows attendance within selected timeframe

*   **Status Filter**
    *   Dropdown filter by attendance status
    *   Options: All Status, Present, Absent, Late, Excused
    *   Default: "All Status"

### Attendance Statistics Display

*   **Overall Statistics Card**
    *   Displays summary statistics
    *   Shows: Total Days, Present Days, Absent Days, Late Days, Excused Days
    *   Attendance Percentage with progress bar
    *   Color-coded by percentage (Green: >90%, Yellow: 75-90%, Red: <75%)

*   **Attendance Percentage**
    *   Large display of percentage
    *   Visual progress bar
    *   Shows percentage calculation

### Attendance List Display

*   **Attendance Record Row**
    *   Displays attendance information in table/list format
    *   Shows: Date, Curriculum, Subject, Status badge, Class Time
    *   Color-coded rows by status
    *   Hover effect

*   **Status Badges**
    *   Present: Green badge with checkmark
    *   Absent: Red badge with X
    *   Late: Yellow badge with clock icon
    *   Excused: Blue badge with info icon

### Calendar View

*   **Monthly Calendar**
    *   Calendar visualization of attendance
    *   Color-coded days by status:
        *   Present: Green
        *   Absent: Red
        *   Late: Yellow
        *   Excused: Blue
        *   No class: Gray
    *   Click day to view details
    *   Legend showing color meanings

*   **Day Details**
    *   Shows attendance details for selected day
    *   Displays: Date, Curriculum, Subject, Status, Class Time
    *   Shows any notes or remarks

### Attendance Breakdown by Curriculum

*   **Curriculum Statistics**
    *   Shows attendance statistics per curriculum
    *   Displays: Curriculum Name, Total Days, Present Days, Absent Days, Percentage
    *   Progress bars for each curriculum
    *   Compare attendance across curriculums

### Export Functionality

*   **Export Report Button**
    *   Dropdown with export options
    *   Formats: PDF, Excel, CSV
    *   Exports filtered attendance data
    *   Includes all statistics and records

### Empty States

*   **No Attendance Records**
    *   Displayed when no attendance records exist
    *   Shows icon and message
    *   Indicates records will appear as classes are conducted

*   **No Results Match Filter**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **View Attendance Records**
    *   Display all attendance records
    *   Filter by curriculum, date range, or status
    *   View in list or calendar format

*   **View Statistics**
    *   Display overall attendance statistics
    *   Breakdown by curriculum
    *   Calculate percentages automatically

*   **Export Reports**
    *   Generate attendance reports
    *   Include statistics and detailed records
    *   Export for specific date range or curriculum
    *   Multiple format options

### Attendance Calculations

*   **Attendance Percentage**
    *   Calculated as: (Present Days / Total Days) * 100
    *   Excludes excused absences from calculation
    *   Updates automatically with new records

*   **Status Counts**
    *   Counts for each status type
    *   Updates based on filtered records
    *   Shows breakdown in statistics card

