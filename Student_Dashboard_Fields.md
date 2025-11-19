# 10.0 Student Dashboard Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Student Name | string | - | - | Display | - | - | - | `Chisa Kuchiha` | Student's full name displayed in welcome banner. |
| 2 | Grade Level | string | - | - | Display | - | - | - | `Grade - 10A` | Student's grade level and section. |
| 3 | Overall Average | decimal | - | - | Display | - | Calculated | - | `87.5` | Overall grade average across all subjects. Shows dash "-" if no grades available. |
| 4 | Subjects Count | integer | - | - | Display | - | Calculated | - | `8` | Total number of subjects student is enrolled in. |
| 5 | Academic Year | string | - | - | Display | - | - | YYYY-YYYY | `2024-2025` | Current academic year in format YYYY-YYYY. |
| 6 | Subject Name | string | - | - | Display | - | - | - | `Mathematics 10` | Name of enrolled subject. |
| 7 | Subject Code | string | - | - | Display | - | - | - | `MATH1001` | Code of the subject (if available). |
| 8 | Semester | string | - | - | Display | - | - | - | `First Semester` | Semester of the subject. |
| 9 | Subject Academic Year | string | - | - | Display | - | - | YYYY-YYYY | `2024-2025` | Academic year for the subject. |
| 10 | Subject Description | string | - | - | Display | - | - | - | `Geometry, statistics, functions...` | Brief description of the subject content. |
| 11 | Final Grade | decimal | - | - | Display | - | Calculated | - | `85.5` | Final grade for the subject. Shows dash "-" if not yet graded. |
| 12 | Subject Icon | - | - | - | Icon | - | - | - | - | Small icon or badge for subject card. |
| 13 | View Subject Details Button | - | - | - | Button | - | - | - | - | Click to view detailed subject information or navigate to grades. |
| 14 | My Grades Button | - | - | - | Navigation | - | - | - | - | Navigate to My Grades screen (11.0). |
| 15 | Student Profile Button | - | - | - | Navigation | - | - | - | - | Navigate to Student Profile screen (12.0). |
| 16 | Student Report Button | - | - | - | Navigation | - | - | - | - | Navigate to Student Report screen (13.0). |
| 17 | Notifications Button | - | - | - | Button | - | - | - | - | Bell icon button for notifications. |
| 18 | Profile Picture | string | - | - | Image | - | - | URL | `https://...` | Student's profile picture in top navigation. |
| 19 | Logout Button | - | - | - | Button | - | - | - | - | Click to logout and redirect to Login screen. |
