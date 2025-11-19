# 6.0 Curriculum Management Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Search Input | string | 0 | 255 | Text Input | No | - | - | `science` | Search by curriculum name or code. Real-time filtering. |
| 2 | Grade Level Filter | integer | - | - | Dropdown | No | All Grades | - | `7` | Filter by grade level. Options: All Grades, Grade 7, Grade 8, Grade 9, Grade 10. |
| 3 | Status Filter | string | - | - | Dropdown | No | All Status | - | `Active` | Filter by Active or Inactive status. Options: All Status, Active, Inactive. |
| 4 | Academic Year Filter | string | - | - | Dropdown | No | All Years | - | `2024-2025` | Filter by academic year. Shows last 5 years. Format: YYYY-YYYY. |
| 5 | Export Report | - | - | - | Dropdown Button | No | - | - | - | Generate report in PDF, Excel, CSV, or Image format. |
| 6 | Curriculum ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for curriculum. |
| 7 | Curriculum Name | string | 3 | 200 | Display | - | - | - | `Science Program Grade 7` | Full name of the curriculum program. |
| 8 | Curriculum Code | string | 2 | 50 | Display | - | - | Uppercase | `SCI-G7-2024` | Curriculum code displayed as badge. Must be unique. |
| 9 | Academic Year | string | - | - | Display | - | - | YYYY-YYYY | `2024-2025` | Academic year in format YYYY-YYYY. |
| 10 | Semester | string | 1 | 50 | Display | - | - | - | `First Semester` | Semester name (e.g., First Semester, Second Semester). |
| 11 | Grade Level | integer | 7 | 12 | Display | - | - | - | `7` | Grade level for the curriculum. |
| 12 | Description | string | 0 | 1000 | Display | No | - | - | `Comprehensive science...` | Optional description of the curriculum. |
| 13 | Subjects Count | integer | - | - | Display | - | Calculated | - | `5` | Number of subjects in curriculum. |
| 14 | Teachers Count | integer | - | - | Display | - | Calculated | - | `3` | Number of unique teachers assigned to curriculum. |
| 15 | Students Count | integer | - | - | Display | - | Calculated | - | `25` | Number of students enrolled in curriculum. |
| 16 | Status Badge | string | - | - | Badge | - | - | - | `Active` | Visual indicator: Green for Active, Red for Inactive. |
| 17 | View Button | - | - | - | Button | - | - | - | - | Navigate to curriculum details page. |
| 18 | Edit Button | - | - | - | Button | - | - | - | - | Navigate to edit curriculum page. |
| 19 | Delete Button | - | - | - | Button | - | - | - | - | Delete curriculum with confirmation dialog. |
| 20 | Create New Curriculum Button | - | - | - | Button | - | - | - | - | Navigate to create curriculum page. |
| 21 | Results Count | integer | - | - | Display | - | Calculated | - | `8` | Shows filtered results count. |

