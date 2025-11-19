# 16.0 Assignment Submission (Student) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Curriculum Filter | integer | - | - | Dropdown | No | All Curriculums | - | `1` | Filter assignments by curriculum. |
| 2 | Status Filter | string | - | - | Dropdown | No | All Status | - | `Not Started` | Filter by assignment status. Options: All Status, Not Started, In Progress, Submitted, Graded. |
| 3 | Search Input | string | 0 | 255 | Text Input | No | - | - | `quiz` | Search by assignment title. |
| 4 | Assignment ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for assignment. |
| 5 | Assignment Title | string | - | - | Display | - | - | - | `Chapter 5 Quiz` | Title of the assignment. |
| 6 | Assignment Description | string | - | - | Display | - | - | - | `Complete the following questions...` | Detailed description of assignment. |
| 7 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Curriculum this assignment belongs to. |
| 8 | Due Date | datetime | - | - | Display | - | - | Date/Time | `2024-01-20 11:59 PM` | Due date and time for assignment submission. |
| 9 | Days Until Due | integer | - | - | Display | - | Calculated | - | `5` | Number of days until due date. Negative if overdue. |
| 10 | Assignment Status | string | - | - | Badge | - | Not Started | - | `Submitted` | Assignment status: Not Started, In Progress, Submitted, Graded. |
| 11 | Submission Date | datetime | - | - | Display | No | - | Date/Time | `2024-01-18 10:30 AM` | Date and time assignment was submitted. |
| 12 | Submitted Files | file | - | - | Display | No | - | - | `assignment.pdf` | Files submitted by student. Multiple files supported. |
| 13 | Grade Received | decimal | - | - | Display | No | - | - | `85.5` | Grade received for assignment (if graded). |
| 14 | Teacher Feedback | string | - | - | Display | No | - | - | `Good work!` | Feedback or comments from teacher. |
| 15 | Assignment Files | file | - | - | Display | - | - | - | `assignment_instructions.pdf` | Files attached to assignment by teacher. |
| 16 | Submission Files | file | - | - | File Upload | No | - | - | `my_assignment.pdf` | Files to upload for submission. Multiple files supported. |
| 17 | Submit Assignment Button | - | - | - | Button | - | - | - | - | Submit assignment with uploaded files. |
| 18 | View Assignment Button | - | - | - | Button | - | - | - | - | View assignment details and instructions. |
| 19 | Download Assignment Files Button | - | - | - | Button | - | - | - | - | Download assignment files and instructions. |
| 20 | View Submission Button | - | - | - | Button | - | - | - | - | View submitted files and details. |
| 21 | Edit Submission Button | - | - | - | Button | - | - | - | - | Edit submission before due date (only if not graded). |

