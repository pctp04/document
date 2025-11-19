# 14.0 Student Dashboard Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Enrolled Curriculums Count | integer | - | - | Display | - | Calculated | - | `4` | Count of curriculums student is enrolled in. |
| 2 | Pending Assignments | integer | - | - | Display | - | Calculated | - | `5` | Count of assignments not yet submitted. |
| 3 | Recent Messages | integer | - | - | Display | - | Calculated | - | `2` | Count of unread messages. |
| 4 | Overall Grade Average | decimal | - | - | Display | - | Calculated | - | `87.5` | Average grade across all enrolled curriculums. |
| 5 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Name of enrolled curriculum. |
| 6 | Curriculum Code | string | - | - | Display | - | - | - | `SCI-G7-2024` | Code of enrolled curriculum. |
| 7 | Academic Year | string | - | - | Display | - | - | YYYY-YYYY | `2024-2025` | Academic year of curriculum. |
| 8 | Semester | string | - | - | Display | - | - | - | `First Semester` | Semester of curriculum. |
| 9 | Grade Level | integer | 7 | 12 | Display | - | - | - | `7` | Grade level of curriculum. |
| 10 | Assignment Title | string | - | - | Display | - | - | - | `Chapter 5 Quiz` | Title of upcoming assignment. |
| 11 | Assignment Due Date | datetime | - | - | Display | - | - | Date/Time | `2024-01-20 11:59 PM` | Due date for assignment submission. |
| 12 | Assignment Status | string | - | - | Badge | - | - | - | `Not Started` | Assignment status: Not Started, In Progress, Submitted, Graded. |
| 13 | Days Until Due | integer | - | - | Display | - | Calculated | - | `5` | Number of days until assignment due date. |
| 14 | Attendance Percentage | decimal | - | - | Display | - | Calculated | - | `95%` | Overall attendance percentage across all curriculums. |
| 15 | Present Days | integer | - | - | Display | - | Calculated | - | `19` | Total present days. |
| 16 | Absent Days | integer | - | - | Display | - | Calculated | - | `1` | Total absent days. |
| 17 | Course Materials Button | - | - | - | Button | - | - | - | - | Click to navigate to Course Materials screen. |
| 18 | Assignment Submission Button | - | - | - | Button | - | - | - | - | Click to navigate to Assignment Submission screen. |
| 19 | Attendance Record Button | - | - | - | Button | - | - | - | - | Click to navigate to Attendance Record screen. |
| 20 | Messaging Center Button | - | - | - | Button | - | - | - | - | Click to navigate to Messaging Center screen. |
| 21 | Logout Button | - | - | - | Button | - | - | - | - | Click to logout and redirect to Student Login screen. |

