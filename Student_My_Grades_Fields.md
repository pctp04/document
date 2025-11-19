# 11.0 My Grades Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Student Name | string | - | - | Display | - | - | - | `Chisa Kuchiha` | Student's full name displayed in banner. |
| 2 | Grade Level | string | - | - | Display | - | - | - | `Grade - 10A` | Student's grade level and section. |
| 3 | Term Filter | string | - | - | Dropdown | No | All Terms | - | `All Terms` | Filter grades by term. Options: All Terms, Prelim, Midterm, Semifinal, Final. |
| 4 | Course Name | string | - | - | Display | - | - | - | `Mathematics 10` | Name of the course/subject. |
| 5 | Course Code | string | - | - | Display | - | - | - | `MATH1001` | Course code for the subject. |
| 6 | Expand/Collapse Button | - | - | - | Button | - | - | - | - | Orange square button to expand/collapse course grade details. |
| 7 | Comments Button | - | - | - | Button | - | - | - | - | Gray square icon with speech bubble for course comments. |
| 8 | Prelim Grade | decimal | - | - | Display | - | Calculated | - | `85.5` | Grade for preliminary period. Shows dash "-" if not yet graded. |
| 9 | Midterm Grade | decimal | - | - | Display | - | Calculated | - | `88.0` | Grade for midterm period. Shows dash "-" if not yet graded. |
| 10 | Semifinal Grade | decimal | - | - | Display | - | Calculated | - | `87.0` | Grade for semifinal period. Shows dash "-" if not yet graded. |
| 11 | Final Grade | decimal | - | - | Display | - | Calculated | - | `90.0` | Grade for final period. Shows dash "-" if not yet graded. |
| 12 | Final Grade (Overall) | decimal | - | - | Display | - | Calculated | - | `87.6` | Overall final grade for the course. Shows dash "-" if not yet graded. Highlighted when selected. |
| 13 | Grade Component Label | string | - | - | Display | - | - | - | `Prelim` | Label for each grade component period. |
| 14 | Course Card | - | - | - | Card | - | - | - | - | White card containing course information and grade breakdown. |

