# 12.0 Student Profile Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Profile Picture | string | - | - | Image | - | - | URL | `https://...` | Student's profile picture displayed in circular format. |
| 2 | Change Photo Button | - | - | - | Button | - | - | - | - | Button with upload icon to change profile picture. |
| 3 | Full Name | string | - | - | Text Input/Display | - | - | - | `Chisa Kuchiha` | Student's full name. Read-only in view mode, editable in edit mode. |
| 4 | Username | string | - | - | Text Input/Display | - | - | - | `Chisa` | Student's username. Read-only in view mode, editable in edit mode. |
| 5 | Student ID | integer | - | - | Display | - | Auto-generated | - | `74` | Unique student identifier. Read-only, cannot be edited. |
| 6 | Curriculum | string | - | - | Display | - | - | - | `Grade - 10A` | Student's current curriculum/grade level. Read-only. |
| 7 | Academic Year | string | - | - | Display | - | - | - | `2021-2022 (Current)` | Current academic year with status indicator. Read-only. |
| 8 | Edit Button | - | - | - | Button | - | - | - | - | Button to enable editing of profile information. Changes to "Save" and "Cancel" in edit mode. |
| 9 | Save Button | - | - | - | Button | - | - | - | - | Save changes to profile. Only visible in edit mode. |
| 10 | Cancel Button | - | - | - | Button | - | - | - | - | Cancel editing and revert changes. Only visible in edit mode. |
| 11 | Profile Picture File | file | - | - | File Upload | No | - | - | `image.jpg` | File input for uploading new profile picture. Accepted formats: JPG, PNG, GIF. |

