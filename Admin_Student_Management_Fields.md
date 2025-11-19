# 4.0 Student Management Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Search Input | string | 0 | 255 | Text Input | No | - | - | `jane` | Search by student name. Real-time filtering. |
| 2 | Grade Level Filter | integer | - | - | Dropdown | No | All Grades | - | `7` | Filter by grade level. Options: All Grades, Grade 7, Grade 8, Grade 9, Grade 10. |
| 3 | Status Filter | string | - | - | Dropdown | No | All Status | - | `Active` | Filter by Active or Inactive status. Options: All Status, Active, Inactive. |
| 4 | Sort By | string | - | - | Dropdown | No | Name (A-Z) | - | `Name (A-Z)` | Sort options: Name (A-Z), Name (Z-A), Grade Level (Low to High), Grade Level (High to Low), Age (Low to High), Age (High to Low). |
| 5 | Items Per Page | integer | - | - | Dropdown | No | 12 | - | `12` | Options: 6, 12, 24, Show All. Controls pagination. |
| 6 | Export Report | - | - | - | Dropdown Button | No | - | - | - | Generate report in PDF, Excel, CSV, or Image format. |
| 7 | Student ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for student. |
| 8 | Full Name | string | - | - | Display | - | - | - | `Jane Smith` | Student's full name (First + Middle + Last). |
| 9 | Grade Level | integer | 7 | 10 | Display | - | - | - | `7` | Student's current grade level. |
| 10 | Age | integer | - | - | Display | - | Calculated | - | `13` | Calculated from date of birth. |
| 11 | Address | string | 10 | 255 | Display | - | - | - | `456 Oak Ave, City` | Student's complete address. |
| 12 | Profile Picture | string | - | - | Image | No | - | URL | `https://...` | Student's profile picture. Shows placeholder icon if not available. |
| 13 | Status Badge | string | - | - | Badge | - | - | - | `Active` | Visual indicator: Green for Active, Red for Inactive. |
| 14 | View Button | - | - | - | Button | - | - | - | - | Navigate to student details page. |
| 15 | Edit Button | - | - | - | Button | - | - | - | - | Navigate to edit student page. |
| 16 | Delete Button | - | - | - | Button | - | - | - | - | Delete student with confirmation dialog. |
| 17 | Add New Student Button | - | - | - | Button | - | - | - | - | Navigate to create student page. |
| 18 | Results Count | integer | - | - | Display | - | Calculated | - | `150` | Shows filtered results count. |
| 19 | Pagination | - | - | - | Navigation | - | - | - | - | Page numbers with previous/next buttons. |

