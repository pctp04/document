# 11.0 Student Performance (Teacher) Screen Logic

## Student Performance UI Elements

### Filter Section

*   **Curriculum Filter**
    *   Dropdown filter for curriculums
    *   Shows only curriculums assigned to logged-in teacher
    *   Default: "All Curriculums"
    *   Filters students by enrollment

*   **Student Name Filter**
    *   Real-time search filtering
    *   Searches by student name
    *   Case-insensitive search
    *   Updates results as user types

*   **Date Range Filter**
    *   Date range picker
    *   Filter performance data by date range
    *   Default: Current academic period
    *   Shows performance within selected timeframe

### Student Performance List Display

*   **Student Performance Card**
    *   Displays student information and performance metrics
    *   Shows: Student Name, Student ID, Curriculum
    *   Attendance: Percentage, Present Days, Absent Days, Late Days
    *   Grades: List of assignment grades, Average Grade
    *   Overall Performance: Rating badge (color-coded)
    *   Hover effect with elevation

*   **Attendance Section**
    *   Display attendance percentage with progress bar
    *   Show breakdown: Present, Absent, Late days
    *   Color-coded by percentage (Green: >90%, Yellow: 75-90%, Red: <75%)

*   **Grades Section**
    *   Display list of assignment grades
    *   Show assignment title and grade
    *   Calculate and display average grade
    *   Highlight missing grades

*   **Grade Input**
    *   Number input for entering grades
    *   Range: 0-100
    *   Decimal values supported
    *   Validation for valid grade range

*   **Remarks Textarea**
    *   Text input for teacher feedback
    *   Maximum 500 characters
    *   Optional field
    *   Character counter display

*   **Save Grade Button**
    *   Save grade and remarks for student
    *   Green success button
    *   Shows confirmation message on save
    *   Updates performance metrics automatically

*   **View Details Button**
    *   Navigate to `/Teacher/Performance/{studentId}`
    *   Blue info button
    *   View detailed performance history

*   **Export Report Button**
    *   Dropdown with export options
    *   Formats: PDF, Excel, CSV
    *   Exports filtered performance data
    *   Includes all performance metrics

### Detailed Performance View

*   **Performance History**
    *   Timeline view of student performance
    *   Shows grades over time
    *   Attendance trends
    *   Chart visualization (optional)

*   **Assignment Breakdown**
    *   Detailed view of each assignment
    *   Shows: Title, Due Date, Submission Date, Grade, Feedback
    *   Link to view submitted files

*   **Attendance Details**
    *   Calendar view of attendance
    *   Color-coded by status (Present, Absent, Late, Excused)
    *   Filter by date range

### Data Operations

*   **Input Grades**
    *   Enter or update grades for assignments
    *   Save remarks/feedback
    *   Automatically recalculates average grade
    *   Updates overall performance rating

*   **View Performance History**
    *   Access detailed performance view
    *   See trends over time
    *   Compare with class average

*   **Export Reports**
    *   Generate performance reports
    *   Include attendance and grades
    *   Export for individual student or entire class
    *   Multiple format options

### Performance Calculations

*   **Average Grade**
    *   Calculated from all assignment grades
    *   Weighted average if weights assigned
    *   Excludes missing assignments

*   **Overall Performance Rating**
    *   Based on average grade and attendance
    *   Excellent: >90% grade and >95% attendance
    *   Good: 80-90% grade and >90% attendance
    *   Average: 70-80% grade and >85% attendance
    *   Needs Improvement: <70% grade or <85% attendance

