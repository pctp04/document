# 10.0 Manage Assignments (Teacher) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Curriculum Filter | integer | - | - | Dropdown | No | All Curriculums | - | `1` | Filter assignments by curriculum. |
| 2 | Status Filter | string | - | - | Dropdown | No | All Status | - | `Published` | Filter by assignment status. Options: All Status, Draft, Published, Closed. |
| 3 | Search Input | string | 0 | 255 | Text Input | No | - | - | `quiz` | Search by assignment title or description. |
| 4 | Assignment ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for assignment. |
| 5 | Assignment Title | string | 1 | 200 | Input/Display | Yes | - | - | `Chapter 5 Quiz` | Title of the assignment. |
| 6 | Assignment Description | string | 0 | 1000 | Textarea/Display | No | - | - | `Complete the following questions...` | Detailed description of assignment. |
| 7 | Due Date | datetime | - | - | Date Input/Display | Yes | - | Date/Time | `2024-01-20 11:59 PM` | Due date and time for assignment submission. |
| 8 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Curriculum this assignment belongs to. |
| 9 | Status | string | - | - | Badge | - | Draft | - | `Published` | Assignment status: Draft, Published, Closed. |
| 10 | Submissions Count | integer | - | - | Display | - | Calculated | - | `20` | Number of students who submitted. |
| 11 | Total Students | integer | - | - | Display | - | Calculated | - | `25` | Total students in curriculum. |
| 12 | Graded Count | integer | - | - | Display | - | Calculated | - | `15` | Number of submissions that have been graded. |
| 13 | Attached Files | string | - | - | File Upload/Display | No | - | URL | `assignment.pdf` | Files attached to assignment. Multiple files supported. |
| 14 | Create Assignment Button | - | - | - | Button | - | - | - | - | Navigate to create assignment form. |
| 15 | Edit Assignment Button | - | - | - | Button | - | - | - | - | Navigate to edit assignment (only for Draft status). |
| 16 | View Submissions Button | - | - | - | Button | - | - | - | - | Navigate to view and grade submissions. |
| 17 | Publish Button | - | - | - | Button | - | - | - | - | Publish draft assignment (changes status to Published). |
| 18 | Close Assignment Button | - | - | - | Button | - | - | - | - | Close assignment (prevents new submissions). |
| 19 | Delete Assignment Button | - | - | - | Button | - | - | - | - | Delete assignment with confirmation (only for Draft status). |

