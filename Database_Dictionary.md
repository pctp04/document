# Database Dictionary

**Database:** u875409848_jumaoas  
**Generated from:** ERD Documentation  
**Date:** Generated from ERD Analysis

---

## Table of Contents

1. [activity_logs](#activity_logs)
2. [ai_prompts](#ai_prompts)
3. [custom_blocks](#custom_blocks)
4. [feedback](#feedback)
5. [feedback_responses](#feedback_responses)
6. [forum_categories](#forum_categories)
7. [forum_replies](#forum_replies)
8. [forum_reply_likes](#forum_reply_likes)
9. [forum_thread_likes](#forum_thread_likes)
10. [forum_threads](#forum_threads)
11. [help_article_votes](#help_article_votes)
12. [help_articles](#help_articles)
13. [help_categories](#help_categories)
14. [media_assets](#media_assets)
15. [payment_transactions](#payment_transactions)
16. [plans](#plans)
17. [subscription_logs](#subscription_logs)
18. [support_messages](#support_messages)
19. [support_tickets](#support_tickets)
20. [system_settings](#system_settings)
21. [templates](#templates)
22. [user_plan](#user_plan)
23. [users](#users)
24. [website_analytics](#website_analytics)
25. [websites](#websites)

---

## activity_logs

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| activity_logs | id | int | Unique identifier for each activity log entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| activity_logs | user_id | int | Reference to the user who performed the action (nullable for anonymous actions) | NULL, FOREIGN KEY (users.id) ON DELETE SET NULL |
| activity_logs | action | varchar(100) | Description of the action performed | NOT NULL |
| activity_logs | entity_type | varchar(50) | Type of entity the action relates to | NULL |
| activity_logs | entity_id | int | ID of the entity the action relates to | NULL |
| activity_logs | ip_address | varchar(45) | IP address of the user who performed the action | NULL |
| activity_logs | user_agent | text | User agent string from the browser/client | NULL |
| activity_logs | details | longtext (JSON) | Additional details about the action in JSON format | NULL |
| activity_logs | timestamp | datetime | Date and time when the action occurred | DEFAULT current_timestamp() |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE SET NULL

---

## ai_prompts

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| ai_prompts | id | int | Unique identifier for each AI prompt entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| ai_prompts | user_id | int | Reference to the user who created the prompt | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| ai_prompts | prompt_text | text | The prompt text sent to the AI | NOT NULL |
| ai_prompts | response_text | text | The response text received from the AI | NULL |
| ai_prompts | created_at | datetime | Date and time when the prompt was created | DEFAULT current_timestamp() |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE

---

## custom_blocks

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| custom_blocks | id | int | Unique identifier for each custom block | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| custom_blocks | user_id | int | Reference to the user who created the block | NOT NULL, FOREIGN KEY (users.id) |
| custom_blocks | name | varchar(100) | Name of the custom block | NULL |
| custom_blocks | block_type | varchar(50) | Type/category of the custom block | NULL |
| custom_blocks | html_content | longtext | HTML content of the custom block | NULL |
| custom_blocks | css_content | longtext | CSS content for styling the custom block | NULL |
| custom_blocks | created_at | datetime | Date and time when the block was created | DEFAULT current_timestamp() |

**Foreign Keys:**
- `user_id` → `users(id)`

---

## feedback

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| feedback | id | int | Unique identifier for each feedback entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| feedback | user_id | int | Reference to the user who submitted the feedback | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| feedback | type | varchar(50) | Type/category of the feedback | NOT NULL |
| feedback | message | text | The feedback message content | NOT NULL |
| feedback | priority | enum | Priority level of the feedback | DEFAULT 'medium' (values: 'low', 'medium', 'high') |
| feedback | status | enum | Current status of the feedback | DEFAULT 'open' (values: 'open', 'assigned', 'responded', 'closed') |
| feedback | assigned_to | int | Reference to the admin user assigned to handle this feedback | NULL, FOREIGN KEY (users.id) ON DELETE SET NULL |
| feedback | response | text | Response to the feedback from admin | NULL |
| feedback | created_at | datetime | Date and time when the feedback was created | DEFAULT current_timestamp() |
| feedback | updated_at | datetime | Date and time when the feedback was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE
- `assigned_to` → `users(id)` ON DELETE SET NULL

---

## feedback_responses

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| feedback_responses | id | int | Unique identifier for each feedback response | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| feedback_responses | feedback_id | int | Reference to the feedback being responded to | NOT NULL, FOREIGN KEY (feedback.id) ON DELETE CASCADE |
| feedback_responses | admin_id | int | Reference to the admin user who provided the response | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| feedback_responses | response | text | The response message from the admin | NOT NULL |
| feedback_responses | created_at | datetime | Date and time when the response was created | DEFAULT current_timestamp() |

**Foreign Keys:**
- `feedback_id` → `feedback(id)` ON DELETE CASCADE
- `admin_id` → `users(id)` ON DELETE CASCADE

---

## forum_categories

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| forum_categories | id | int | Unique identifier for each forum category | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| forum_categories | name | varchar(100) | Name of the forum category | NOT NULL |
| forum_categories | description | text | Description of the forum category | NULL |
| forum_categories | icon | varchar(50) | Icon identifier for the category | NULL |
| forum_categories | color | varchar(7) | Color code (hex) for the category | NULL |
| forum_categories | is_active | tinyint(1) | Whether the category is currently active | DEFAULT 1 |
| forum_categories | thread_count | int | Count of threads in this category | DEFAULT 0 |
| forum_categories | last_activity | datetime | Date and time of the last activity in this category | NULL |
| forum_categories | created_at | datetime | Date and time when the category was created | DEFAULT current_timestamp() |
| forum_categories | updated_at | datetime | Date and time when the category was last updated | DEFAULT current_timestamp() ON UPDATE |

---

## forum_replies

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| forum_replies | id | int | Unique identifier for each forum reply | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| forum_replies | thread_id | int | Reference to the forum thread this reply belongs to | NOT NULL, FOREIGN KEY (forum_threads.id) ON DELETE CASCADE |
| forum_replies | author_id | int | Reference to the user who authored the reply | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| forum_replies | content | text | Content of the forum reply | NOT NULL |
| forum_replies | likes | int | Number of likes received by this reply | DEFAULT 0 |
| forum_replies | is_deleted | tinyint(1) | Whether the reply has been deleted (soft delete) | DEFAULT 0 |
| forum_replies | created_at | datetime | Date and time when the reply was created | DEFAULT current_timestamp() |
| forum_replies | updated_at | datetime | Date and time when the reply was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `thread_id` → `forum_threads(id)` ON DELETE CASCADE
- `author_id` → `users(id)` ON DELETE CASCADE

---

## forum_reply_likes

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| forum_reply_likes | id | int | Unique identifier for each like entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| forum_reply_likes | reply_id | int | Reference to the forum reply that was liked | NOT NULL, FOREIGN KEY (forum_replies.id) ON DELETE CASCADE |
| forum_reply_likes | user_id | int | Reference to the user who liked the reply | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| forum_reply_likes | likes | tinyint(4) | Like value (typically 1 for like) | DEFAULT 1 |
| forum_reply_likes | created_at | datetime | Date and time when the like was created | DEFAULT current_timestamp() |
| forum_reply_likes | updated_at | datetime | Date and time when the like was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `reply_id` → `forum_replies(id)` ON DELETE CASCADE
- `user_id` → `users(id)` ON DELETE CASCADE

**Unique Constraints:**
- UNIQUE KEY `unique_user_reply_like` (user_id, reply_id)

---

## forum_thread_likes

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| forum_thread_likes | id | int | Unique identifier for each like entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| forum_thread_likes | thread_id | int | Reference to the forum thread that was liked | NOT NULL, FOREIGN KEY (forum_threads.id) ON DELETE CASCADE |
| forum_thread_likes | user_id | int | Reference to the user who liked the thread | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| forum_thread_likes | likes | tinyint(4) | Like value (typically 1 for like) | DEFAULT 1 |
| forum_thread_likes | created_at | datetime | Date and time when the like was created | DEFAULT current_timestamp() |
| forum_thread_likes | updated_at | datetime | Date and time when the like was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `thread_id` → `forum_threads(id)` ON DELETE CASCADE
- `user_id` → `users(id)` ON DELETE CASCADE

**Unique Constraints:**
- UNIQUE KEY `unique_user_thread_like` (user_id, thread_id)

---

## forum_threads

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| forum_threads | id | int | Unique identifier for each forum thread | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| forum_threads | category_id | int | Reference to the forum category this thread belongs to | NOT NULL, FOREIGN KEY (forum_categories.id) ON DELETE CASCADE |
| forum_threads | author_id | int | Reference to the user who created the thread | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| forum_threads | title | varchar(200) | Title of the forum thread | NOT NULL |
| forum_threads | content | text | Content of the forum thread | NOT NULL |
| forum_threads | views | int | Number of views for this thread | DEFAULT 0 |
| forum_threads | replies_count | int | Count of replies in this thread | DEFAULT 0 |
| forum_threads | likes | int | Number of likes received by this thread | DEFAULT 0 |
| forum_threads | is_pinned | tinyint(1) | Whether the thread is pinned to the top | DEFAULT 0 |
| forum_threads | is_locked | tinyint(1) | Whether the thread is locked from new replies | DEFAULT 0 |
| forum_threads | is_deleted | tinyint(1) | Whether the thread has been deleted (soft delete) | DEFAULT 0 |
| forum_threads | created_at | datetime | Date and time when the thread was created | DEFAULT current_timestamp() |
| forum_threads | updated_at | datetime | Date and time when the thread was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `category_id` → `forum_categories(id)` ON DELETE CASCADE
- `author_id` → `users(id)` ON DELETE CASCADE

---

## help_article_votes

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| help_article_votes | id | int | Unique identifier for each vote entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| help_article_votes | article_id | int | Reference to the help article that was voted on | NOT NULL, FOREIGN KEY (help_articles.id) ON DELETE CASCADE |
| help_article_votes | user_id | int | Reference to the user who cast the vote | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| help_article_votes | vote_type | enum | Type of vote (upvote or downvote) | NOT NULL (values: 'up', 'down') |
| help_article_votes | created_at | datetime | Date and time when the vote was created | DEFAULT current_timestamp() |

**Foreign Keys:**
- `article_id` → `help_articles(id)` ON DELETE CASCADE
- `user_id` → `users(id)` ON DELETE CASCADE

---

## help_articles

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| help_articles | id | int | Unique identifier for each help article | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| help_articles | category_id | int | Reference to the help category this article belongs to | NOT NULL, FOREIGN KEY (help_categories.id) ON DELETE CASCADE |
| help_articles | title | varchar(200) | Title of the help article | NOT NULL |
| help_articles | content | text | Content of the help article | NOT NULL |
| help_articles | author_id | int | Reference to the user who authored the article | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| help_articles | views | int | Number of views for this article | DEFAULT 0 |
| help_articles | helpful_count | int | Count of helpful votes received | DEFAULT 0 |
| help_articles | created_at | datetime | Date and time when the article was created | DEFAULT current_timestamp() |
| help_articles | updated_at | datetime | Date and time when the article was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `category_id` → `help_categories(id)` ON DELETE CASCADE
- `author_id` → `users(id)` ON DELETE CASCADE

---

## help_categories

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| help_categories | id | int | Unique identifier for each help category | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| help_categories | name | varchar(100) | Name of the help category | NOT NULL |
| help_categories | description | text | Description of the help category | NULL |
| help_categories | created_at | datetime | Date and time when the category was created | DEFAULT current_timestamp() |

---

## media_assets

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| media_assets | id | int | Unique identifier for each media asset | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| media_assets | user_id | int | Reference to the user who uploaded the media asset | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| media_assets | filename | varchar(255) | Original filename of the uploaded file | NOT NULL |
| media_assets | file_path | varchar(500) | Path where the file is stored | NOT NULL |
| media_assets | file_type | varchar(50) | MIME type or file extension | NULL |
| media_assets | file_size | int | Size of the file in bytes | NULL |
| media_assets | created_at | datetime | Date and time when the file was uploaded | DEFAULT current_timestamp() |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE

---

## payment_transactions

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| payment_transactions | id | int | Unique identifier for each payment transaction | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| payment_transactions | user_id | int | Reference to the user who made the payment | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| payment_transactions | plan_id | int | Reference to the plan being purchased | NOT NULL, FOREIGN KEY (plans.id) |
| payment_transactions | amount | decimal(10,2) | Amount of the transaction | NOT NULL |
| payment_transactions | status | enum | Status of the payment transaction | DEFAULT 'pending' (values: 'pending', 'completed', 'failed') |
| payment_transactions | transaction_reference | varchar(100) | Unique reference number for the transaction | NOT NULL, UNIQUE |
| payment_transactions | created_at | datetime | Date and time when the transaction was created | DEFAULT current_timestamp() |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE
- `plan_id` → `plans(id)`

**Unique Constraints:**
- UNIQUE KEY on `transaction_reference`

---

## plans

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| plans | id | int | Unique identifier for each subscription plan | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| plans | name | varchar(50) | Name of the subscription plan | NOT NULL |
| plans | type | enum | Type of subscription plan | NOT NULL (values: 'free', 'monthly', 'yearly') |
| plans | price | decimal(10,2) | Price of the subscription plan | NOT NULL |
| plans | features | text | Description of features included in the plan | NULL |
| plans | website_limit | int | Maximum number of websites allowed in this plan | NULL |
| plans | ai_chat_limit | int | Maximum number of AI chat interactions allowed | NULL |
| plans | is_active | tinyint(1) | Whether the plan is currently active and available | DEFAULT 1 |
| plans | created_at | datetime | Date and time when the plan was created | DEFAULT current_timestamp() |

---

## subscription_logs

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| subscription_logs | id | int | Unique identifier for each subscription log entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| subscription_logs | user_id | int | Reference to the user whose subscription is being logged | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| subscription_logs | plan_id | int | Reference to the plan involved in the subscription action | NOT NULL, FOREIGN KEY (plans.id) |
| subscription_logs | action | enum | Type of subscription action performed | NOT NULL (values: 'created', 'upgraded', 'downgraded', 'cancelled', 'renewed') |
| subscription_logs | payment_status | enum | Status of the payment for this subscription action | DEFAULT 'pending' (values: 'pending', 'completed', 'failed') |
| subscription_logs | amount | decimal(10,2) | Amount charged for this subscription action | DEFAULT 0.00 |
| subscription_logs | payment_reference | varchar(100) | Reference number for the payment transaction | NULL |
| subscription_logs | created_at | datetime | Date and time when the subscription log entry was created | DEFAULT current_timestamp() |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE
- `plan_id` → `plans(id)`

---

## support_messages

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| support_messages | id | int | Unique identifier for each support message | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| support_messages | ticket_id | int | Reference to the support ticket this message belongs to | NOT NULL, FOREIGN KEY (support_tickets.id) ON DELETE CASCADE |
| support_messages | sender_id | int | Reference to the user who sent the message | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| support_messages | sender_type | enum | Type of sender (user or admin) | NOT NULL (values: 'user', 'admin') |
| support_messages | message | text | Content of the support message | NOT NULL |
| support_messages | is_internal | tinyint(1) | Whether this is an internal note (not visible to user) | DEFAULT 0 |
| support_messages | created_at | datetime | Date and time when the message was created | DEFAULT current_timestamp() |

**Foreign Keys:**
- `ticket_id` → `support_tickets(id)` ON DELETE CASCADE
- `sender_id` → `users(id)` ON DELETE CASCADE

---

## support_tickets

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| support_tickets | id | int | Unique identifier for each support ticket | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| support_tickets | ticket_number | varchar(20) | Unique ticket number for reference | NOT NULL, UNIQUE |
| support_tickets | user_id | int | Reference to the user who created the ticket | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| support_tickets | subject | varchar(200) | Subject/title of the support ticket | NOT NULL |
| support_tickets | description | text | Detailed description of the issue | NOT NULL |
| support_tickets | priority | enum | Priority level of the ticket | DEFAULT 'medium' (values: 'low', 'medium', 'high') |
| support_tickets | status | enum | Current status of the ticket | DEFAULT 'open' (values: 'open', 'assigned', 'in_progress', 'closed') |
| support_tickets | assigned_to | int | Reference to the admin user assigned to handle this ticket | NULL, FOREIGN KEY (users.id) ON DELETE SET NULL |
| support_tickets | resolution | text | Resolution details for the ticket | NULL |
| support_tickets | created_at | datetime | Date and time when the ticket was created | DEFAULT current_timestamp() |
| support_tickets | updated_at | datetime | Date and time when the ticket was last updated | DEFAULT current_timestamp() ON UPDATE |
| support_tickets | closed_at | datetime | Date and time when the ticket was closed | NULL |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE
- `assigned_to` → `users(id)` ON DELETE SET NULL

**Unique Constraints:**
- UNIQUE KEY on `ticket_number`

---

## system_settings

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| system_settings | id | int | Unique identifier for each system setting | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| system_settings | setting_key | varchar(100) | Unique key identifier for the setting | NOT NULL, UNIQUE |
| system_settings | setting_value | longtext (JSON) | Value of the setting stored in JSON format | NOT NULL |
| system_settings | updated_at | datetime | Date and time when the setting was last updated | DEFAULT current_timestamp() ON UPDATE |
| system_settings | updated_by | int | Reference to the admin user who last updated this setting | NULL, FOREIGN KEY (users.id) ON DELETE SET NULL |

**Foreign Keys:**
- `updated_by` → `users(id)` ON DELETE SET NULL

**Unique Constraints:**
- UNIQUE KEY on `setting_key`

---

## templates

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| templates | id | int | Unique identifier for each template | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| templates | name | varchar(100) | Name of the template | NOT NULL |
| templates | description | text | Description of the template | NULL |
| templates | category | varchar(50) | Category/type of the template | NULL |
| templates | html_base | longtext | Base HTML content of the template | NULL |
| templates | css_base | longtext | Base CSS content of the template | NULL |
| templates | is_featured | tinyint(1) | Whether the template is featured | DEFAULT 0 |
| templates | is_active | tinyint(1) | Whether the template is currently active | DEFAULT 1 |
| templates | is_community | tinyint(1) | Whether this is a community-created template | DEFAULT 0 |
| templates | creator_user_id | int | Reference to the user who created this template | NULL, FOREIGN KEY (users.id) ON DELETE SET NULL |
| templates | source_website_id | int | Reference to the website this template was derived from | NULL, FOREIGN KEY (websites.id) ON DELETE SET NULL |
| templates | created_at | datetime | Date and time when the template was created | DEFAULT current_timestamp() |
| templates | updated_at | datetime | Date and time when the template was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `creator_user_id` → `users(id)` ON DELETE SET NULL
- `source_website_id` → `websites(id)` ON DELETE SET NULL

---

## user_plan

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| user_plan | id | int | Unique identifier for each user plan subscription | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| user_plan | user_id | int | Reference to the user who has this subscription | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| user_plan | plan_id | int | Reference to the subscription plan | NOT NULL, FOREIGN KEY (plans.id) ON DELETE CASCADE |
| user_plan | status | enum | Current status of the subscription | DEFAULT 'active' (values: 'active', 'cancelled', 'expired') |
| user_plan | start_date | datetime | Date and time when the subscription started | DEFAULT current_timestamp() |
| user_plan | end_date | datetime | Date and time when the subscription ends (null for ongoing) | NULL |
| user_plan | created_at | datetime | Date and time when the subscription was created | DEFAULT current_timestamp() |
| user_plan | updated_at | datetime | Date and time when the subscription was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE
- `plan_id` → `plans(id)` ON DELETE CASCADE

---

## users

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| users | id | int | Unique identifier for each user | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| users | username | varchar(50) | Unique username for the user | NOT NULL, UNIQUE |
| users | email | varchar(100) | Unique email address for the user | NOT NULL, UNIQUE |
| users | password_hash | varchar(255) | Hashed password for authentication | NULL |
| users | role | enum | Role of the user in the system | DEFAULT 'user' (values: 'user', 'admin') |
| users | is_verified | tinyint(1) | Whether the user's email has been verified | DEFAULT 0 |
| users | created_at | datetime | Date and time when the user account was created | DEFAULT current_timestamp() |
| users | updated_at | datetime | Date and time when the user account was last updated | DEFAULT current_timestamp() ON UPDATE |

**Unique Constraints:**
- UNIQUE KEY on `username`
- UNIQUE KEY on `email`

---

## website_analytics

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| website_analytics | id | int | Unique identifier for each analytics entry | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| website_analytics | website_id | int | Reference to the website being tracked | NOT NULL, FOREIGN KEY (websites.id) |
| website_analytics | visit_time | datetime | Date and time of the visit | DEFAULT current_timestamp() |
| website_analytics | visitor_ip | varchar(45) | IP address of the visitor | NULL |
| website_analytics | visitor_id | varchar(50) | Unique identifier for the visitor | NULL |
| website_analytics | session_id | varchar(50) | Session identifier for the visit | NULL |
| website_analytics | user_agent | text | User agent string from the visitor's browser | NULL |
| website_analytics | referrer | text | URL of the referring page | NULL |

**Foreign Keys:**
- `website_id` → `websites(id)`

---

## websites

| Table Name | Column | Data Type | Description | Constraints |
|------------|--------|-----------|-------------|-------------|
| websites | id | int | Unique identifier for each website | PRIMARY KEY, NOT NULL, AUTO_INCREMENT |
| websites | user_id | int | Reference to the user who owns this website | NOT NULL, FOREIGN KEY (users.id) ON DELETE CASCADE |
| websites | title | varchar(200) | Title of the website | NOT NULL |
| websites | slug | varchar(200) | Unique URL-friendly identifier for the website | NOT NULL, UNIQUE |
| websites | html_content | longtext | HTML content of the website | NULL |
| websites | css_content | longtext | CSS content for styling the website | NULL |
| websites | template_id | int | Reference to the template used for this website | NULL, FOREIGN KEY (templates.id) ON DELETE SET NULL |
| websites | is_published | tinyint(1) | Whether the website is published and publicly accessible | DEFAULT 0 |
| websites | preview_url | varchar(500) | Preview URL for the website | NULL |
| websites | has_custom_html | tinyint(1) | Whether the website has custom HTML content | DEFAULT 0 |
| websites | has_custom_css | tinyint(1) | Whether the website has custom CSS content | DEFAULT 0 |
| websites | created_at | datetime | Date and time when the website was created | DEFAULT current_timestamp() |
| websites | updated_at | datetime | Date and time when the website was last updated | DEFAULT current_timestamp() ON UPDATE |

**Foreign Keys:**
- `user_id` → `users(id)` ON DELETE CASCADE
- `template_id` → `templates(id)` ON DELETE SET NULL

**Unique Constraints:**
- UNIQUE KEY on `slug`

---

## Summary Statistics

**Total Tables:** 25

**Total Relationships:** 40+ foreign key relationships

**Optional Relationships (NULL allowed):**
1. `activity_logs.user_id` → `users.id`
2. `feedback.assigned_to` → `users.id`
3. `support_tickets.assigned_to` → `users.id`
4. `system_settings.updated_by` → `users.id`
5. `templates.creator_user_id` → `users.id`
6. `templates.source_website_id` → `websites.id`
7. `websites.template_id` → `templates.id`

---

## Data Type Reference

- **int**: Integer (32-bit signed integer)
- **tinyint(1)**: Boolean-like integer (0 or 1)
- **tinyint(4)**: Small integer
- **varchar(n)**: Variable-length string up to n characters
- **text**: Variable-length text string (up to 65,535 characters)
- **longtext**: Very large text string (up to 4GB)
- **decimal(10,2)**: Fixed-point decimal number (10 total digits, 2 after decimal)
- **datetime**: Date and time value
- **enum**: Enumeration type (fixed set of string values)

---

**End of Database Dictionary**

