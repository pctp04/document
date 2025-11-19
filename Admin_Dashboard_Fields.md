# 2.0 Admin Dashboard Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Total Teachers | integer | - | - | Display | - | Calculated | - | `25` | Count of all teachers in system (active and inactive). |
| 2 | Active Teachers | integer | - | - | Display | - | Calculated | - | `23` | Count of active teachers only. |
| 3 | Inactive Teachers | integer | - | - | Display | - | Calculated | - | `2` | Count of inactive teachers. Displayed only if greater than 0. |
| 4 | Total Students | integer | - | - | Display | - | Calculated | - | `150` | Count of all students in system (active and inactive). |
| 5 | Active Students | integer | - | - | Display | - | Calculated | - | `145` | Count of active students only. |
| 6 | Inactive Students | integer | - | - | Display | - | Calculated | - | `5` | Count of inactive students. Displayed only if greater than 0. |
| 7 | Total Subjects | integer | - | - | Display | - | Calculated | - | `12` | Count of all subjects in system (active and inactive). |
| 8 | Active Subjects | integer | - | - | Display | - | Calculated | - | `11` | Count of active subjects only. |
| 9 | Inactive Subjects | integer | - | - | Display | - | Calculated | - | `1` | Count of inactive subjects. Displayed only if greater than 0. |
| 10 | Total Curriculums | integer | - | - | Display | - | Calculated | - | `8` | Count of all curriculums in system (active and inactive). |
| 11 | Active Curriculums | integer | - | - | Display | - | Calculated | - | `7` | Count of active curriculums only. |
| 12 | Inactive Curriculums | integer | - | - | Display | - | Calculated | - | `1` | Count of inactive curriculums. Displayed only if greater than 0. |
| 13 | Grade 7 Students | integer | - | - | Display | - | Calculated | - | `35` | Count of students in Grade 7. |
| 14 | Grade 8 Students | integer | - | - | Display | - | Calculated | - | `40` | Count of students in Grade 8. |
| 15 | Grade 9 Students | integer | - | - | Display | - | Calculated | - | `38` | Count of students in Grade 9. |
| 16 | Grade 10 Students | integer | - | - | Display | - | Calculated | - | `37` | Count of students in Grade 10. |
| 17 | System Status | string | - | - | Display | - | Static | - | `System Running Smoothly` | Status indicator showing system operational state. |
| 18 | Database Status | string | - | - | Display | - | Static | - | `Database Connected` | Status indicator showing database connection state. |
| 19 | Active Users Count | integer | - | - | Display | - | Calculated | - | `168` | Total count of active teachers and students combined. |
| 20 | Add New Teacher | - | - | - | Button | - | - | - | - | Click to navigate to Create Teacher screen. |
| 21 | Add New Student | - | - | - | Button | - | - | - | - | Click to navigate to Create Student screen. |
| 22 | Add New Subject | - | - | - | Button | - | - | - | - | Click to navigate to Create Subject screen. |
| 23 | Create Curriculum | - | - | - | Button | - | - | - | - | Click to navigate to Create Curriculum screen. |
| 24 | Logout | - | - | - | Button | - | - | - | - | Click to logout and redirect to Login screen. |

