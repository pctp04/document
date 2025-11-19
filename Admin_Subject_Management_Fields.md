# 5.0 Subject Management Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Search Input | string | 0 | 255 | Text Input | No | - | - | `math` | Search by subject code or name. Real-time filtering. |
| 2 | Code Filter | string | - | - | Dropdown | No | All Codes | - | `701` | Filter by subject code prefix. Options: All Codes, 701, 801, 901, 1001. |
| 3 | Status Filter | string | - | - | Dropdown | No | All Status | - | `Active` | Filter by Active or Inactive status. Options: All Status, Active, Inactive. |
| 4 | Sort By | string | - | - | Dropdown | No | Code (A-Z) | - | `Code (A-Z)` | Sort options: Code (A-Z), Code (Z-A), Name (A-Z), Name (Z-A). |
| 5 | Export Report | - | - | - | Dropdown Button | No | - | - | - | Generate report in PDF, Excel, CSV, or Image format. |
| 6 | Subject ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for subject. |
| 7 | Subject Code | string | 1 | 20 | Display | - | - | Uppercase | `MATH101` | Subject code displayed as badge. Must be unique. |
| 8 | Subject Name | string | 1 | 200 | Display | - | - | - | `Mathematics` | Full name of the subject. |
| 9 | Description | string | 0 | 1000 | Display | No | - | - | `Introduction to algebra...` | Optional description of the subject. |
| 10 | Status Badge | string | - | - | Badge | - | - | - | `Active` | Visual indicator: Green for Active, Red for Inactive. |
| 11 | View Button | - | - | - | Button | - | - | - | - | Navigate to subject details page. |
| 12 | Edit Button | - | - | - | Button | - | - | - | - | Navigate to edit subject page. |
| 13 | Delete Button | - | - | - | Button | - | - | - | - | Delete subject with confirmation dialog. |
| 14 | Add New Subject Button | - | - | - | Button | - | - | - | - | Navigate to create subject page. |
| 15 | Results Count | integer | - | - | Display | - | Calculated | - | `12` | Shows filtered results count. |

