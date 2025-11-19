# 15.0 Course Materials (Student) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Curriculum Filter | integer | - | - | Dropdown | No | All Curriculums | - | `1` | Filter materials by curriculum. |
| 2 | Subject Filter | integer | - | - | Dropdown | No | All Subjects | - | `1` | Filter materials by subject. |
| 3 | Material Type Filter | string | - | - | Dropdown | No | All Types | - | `Lecture Notes` | Filter by material type. Options: All Types, Lecture Notes, Assignments, Resources, Videos. |
| 4 | Search Input | string | 0 | 255 | Text Input | No | - | - | `chapter 5` | Search by material title or description. |
| 5 | Curriculum Name | string | - | - | Display | - | - | - | `Science Program Grade 7` | Name of curriculum materials belong to. |
| 6 | Subject Name | string | - | - | Display | - | - | - | `Mathematics` | Name of subject materials belong to. |
| 7 | Material ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for material. |
| 8 | Material Title | string | 1 | 200 | Display | - | - | - | `Chapter 5 Lecture Notes` | Title of the course material. |
| 9 | Material Description | string | 0 | 500 | Display | No | - | - | `Notes covering algebraic equations...` | Description of the material content. |
| 10 | Material Type | string | - | - | Badge | - | - | - | `Lecture Notes` | Type of material: Lecture Notes, Assignment, Resource, Video. |
| 11 | Upload Date | datetime | - | - | Display | - | - | Date/Time | `2024-01-10 09:00 AM` | Date and time material was uploaded. |
| 12 | File Name | string | - | - | Display | - | - | - | `chapter5_notes.pdf` | Name of the uploaded file. |
| 13 | File Size | string | - | - | Display | - | - | - | `2.5 MB` | Size of the file in readable format. |
| 14 | Download Link | string | - | - | Link | - | - | URL | `https://...` | Link to download the material file. |
| 15 | Download Button | - | - | - | Button | - | - | - | - | Download the material file. |
| 16 | View Button | - | - | - | Button | - | - | - | - | View material details (for videos or preview). |
| 17 | Results Count | integer | - | - | Display | - | Calculated | - | `15` | Shows filtered results count. |

