# 9.1 Add New Assessment Modal (Teacher) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH<br>MIN | LENGTH<br>MAX | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|--------|------------|----------|--------------|---------------|---------|---------|
| 1 | Assessment Title | string | 1 | 200 | Text Input | Yes | - | - | `Chapter 5 Quiz` | Title of the assessment. Placeholder: "Enter assessment title". |
| 2 | Assessment Type | string | - | - | Dropdown | Yes | - | - | `Quiz` | Type of assessment. Options: Quiz, Exam, Assignment, Project, Other. Required selection. |
| 3 | Subject Selection | integer | - | - | Dropdown | Yes | - | - | `1` | Select subject for assessment. Shows only subjects assigned to teacher. Required. |
| 4 | Assessment Date | date | - | - | Date Input | Yes | Today | Date | `2024-01-15` | Date when assessment was conducted. Date picker. Cannot be in the future. |
| 5 | Description | string | 0 | 500 | Textarea | No | - | - | `Midterm examination covering chapters 1-5` | Description or notes about the assessment. Optional field. Character counter. |
| 6 | Student Selection | integer | - | - | Multi-select/Checkbox | Yes | - | - | `1, 2, 3` | Select students to include in assessment. Shows students enrolled in selected subject's curriculum. Required - at least one student must be selected. |
| 7 | Grade Input (per student) | decimal | 0 | 100 | Number Input | Yes | - | - | `85.5` | Grade for each selected student. Range: 0-100. Decimal values supported. Required for each student. |
| 8 | Remarks (per student) | string | 0 | 200 | Textarea | No | - | - | `Good work!` | Optional remarks or feedback for each student. Character counter per student. |
| 9 | Save Button | - | - | - | Button | - | - | - | - | Save assessment and all student grades. Primary button. Validates all required fields. Shows loading state. |
| 10 | Cancel Button | - | - | - | Button | - | - | - | - | Close modal without saving. Secondary button. Discards all entered data. |
| 11 | Bulk Grade Entry | boolean | - | - | Checkbox | No | false | - | `checked` | Option to apply same grade to all selected students. When checked, single grade input applies to all. |
| 12 | Student Name | string | - | - | Display | - | - | - | `John Doe` | Student's full name in grade entry list. |
| 13 | Student ID | integer | - | - | Display | - | - | - | `1` | Student's ID in grade entry list. |

