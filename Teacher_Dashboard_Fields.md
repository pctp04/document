# 8.0 Teacher Dashboard Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Assigned Curriculums Count | integer | - | - | Display | - | Calculated | - | `3` | Count of curriculums assigned to logged-in teacher. |
| 2 | Total Students | integer | - | - | Display | - | Calculated | - | `75` | Total count of students across all assigned curriculums. |
| 3 | Pending Assignments | integer | - | - | Display | - | Calculated | - | `5` | Count of assignments that need grading. |
| 4 | Recent Messages | integer | - | - | Display | - | Calculated | - | `3` | Count of unread messages. |
| 5 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Name of assigned curriculum. |
| 6 | Curriculum Code | string | - | - | Display | - | - | - | `SCI-G7-2024` | Code of assigned curriculum. |
| 7 | Students in Curriculum | integer | - | - | Display | - | Calculated | - | `25` | Number of students enrolled in specific curriculum. |
| 8 | Average Grade | decimal | - | - | Display | - | Calculated | - | `85.5` | Average grade across all students in curriculum. |
| 9 | Total Grades | integer | - | - | Display | - | Calculated | - | `150` | Total number of grades recorded for curriculum. |
| 10 | Upcoming Classes | string | - | - | Display | - | - | Date/Time | `2024-01-15 09:00 AM` | List of upcoming class schedules. |
| 11 | Assignment Title | string | - | - | Display | - | - | - | `Chapter 5 Quiz` | Title of pending assignment. |
| 12 | Assignment Due Date | datetime | - | - | Display | - | - | Date/Time | `2024-01-20 11:59 PM` | Due date for assignment submission. |
| 13 | Unread Messages Count | integer | - | - | Display | - | Calculated | - | `3` | Number of unread messages. |
| 14 | Manage Courses Button | - | - | - | Button | - | - | - | - | Click to navigate to Manage Courses screen. |
| 15 | Manage Assignments Button | - | - | - | Button | - | - | - | - | Click to navigate to Manage Assignments screen. |
| 16 | Student Performance Button | - | - | - | Button | - | - | - | - | Click to navigate to Student Performance screen. |
| 17 | Communication Center Button | - | - | - | Button | - | - | - | - | Click to navigate to Communication Center screen. |
| 18 | Logout Button | - | - | - | Button | - | - | - | - | Click to logout and redirect to Teacher Login screen. |

