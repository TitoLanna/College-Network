# README.md

## Overview
This SQL dump was generated using **phpMyAdmin (version 4.9.0.1)**, compatible with **MariaDB Server version 10.4.6** and **PHP version 7.3.9**. The dump contains the schema for a database named `sn`, which appears to support functionalities commonly found in social networking platforms.

## Database Details
- **Database Name:** `sn`
- **Host:** `localhost`
- **Generation Time:** September 14, 2019, at 03:42 PM (UTC)

## SQL Settings
- **SQL Mode:** `NO_AUTO_VALUE_ON_ZERO`
- **Autocommit:** Disabled (set to 0)
- **Time Zone:** `+00:00`
- **Character Set:** UTF-8 (`utf8mb4`) and Latin1 for specific tables

## Tables Included

### 1. `comments`
- **Description:** Stores user comments associated with posts.
- **Key Fields:**
  - `c_id`: Unique identifier for each comment.
  - `c_author_id`: ID of the user who wrote the comment.
  - `c_post_id`: ID of the post the comment belongs to.
  - `c_content`: The actual comment content.
  - `c_edited`: Indicates if the comment has been edited (0 = No, 1 = Yes).
  - `c_time_edited`: Timestamp of the last edit.
  - `c_time`: Timestamp when the comment was created.

### 2. `follow`
- **Description:** Manages user follow relationships.
- **Key Fields:**
  - `id`: Unique identifier for the follow record.
  - `uf_one`: ID of the user who is following.
  - `uf_two`: ID of the user being followed.

### 3. `likes`
- **Description:** Records likes on posts.
- **Key Fields:**
  - `id`: Unique identifier for each like.
  - `liker`: ID of the user who liked the post.
  - `post_id`: ID of the liked post.

### 4. `messages`
- **Description:** Stores direct messages between users.
- **Key Fields:**
  - `id`: Unique identifier for each message.
  - `m_id`: Message thread identifier.
  - `message`: The message content.
  - `m_from`: ID of the sender.
  - `m_to`: ID of the recipient.
  - `m_time`: Timestamp when the message was sent.
  - `m_seen`: Indicates if the message has been read (0 = No, 1 = Yes).

### 5. `mynotepad`
- **Description:** A personal note-taking feature for users.
- **Key Fields:**
  - `main_id`: Primary key for each note.
  - `id`: Identifier for the note.
  - `author_id`: ID of the user who created the note.
  - `note_title`: Title of the note.

## Import Instructions
1. Open **phpMyAdmin**.
2. Select or create a database named `sn`.
3. Click on the **Import** tab.
4. Upload the SQL file and click **Go**.

## Compatibility Notes
- Ensure that your MariaDB and PHP versions are compatible with the versions used during the dump.
- Modify character sets or SQL modes if necessary to match your server configuration.

## License
This SQL dump is provided as-is. Ensure compliance with data privacy regulations if the data is real.

---
*Generated on September 14, 2019, using phpMyAdmin 4.9.0.1*

