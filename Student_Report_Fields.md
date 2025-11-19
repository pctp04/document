# 13.0 Student Report Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH<br>MIN | LENGTH<br>MAX | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|--------|------------|----------|--------------|---------------|---------|---------|
| 1 | Student Name | string | - | - | Display | - | - | - | `Chisa Kuchiha` | Student's full name displayed in report header. |
| 2 | Report Title | string | - | - | Display | - | - | - | `Student Report` | Title of the report page. |
| 3 | Term Filter | string | - | - | Dropdown | No | All Periods | - | `All Periods` | Filter report by term. Options: All Periods, Prelim, Midterm, Semifinal, Final. |
| 4 | Generate Report Button | - | - | - | Button | - | - | - | - | Purple button to generate/refresh the report. |
| 5 | Course Name | string | - | - | Display | - | - | - | `Mathematics 10` | Name of the course/subject in report table. |
| 6 | Course Code | string | - | - | Display | - | - | - | `MATH1001` | Course code displayed next to course name. |
| 7 | Prelim Grade | decimal | - | - | Display | - | Calculated | - | `85.5` | Grade for preliminary period. Shows dash "-" if not yet graded. |
| 8 | Midterm Grade | decimal | - | - | Display | - | Calculated | - | `88.0` | Grade for midterm period. Shows dash "-" if not yet graded. |
| 9 | Semifinal Grade | decimal | - | - | Display | - | Calculated | - | `87.0` | Grade for semifinal period. Shows dash "-" if not yet graded. |
| 10 | Final Grade | decimal | - | - | Display | - | Calculated | - | `90.0` | Grade for final period. Shows dash "-" if not yet graded. |
| 11 | Teacher Name | string | - | - | Display | - | - | - | `Kathleen Roma` | Name of teacher assigned to the course. |
| 12 | Report Table | - | - | - | Table | - | - | - | - | Table displaying all courses with grade periods and teachers. |
| 13 | Export Report Button | - | - | - | Button | No | - | - | - | Export report in PDF, Excel, or CSV format (optional). |

