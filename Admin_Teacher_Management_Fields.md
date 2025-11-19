# 3.0 Teacher Management Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH<br>MIN | LENGTH<br>MAX | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|--------|------------|----------|--------------|---------------|---------|---------|
| 1 | Search Input | string | 0 | 255 | Text Input | No | - | - | `john` | Search by teacher name, username, or assigned subjects. Real-time filtering. |
| 2 | Status Filter | string | - | - | Dropdown | No | All Status | - | `Active` | Filter by Active or Inactive status. Options: All Status, Active, Inactive. |
| 3 | Sort By | string | - | - | Dropdown | No | Name (A-Z) | - | `Name (A-Z)` | Sort options: Name (A-Z), Name (Z-A), ID (Low to High), ID (High to Low), Age (Low to High), Age (High to Low). |
| 4 | Items Per Page | integer | - | - | Dropdown | No | 12 | - | `12` | Options: 6, 12, 24, Show All. Controls pagination. |
| 5 | Export Report | - | - | - | Dropdown Button | No | - | - | - | Generate report in PDF, Excel, CSV, or Image format. |
| 6 | Teacher ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for teacher. |
| 7 | Full Name | string | - | - | Display | - | - | - | `John Doe` | Teacher's full name (First + Middle + Last). |
| 8 | Username | string | 1 | 100 | Display | - | - | - | `johndoe` | Teacher's login username. Displayed with @ prefix. |
| 9 | Age | integer | - | - | Display | - | Calculated | - | `35` | Calculated from date of birth. |
| 10 | Address | string | 10 | 255 | Display | - | - | - | `123 Main St, City` | Teacher's complete address. |
| 11 | Profile Picture | string | - | - | Image | No | - | URL | `https://...` | Teacher's profile picture. Shows placeholder if not available. |
| 12 | Assigned Subjects | string | - | - | Display | No | - | - | `MATH101, ENG102` | List of subject codes assigned to teacher. |
| 13 | Curriculum Count | integer | - | - | Display | - | Calculated | - | `3` | Number of curriculums teacher is assigned to. |
| 14 | Status Badge | string | - | - | Badge | - | - | - | `Active` | Visual indicator: Green for Active, Red for Inactive. |
| 15 | View Button | - | - | - | Button | - | - | - | - | Navigate to teacher details page. |
| 16 | Edit Button | - | - | - | Button | - | - | - | - | Navigate to edit teacher page. |
| 17 | Delete Button | - | - | - | Button | - | - | - | - | Delete teacher with confirmation dialog. |
| 18 | Add New Teacher Button | - | - | - | Button | - | - | - | - | Navigate to create teacher page. |
| 19 | Results Count | integer | - | - | Display | - | Calculated | - | `25` | Shows filtered results count. |
| 20 | Pagination | - | - | - | Navigation | - | - | - | - | Page numbers with previous/next buttons. |

