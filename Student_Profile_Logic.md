# 12.0 Student Profile Screen Logic

## Student Profile UI Elements

### Top Navigation Bar

*   **Back Arrow**
    *   Left-pointing arrow icon
    *   Navigate back to previous page

*   **Student Portal Button**
    *   Button with house icon and "Student Portal" text
    *   Navigate to dashboard/home

*   **Notifications Icon**
    *   Bell icon for notifications
    *   Shows badge if unread

*   **Profile Picture**
    *   Circular profile picture
    *   Same image as displayed in profile section

### Student Profile Banner

*   **Banner Title**
    *   Large purple-blue gradient banner
    *   Displays "Student Profile" in large white text
    *   Centered text

*   **Banner Subtitle**
    *   Subtitle below "Student Profile"
    *   Shows "Manage your account information and security settings"
    *   White text, smaller font

### Profile Information Section

*   **Section Header**
    *   Title: "Profile Information" in bold, dark gray text
    *   Positioned below banner

*   **Edit Button**
    *   Blue rectangular button labeled "Edit"
    *   Positioned to the right of "Profile Information" title
    *   Toggles between view and edit modes
    *   Changes to "Save" and "Cancel" buttons in edit mode

### Profile Picture Section

*   **Profile Picture Display**
    *   Circular profile picture
    *   Large size, centered in section
    *   Shows current profile image
    *   Same image as top navigation

*   **Change Photo Button**
    *   Button with upload icon and "Change Photo" text
    *   Positioned below profile picture
    *   Opens file picker for image upload
    *   Only functional in edit mode

*   **Profile Picture Upload**
    *   File input for image selection
    *   Accepted formats: JPG, PNG, GIF
    *   Maximum file size validation
    *   Preview new image before saving

### Profile Details Fields

*   **Full Name Field**
    *   Label: "Full Name"
    *   Read-only text field in view mode
    *   Editable text input in edit mode
    *   Displays student's full name

*   **Username Field**
    *   Label: "Username"
    *   Read-only text field in view mode
    *   Editable text input in edit mode
    *   Displays student's username
    *   Validation for uniqueness if changed

*   **Student ID Field**
    *   Label: "Student ID"
    *   Read-only text field (always)
    *   Cannot be edited
    *   Displays unique student identifier

*   **Curriculum Field**
    *   Label: "Curriculum"
    *   Read-only text field (always)
    *   Cannot be edited
    *   Displays current grade level/section

*   **Academic Year Field**
    *   Label: "Academic Year"
    *   Read-only text field (always)
    *   Cannot be edited
    *   Displays current academic year with "(Current)" indicator

### Edit Mode

*   **Enable Editing**
    *   Click "Edit" button to enter edit mode
    *   Full Name and Username become editable
    *   Change Photo button becomes active
    *   Edit button changes to "Save" and "Cancel" buttons

*   **Save Changes**
    *   Click "Save" button to save changes
    *   Validates all editable fields
    *   Uploads new profile picture if changed
    *   Updates profile information
    *   Returns to view mode
    *   Shows success message

*   **Cancel Editing**
    *   Click "Cancel" button to discard changes
    *   Reverts all fields to original values
    *   Discards uploaded profile picture
    *   Returns to view mode
    *   No confirmation required

### Validation

*   **Field Validation**
    *   Full Name: Required, cannot be empty
    *   Username: Required, cannot be empty, must be unique
    *   Profile Picture: Valid image format, size limits

*   **Error Messages**
    *   Display validation errors below fields
    *   Red text color
    *   Clear, specific error messages

### Data Operations

*   **View Profile**
    *   Display all profile information
    *   Read-only mode by default
    *   Shows current profile picture

*   **Edit Profile**
    *   Enable editing of Full Name and Username
    *   Allow profile picture upload
    *   Save changes to database
    *   Update profile picture file

*   **Change Profile Picture**
    *   Upload new image file
    *   Validate file type and size
    *   Replace existing profile picture
    *   Update in navigation and profile section

