# 8.0 Subject Information Page (Teacher) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Search Input | string | 0 | 255 | Text Input | No | - | - | `mathematics` | Search by subject name or code. Real-time filtering. |
| 2 | Subject Filter | integer | - | - | Dropdown | No | All Subjects | - | `1` | Filter by specific subject. Shows all assigned subjects. |
| 3 | Curriculum Filter | integer | - | - | Dropdown | No | All Curriculums | - | `1` | Filter subjects by curriculum. |
| 4 | Subject ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for subject. |
| 5 | Subject Code | string | - | - | Display | - | - | Uppercase | `MATH101` | Subject code displayed as badge. |
| 6 | Subject Name | string | - | - | Display | - | - | - | `Mathematics` | Full name of the subject. |
| 7 | Description | string | - | - | Display | No | - | - | `Introduction to algebra...` | Description of the subject. |
| 8 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Name of curriculum this subject belongs to. |
| 9 | Curriculum Code | string | - | - | Display | - | - | - | `SCI-G7-2024` | Code of curriculum. |
| 10 | Academic Year | string | - | - | Display | - | - | YYYY-YYYY | `2024-2025` | Academic year in format YYYY-YYYY. |
| 11 | Semester | string | - | - | Display | - | - | - | `First Semester` | Semester name. |
| 12 | Grade Level | integer | 7 | 12 | Display | - | - | - | `7` | Grade level for the subject. |
| 13 | Enrolled Students Count | integer | - | - | Display | - | Calculated | - | `25` | Number of students enrolled in subject/curriculum. |
| 14 | Class Schedule | string | - | - | Display | No | - | - | `Monday, Wednesday, Friday 9:00 AM` | Class schedule information if available. |
| 15 | View Students Button | - | - | - | Button | - | - | - | - | Navigate to view student list for this subject. |
| 16 | View Assessment Records Button | - | - | - | Button | - | - | - | - | Navigate to Assessment Records Page filtered by this subject. |
| 17 | Results Count | integer | - | - | Display | - | Calculated | - | `5` | Shows filtered results count. |

