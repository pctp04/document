# 7.0 Teacher Dashboard Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH<br>MIN | LENGTH<br>MAX | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|--------|------------|----------|--------------|---------------|---------|---------|
| 1 | Assigned Subjects Count | integer | - | - | Display | - | Calculated | - | `5` | Count of subjects assigned to logged-in teacher. |
| 2 | Total Students | integer | - | - | Display | - | Calculated | - | `75` | Total count of students across all assigned subjects/curriculums. |
| 3 | Total Assessments | integer | - | - | Display | - | Calculated | - | `25` | Total number of assessments recorded. |
| 4 | Recent Assessments | integer | - | - | Display | - | Calculated | - | `5` | Count of assessments created in the last 7 days. |
| 5 | Subject Name | string | - | - | Display | - | - | - | `Mathematics` | Name of assigned subject. |
| 6 | Subject Code | string | - | - | Display | - | - | - | `MATH101` | Code of assigned subject. |
| 7 | Students in Subject | integer | - | - | Display | - | Calculated | - | `25` | Number of students enrolled in subject's curriculum. |
| 8 | Assessments Count | integer | - | - | Display | - | Calculated | - | `8` | Number of assessments for this subject. |
| 9 | Average Grade | decimal | - | - | Display | - | Calculated | - | `85.5` | Average grade across all assessments for subject. |
| 10 | Upcoming Classes | string | - | - | Display | - | - | Date/Time | `2024-01-15 09:00 AM` | List of upcoming class schedules. |
| 11 | Recent Assessment Title | string | - | - | Display | - | - | - | `Chapter 5 Quiz` | Title of most recent assessment. |
| 12 | Recent Assessment Date | date | - | - | Display | - | - | Date | `2024-01-15` | Date of most recent assessment. |
| 13 | Subject Information Button | - | - | - | Button | - | - | - | - | Click to navigate to Subject Information Page (8.0). |
| 14 | Assessment Records Button | - | - | - | Button | - | - | - | - | Click to navigate to Assessment Records Page (9.0). |
| 15 | Logout Button | - | - | - | Button | - | - | - | - | Click to logout and redirect to Login screen. |

