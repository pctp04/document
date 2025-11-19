# 18.0 Messaging Center (Student) Screen Logic

## Messaging Center UI Elements

### Filter Section

*   **Message Type Filter**
    *   Dropdown filter for message type
    *   Options: All Messages, Sent, Received
    *   Default: "All Messages"
    *   Separates sent and received messages

*   **Sender Filter**
    *   Dropdown filter by sender type
    *   Options: All Senders, Teachers, Students, System
    *   Default: "All Senders"
    *   Filters messages by sender category

*   **Search Input**
    *   Real-time search filtering
    *   Searches by message subject or content
    *   Case-insensitive search
    *   Updates results as user types

### Compose Message Form

*   **Compose Message Button**
    *   Opens compose message modal/form
    *   Primary button in page header
    *   Clears form for new message

*   **Recipient Type Selection**
    *   Radio buttons or dropdown
    *   Options: Teacher, Student, All Students in Curriculum
    *   Required selection
    *   Changes available recipient options

*   **Recipient Selection**
    *   Dropdown or multi-select
    *   Shows teachers or students based on recipient type
    *   Required if individual recipient selected
    *   Searchable dropdown for large lists

*   **Curriculum Selection**
    *   Dropdown (shown when "All Students in Curriculum" selected)
    *   Shows curriculums student is enrolled in
    *   Required for curriculum-wide messages

*   **Message Subject**
    *   Required text input
    *   Maximum 200 characters
    *   Placeholder: "Enter message subject"

*   **Message Body**
    *   Required textarea
    *   Maximum 2000 characters
    *   Rich text editor support (optional)
    *   Character counter display

*   **Attachments**
    *   File upload input
    *   Multiple files supported
    *   Accepted formats: PDF, DOC, DOCX, images
    *   Maximum file size: 10MB per file
    *   Shows list of attached files

*   **Send Button**
    *   Send message to selected recipient
    *   Primary button
    *   Validates all required fields
    *   Shows loading state during send
    *   Confirmation message on success

### Message Inbox Display

*   **Message List**
    *   Displays messages in list or card layout
    *   Shows: Sender/Recipient Name, Subject, Preview, Sent Date, Read Status
    *   Color-coded by read status (unread messages highlighted)
    *   Hover effect with elevation

*   **Read Status Badge**
    *   Visual indicator for message status
    *   Green badge for read messages
    *   Blue badge for unread messages
    *   Badge count in inbox header

*   **View Message Button**
    *   Opens message detail view
    *   Blue info button
    *   Marks message as read when viewed
    *   Shows full message content and attachments

*   **Reply Button**
    *   Opens reply form (for received messages)
    *   Green button
    *   Pre-fills recipient and subject
    *   Includes original message in reply

*   **Delete Message Button**
    *   Delete message permanently
    *   Red danger button
    *   Requires confirmation modal
    *   Removes from inbox

### Message Detail View

*   **Full Message Display**
    *   Shows complete message content
    *   Displays sender/recipient information
    *   Shows sent date and time
    *   Lists all attachments with download links

*   **Attachment Download**
    *   Download attached files
    *   Shows file name and size
    *   Download button for each file

*   **Reply Functionality**
    *   Quick reply option
    *   Pre-filled form with recipient
    *   Includes original message reference

### Data Operations

*   **Compose and Send Message**
    *   Create new message
    *   Select recipient (teacher or student)
    *   Enter subject and body
    *   Attach files (optional)
    *   Send message
    *   Notification sent to recipient

*   **View Messages**
    *   Display inbox with all messages
    *   Filter by type, sender, or search
    *   Mark as read when viewed
    *   Unread count updates automatically

*   **Reply to Message**
    *   Reply to received messages
    *   Pre-fills recipient information
    *   Includes original message context
    *   Send reply

*   **Delete Messages**
    *   Delete sent or received messages
    *   Permanent deletion
    *   Requires confirmation
    *   Updates inbox count

### Notifications

*   **New Message Notification**
    *   Badge showing unread count
    *   Real-time updates (if WebSocket/SignalR implemented)
    *   Email notification (optional)

*   **Message Sent Confirmation**
    *   Success message after sending
    *   Confirms message delivery
    *   Shows recipient name

