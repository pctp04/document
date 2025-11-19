# 17.0 Attendance Record (Student) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Curriculum Filter | integer | - | - | Dropdown | No | All Curriculums | - | `1` | Filter attendance records by curriculum. |
| 2 | Date Range Filter | date | - | - | Date Range Input | No | - | Date Range | `2024-01-01 to 2024-01-31` | Filter attendance by date range. |
| 3 | Status Filter | string | - | - | Dropdown | No | All Status | - | `Present` | Filter by attendance status. Options: All Status, Present, Absent, Late, Excused. |
| 4 | Attendance ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for attendance record. |
| 5 | Date | date | - | - | Display | - | - | Date | `2024-01-15` | Date of attendance record. |
| 6 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Curriculum for attendance record. |
| 7 | Subject Name | string | - | - | Display | - | - | - | `Mathematics` | Subject for attendance record. |
| 8 | Attendance Status | string | - | - | Badge | - | - | - | `Present` | Attendance status: Present, Absent, Late, Excused. |
| 9 | Class Time | time | - | - | Display | - | - | Time | `09:00 AM` | Time of the class. |
| 10 | Total Days | integer | - | - | Display | - | Calculated | - | `20` | Total number of class days in period. |
| 11 | Present Days | integer | - | - | Display | - | Calculated | - | `19` | Number of days student was present. |
| 12 | Absent Days | integer | - | - | Display | - | Calculated | - | `1` | Number of days student was absent. |
| 13 | Late Days | integer | - | - | Display | - | Calculated | - | `0` | Number of days student was late. |
| 14 | Excused Days | integer | - | - | Display | - | Calculated | - | `0` | Number of days student was excused. |
| 15 | Attendance Percentage | decimal | - | - | Display | - | Calculated | - | `95%` | Overall attendance percentage. |
| 16 | Calendar View | - | - | - | Calendar | - | - | - | - | Calendar visualization of attendance. |
| 17 | Export Report Button | - | - | - | Button | - | - | - | - | Export attendance report in PDF, Excel, or CSV format. |
| 18 | Results Count | integer | - | - | Display | - | Calculated | - | `20` | Shows filtered results count. |

