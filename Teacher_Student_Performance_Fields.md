# 11.0 Student Performance (Teacher) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Curriculum Filter | integer | - | - | Dropdown | No | All Curriculums | - | `1` | Filter performance data by curriculum. |
| 2 | Student Name Filter | string | 0 | 255 | Text Input | No | - | - | `john` | Search by student name. Real-time filtering. |
| 3 | Date Range Filter | date | - | - | Date Range Input | No | - | Date Range | `2024-01-01 to 2024-01-31` | Filter performance data by date range. |
| 4 | Student ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for student. |
| 5 | Student Name | string | - | - | Display | - | - | - | `John Doe` | Student's full name. |
| 6 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Curriculum student is enrolled in. |
| 7 | Attendance Record | string | - | - | Display | - | Calculated | Percentage | `95%` | Student's attendance percentage. |
| 8 | Present Days | integer | - | - | Display | - | Calculated | - | `19` | Number of days student was present. |
| 9 | Absent Days | integer | - | - | Display | - | Calculated | - | `1` | Number of days student was absent. |
| 10 | Late Days | integer | - | - | Display | - | Calculated | - | `0` | Number of days student was late. |
| 11 | Assignment Grades | decimal | - | - | Display | - | Calculated | - | `85, 90, 88` | List of grades for assignments. |
| 12 | Average Grade | decimal | - | - | Display | - | Calculated | - | `87.67` | Average grade across all assignments. |
| 13 | Overall Performance | string | - | - | Display | - | Calculated | - | `Excellent` | Overall performance rating (Excellent, Good, Average, Needs Improvement). |
| 14 | Grade Input | decimal | 0 | 100 | Number Input | No | - | - | `85.5` | Input field for teacher to enter grade. |
| 15 | Remarks | string | 0 | 500 | Textarea | No | - | - | `Good work!` | Teacher's remarks or feedback for student. |
| 16 | Export Report Button | - | - | - | Button | - | - | - | - | Export performance report in PDF, Excel, or CSV format. |
| 17 | View Details Button | - | - | - | Button | - | - | - | - | Navigate to detailed student performance view. |
| 18 | Save Grade Button | - | - | - | Button | - | - | - | - | Save grade and remarks for student. |

