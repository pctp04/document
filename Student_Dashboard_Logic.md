# 10.0 Student Dashboard Screen Logic

## Student Dashboard UI Elements

### Top Navigation Bar

*   **Back Arrow**
    *   Left-pointing arrow icon
    *   Navigate back to previous page

*   **Student Portal Button**
    *   Button with house icon and "Student Portal" text
    *   Navigate to dashboard/home
    *   Light gray/purple background

*   **Notifications Icon**
    *   Bell icon on the right
    *   Shows notification badge if unread notifications exist
    *   Click to view notifications

*   **Profile Picture**
    *   Circular profile picture on the right
    *   Shows student's profile image
    *   Click to navigate to Student Profile

### Welcome Banner

*   **Welcome Message**
    *   Large purple-blue gradient banner
    *   Displays "Welcome back, [Student Name]!"
    *   White, bold text
    *   Personalized greeting

*   **Grade Level Display**
    *   Subtitle below welcome message
    *   Shows "Here's an overview of your academic progress for [Grade Level]"
    *   White text, smaller font

### Academic Summary Cards

*   **Overall Average Card**
    *   White rounded card
    *   Label: "Overall Average"
    *   Value: Calculated average grade or dash "-" if no grades
    *   Displays percentage or letter grade

*   **Subjects Card**
    *   White rounded card
    *   Label: "Subjects"
    *   Value: Count of enrolled subjects
    *   Shows total number of subjects

*   **Academic Year Card**
    *   White rounded card
    *   Label: "Academic Year"
    *   Value: Current academic year (YYYY-YYYY format)
    *   Shows active academic period

### My Subjects Section

*   **Section Header**
    *   Title: "My Subjects" in bold, dark text
    *   Subtitle: "View the subjects assigned to your curriculum"
    *   Smaller, lighter text

*   **Subject Card**
    *   White rounded card for each subject
    *   Left side: Small colored icon/badge (orange square with dash)
    *   Middle section:
        *   Subject name in bold (e.g., "Mathematics 10")
        *   Clock icon followed by semester and academic year
        *   Subject description text
    *   Right side:
        *   Final Grade display (shows "-Final Grade" if not graded)
        *   Document/list icon
    *   Hover effect with elevation
    *   Click to view subject details or navigate to grades

*   **Subject Information Display**
    *   Subject Name: Bold, prominent text
    *   Semester and Academic Year: Small text with clock icon
    *   Description: Brief description of subject content
    *   Final Grade: Shows grade if available, or "-" if not graded

### Navigation

*   **Sidebar Navigation**
    *   ELASI logo/brand at top
    *   Navigation menu items (if expanded)
    *   Collapsible sidebar

*   **My Grades Navigation**
    *   Accessible via navigation menu or subject cards
    *   Navigate to My Grades screen (11.0)

*   **Student Profile Navigation**
    *   Accessible via profile picture or navigation menu
    *   Navigate to Student Profile screen (12.0)

*   **Student Report Navigation**
    *   Accessible via navigation menu
    *   Navigate to Student Report screen (13.0)

*   **Logout**
    *   Clear session and redirect to unified Login screen

### Data Operations

*   **View Subject Details**
    *   Click subject card to view details
    *   Navigate to subject-specific grades or information
    *   Shows full subject information

*   **Calculate Overall Average**
    *   Calculate from all subject final grades
    *   Exclude subjects without grades
    *   Display as percentage or letter grade
