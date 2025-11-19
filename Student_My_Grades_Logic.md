# 11.0 My Grades Screen Logic

## My Grades UI Elements

### Top Navigation Bar

*   **Back Arrow**
    *   Left-pointing arrow icon
    *   Navigate back to Student Dashboard

*   **Student Portal Button**
    *   Button with house icon and "Student Portal" text
    *   Navigate to dashboard/home

*   **Notifications Icon**
    *   Bell icon for notifications
    *   Shows badge if unread

*   **Profile Picture**
    *   Circular profile picture
    *   Navigate to Student Profile

### My Grades Banner

*   **Banner Title**
    *   Large purple-blue gradient banner
    *   Displays "My Grades" in large white text
    *   Prominent header section

*   **Student Information**
    *   Subtitle below "My Grades"
    *   Shows "[Student Name] · [Grade Level]"
    *   White text, smaller font

### Academic Grades Section

*   **Section Header**
    *   Title: "Academic Grades" in dark gray text
    *   Positioned below banner

*   **Term Filter Dropdown**
    *   Dropdown labeled "All Terms" with down arrow
    *   Options: All Terms, Prelim, Midterm, Semifinal, Final
    *   Filters displayed grades by term
    *   Default: "All Terms"
    *   Positioned to the right of "Academic Grades" heading

### Course Grade Cards

*   **Course Card**
    *   White rounded card for each course
    *   Shows course name in bold (e.g., "Mathematics 10")
    *   Shows course code below name (e.g., "MATH1001")
    *   Expandable/collapsible to show grade components

*   **Expand/Collapse Button**
    *   Orange square button with white horizontal dash/minus icon
    *   Toggles course grade details visibility
    *   Icon changes when expanded/collapsed
    *   Positioned on right side of course card

*   **Comments Button**
    *   Gray square icon with speech bubble
    *   Opens comments or notes for the course
    *   Positioned next to expand/collapse button

*   **Grade Components List**
    *   Displayed when course card is expanded
    *   Each component on separate line with light gray background
    *   Components: Prelim, Midterm, Semifinal, Final, Final Grade
    *   Shows grade value or dash "-" if not graded
    *   Final Grade line highlighted with light blue background when selected

*   **Grade Display**
    *   Each grade component shows:
        *   Component name (Prelim, Midterm, etc.)
        *   Grade value (numeric) or dash "-"
    *   Grades displayed to the right of component name
    *   Final Grade highlighted when focused/selected

### Empty States

*   **No Grades Available**
    *   Displayed when no courses have grades
    *   Shows message indicating grades will appear when available

*   **No Results for Term Filter**
    *   Displayed when selected term has no grades
    *   Shows message and option to change filter

### Data Operations

*   **Filter by Term**
    *   Select term from dropdown
    *   Filter displayed grades by selected term
    *   Update course cards to show only relevant grades
    *   "All Terms" shows all grade components

*   **View Grade Details**
    *   Expand course card to view all grade components
    *   Collapse to show only course summary
    *   Toggle expand/collapse state

*   **View Comments**
    *   Click comments button
    *   View teacher comments or notes for course
    *   Opens comments modal or section

### Grade Calculations

*   **Final Grade Calculation**
    *   Calculated from component grades (Prelim, Midterm, Semifinal, Final)
    *   May use weighted average if weights assigned
    *   Updates automatically when component grades change

*   **Display Format**
    *   Grades shown as numeric values (0-100)
    *   Decimal values supported
    *   Dash "-" displayed if grade not yet entered

