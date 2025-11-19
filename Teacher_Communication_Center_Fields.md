# 12.0 Communication Center (Teacher) Screen Fields

| No. | FIELD NAME | DATA TYPE | LENGTH | FIELD TYPE | REQUIRED | DEFAULT VALUE | DISPLAY FORMAT | EXAMPLE | REMARKS |
|-----|------------|-----------|--------|------------|----------|--------------|---------------|---------|---------|
| | | MIN | MAX | | | | | | |
| 1 | Message Type Filter | string | - | - | Dropdown | No | All Messages | - | `Sent` | Filter by message type. Options: All Messages, Sent, Received. |
| 2 | Recipient Filter | string | - | - | Dropdown | No | All Recipients | - | `Students` | Filter by recipient type. Options: All Recipients, Students, Parents, Teachers. |
| 3 | Search Input | string | 0 | 255 | Text Input | No | - | - | `assignment` | Search by message subject or content. |
| 4 | Compose Message Button | - | - | - | Button | - | - | - | - | Open compose message form. |
| 5 | Recipient Type | string | - | - | Radio/Dropdown | Yes | - | - | `Individual Student` | Select recipient type: Individual Student, Multiple Students, All Students in Curriculum, Parent. |
| 6 | Recipient Selection | integer | - | - | Multi-select | Yes | - | - | `1, 2, 3` | Select specific recipients (students or parents). |
| 7 | Curriculum Selection | integer | - | - | Dropdown | No | - | - | `1` | Select curriculum to message all students (if applicable). |
| 8 | Message Subject | string | 1 | 200 | Text Input | Yes | - | - | `Assignment Reminder` | Subject line of the message. |
| 9 | Message Body | string | 1 | 2000 | Textarea | Yes | - | - | `Please remember to submit...` | Main content of the message. Rich text editor support. |
| 10 | Attachments | file | - | - | File Upload | No | - | - | `document.pdf` | Attach files to message. Multiple files supported. |
| 11 | Send Button | - | - | - | Button | - | - | - | - | Send message to selected recipients. |
| 12 | Message ID | integer | - | - | Display | - | Auto-generated | - | `1` | Unique identifier for message. |
| 13 | Sender Name | string | - | - | Display | - | - | - | `John Teacher` | Name of message sender. |
| 14 | Recipient Name | string | - | - | Display | - | - | - | `Jane Student` | Name of message recipient. |
| 15 | Message Subject (Display) | string | - | - | Display | - | - | - | `Assignment Reminder` | Subject of message in inbox. |
| 16 | Message Preview | string | - | - | Display | - | - | - | `Please remember to...` | Truncated preview of message content. |
| 17 | Sent Date | datetime | - | - | Display | - | - | Date/Time | `2024-01-15 10:30 AM` | Date and time message was sent. |
| 18 | Read Status | string | - | - | Badge | - | Unread | - | `Read` | Message read status: Read, Unread. |
| 19 | View Message Button | - | - | - | Button | - | - | - | - | View full message content. |
| 20 | Reply Button | - | - | - | Button | - | - | - | - | Reply to received message. |
| 21 | Delete Message Button | - | - | - | Button | - | - | - | - | Delete message with confirmation. |

