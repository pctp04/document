# 15.0 Course Materials (Student) Screen Logic

## Course Materials UI Elements

### Filter Section

*   **Curriculum Filter**
    *   Dropdown filter for curriculums
    *   Shows only curriculums student is enrolled in
    *   Default: "All Curriculums"

*   **Subject Filter**
    *   Dropdown filter for subjects
    *   Shows subjects from selected curriculum
    *   Default: "All Subjects"
    *   Updates based on curriculum selection

*   **Material Type Filter**
    *   Dropdown filter by material type
    *   Options: All Types, Lecture Notes, Assignments, Resources, Videos
    *   Default: "All Types"

*   **Search Input**
    *   Real-time search filtering
    *   Searches by material title or description
    *   Case-insensitive search
    *   Updates results as user types

### Materials List Display

*   **Material Card**
    *   Displays material information in card layout
    *   Shows: Material Title, Description (truncated), Type badge, Upload Date
    *   File information: File Name, File Size
    *   Hover effect with elevation

*   **Material Type Badge**
    *   Visual indicator for material type
    *   Color-coded badges:
        *   Lecture Notes: Blue
        *   Assignments: Orange
        *   Resources: Green
        *   Videos: Red

*   **Download Button**
    *   Download material file
    *   Primary button
    *   Shows download progress
    *   Opens file in browser or downloads based on file type

*   **View Button**
    *   View material details or preview
    *   Blue info button
    *   For videos: opens video player
    *   For PDFs: opens PDF viewer
    *   For other files: shows file details

### Material Organization

*   **Grouped by Curriculum**
    *   Materials organized by curriculum
    *   Expandable sections for each curriculum
    *   Shows curriculum name and code

*   **Grouped by Subject**
    *   Within curriculum, materials grouped by subject
    *   Shows subject name and code
    *   Collapsible subject sections

*   **Chronological Order**
    *   Materials sorted by upload date (newest first)
    *   Shows relative time (e.g., "2 days ago")
    *   Option to sort by name or date

### File Handling

*   **File Download**
    *   Direct download link
    *   Supports various file formats:
        *   Documents: PDF, DOC, DOCX
        *   Images: JPG, PNG, GIF
        *   Videos: MP4, AVI
        *   Archives: ZIP, RAR

*   **File Preview**
    *   Preview available for certain file types
    *   PDFs: In-browser viewer
    *   Images: Lightbox preview
    *   Videos: Embedded player

*   **File Size Display**
    *   Shows file size in readable format
    *   Formats: Bytes, KB, MB, GB
    *   Helps students understand download size

### Empty States

*   **No Materials Available**
    *   Displayed when no materials exist for enrolled curriculums
    *   Shows icon, message, and contact teacher information

*   **No Results Match Search**
    *   Displayed when filters return no results
    *   Shows icon, message, and "Reset Filters" button

### Data Operations

*   **View Materials**
    *   Display all available course materials
    *   Filter by curriculum, subject, or type
    *   Search by title or description

*   **Download Materials**
    *   Download individual files
    *   Track download history (optional)
    *   Support for batch download (optional)

*   **View Material Details**
    *   View full material information
    *   See upload date and teacher who uploaded
    *   Preview content if supported

