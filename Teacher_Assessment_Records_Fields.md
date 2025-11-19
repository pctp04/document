# 9.0 Assessment Records Page (Teacher) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH<br>MIN | LENGTH<br>MAX | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|--------|------------|----------|--------------|---------------|---------|---------|
| 1 | Subject Filter | integer | - | - | Dropdown | No | All Subjects | - | `1` | Filter assessments by subject. Shows all assigned subjects. |
| 2 | Assessment Type Filter | string | - | - | Dropdown | No | All Types | - | `Quiz` | Filter by assessment type. Options: All Types, Quiz, Exam, Assignment, Project, Other. |
| 3 | Date Range Filter | date | - | - | Date Range Input | No | - | Date Range | `2024-01-01 to 2024-01-31` | Filter assessments by date range. |
| 4 | Search Input | string | 0 | 255 | Text Input | No | - | - | `midterm` | Search by assessment title or description. |
| 5 | Assessment ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for assessment. |
| 6 | Assessment Title | string | 1 | 200 | Display | - | - | - | `Chapter 5 Quiz` | Title of the assessment. |
| 7 | Assessment Type | string | - | - | Badge | - | - | - | `Quiz` | Type of assessment: Quiz, Exam, Assignment, Project, Other. |
| 8 | Subject Name | string | - | - | Display | - | - | - | `Mathematics` | Subject this assessment belongs to. |
| 9 | Assessment Date | date | - | - | Display | - | - | Date | `2024-01-15` | Date when assessment was conducted. |
| 10 | Students Assessed Count | integer | - | - | Display | - | Calculated | - | `25` | Number of students who took the assessment. |
| 11 | Average Grade | decimal | - | - | Display | - | Calculated | - | `85.5` | Average grade across all students. |
| 12 | Highest Grade | decimal | - | - | Display | - | Calculated | - | `98` | Highest grade received. |
| 13 | Lowest Grade | decimal | - | - | Display | - | Calculated | - | `65` | Lowest grade received. |
| 14 | Description | string | 0 | 500 | Display | No | - | - | `Midterm examination covering chapters 1-5` | Description or notes about the assessment. |
| 15 | Add New Assessment Button | - | - | - | Button | - | - | - | - | Opens Add New Assessment Modal (9.1). |
| 16 | View Details Button | - | - | - | Button | - | - | - | - | View detailed assessment information and individual student grades. |
| 17 | Edit Assessment Button | - | - | - | Button | - | - | - | - | Edit assessment details (if allowed). |
| 18 | Delete Assessment Button | - | - | - | Button | - | - | - | - | Delete assessment with confirmation. |
| 19 | Export Report Button | - | - | - | Button | - | - | - | - | Export assessment records in PDF, Excel, or CSV format. |
| 20 | Results Count | integer | - | - | Display | - | Calculated | - | `15` | Shows filtered results count. |

