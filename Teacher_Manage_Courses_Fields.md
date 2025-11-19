# 9.0 Manage Courses (Teacher) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Search Input | string | 0 | 255 | Text Input | No | - | - | `science` | Search by curriculum name or code. Real-time filtering. |
| 2 | Academic Year Filter | string | - | - | Dropdown | No | All Years | - | `2024-2025` | Filter by academic year. Format: YYYY-YYYY. |
| 3 | Grade Level Filter | integer | - | - | Dropdown | No | All Grades | - | `7` | Filter by grade level. Options: All Grades, Grade 7, Grade 8, Grade 9, Grade 10. |
| 4 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Name of assigned curriculum. |
| 5 | Curriculum Code | string | - | - | Display | - | - | - | `SCI-G7-2024` | Code of assigned curriculum displayed as badge. |
| 6 | Academic Year | string | - | - | Display | - | - | YYYY-YYYY | `2024-2025` | Academic year in format YYYY-YYYY. |
| 7 | Semester | string | - | - | Display | - | - | - | `First Semester` | Semester name. |
| 8 | Grade Level | integer | 7 | 12 | Display | - | - | - | `7` | Grade level for the curriculum. |
| 9 | Subjects Count | integer | - | - | Display | - | Calculated | - | `5` | Number of subjects in curriculum. |
| 10 | Students Count | integer | - | - | Display | - | Calculated | - | `25` | Number of students enrolled in curriculum. |
| 11 | View Course Materials Button | - | - | - | Button | - | - | - | - | Navigate to course materials page for curriculum. |
| 12 | View Students Button | - | - | - | Button | - | - | - | - | Navigate to student list for curriculum. |
| 13 | Manage Assignments Button | - | - | - | Button | - | - | - | - | Navigate to assignments for this curriculum. |
| 14 | View Performance Button | - | - | - | Button | - | - | - | - | Navigate to student performance for this curriculum. |
| 15 | Results Count | integer | - | - | Display | - | Calculated | - | `3` | Shows filtered results count. |

