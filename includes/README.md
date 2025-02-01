# CollNet Project - Include Section README

## Overview
The **Include Section** of the CollNet project manages core functionalities essential for the platform's operation. It handles session control, database connectivity, time functions, and post-fetching mechanisms, ensuring seamless integration across different components of the social network.

## Included Files
- **GeT_login_whileFetch.php**: 
- **country_name_function.php**: 
- **dbqueries.php**: 
- **deleteSavedPost.php**: 
- **deletecomm.php**:
- **deletepost.php**:
- **emoticons.php**:
- **emoticons_c_m.php**:
- **endJScodes.php**:
- **f_action.php**:
- **fetchTrending.php**:
- **fetch_comments.php**:
- **fetch_notifybox.php**: 
- **fetch_posts.php**:
- **fetch_posts_home.php**:
- **fetch_posts_saved.php**:
- **fetch_posts_user.php**:
- **fetch_user_info.php**:
- **footer.php**:
- **footer_white.php**:
- **head_imports_main.php**:
- **index.php**:
- **insert_commentdb.php**:
- **lac.php**:
- **login_signup_codes.php**:
- **m_requests.php**:
- **myphotosProfile.php**:
- **navbar_main.php**:
- **num_k_m_count.php**:
- **r_star.php**:
- **report.php**:
- **searchq.php**:
- **send_saved_postDB.php**:
- **share.php**:
- **time_function.php**:
- **updatecomment.php**:
- **updatepost.php**:
- **uploadcoverphoto.php**:
- **uploadprofilephoto.php**:
- **userStatus.php**:
- **w_post_form.php**:
- **wpost.php**:
- **ytframe.php**:

## User Session Handling
This section manages user sessions by fetching user data from the database and storing it in PHP session variables. It includes personal details such as user ID, full name, username, email, password, profile and cover photos, school, work, country, birthday, verification status, website, biography, admin status, gender, profile picture border, language preference, and online status.

The system also includes logic to standardize gender representation and ensure secure authentication across user sessions.

## Country Data Management
The **Include Section** also incorporates a predefined list of countries with their corresponding ISO country codes. This feature facilitates the standardization of country information in user profiles and supports functionalities that require geographical data.

## Database and Table Management[**dbqueries.php**]
The **Include Section** also includes scripts for database creation and table management within the CollNet project. These PHP functions handle the initialization of the database and the creation of essential tables:

- **CreatecollegenetDB()**: Initializes the `collegenet` database.
- **CreateuserTB()**: Creates the `users` table to store user information, including credentials, contact details, verification status, and profile images.
- **CreatedepartmentTB()**: Establishes the `department` table to manage academic department data.
- **CreatedepartmentclassTB()**: Sets up the `departmentclass` table to link classes with departments.
- **CreateclassTB()**: Creates the `Class` table to store information about different classes.
- **CreatePostTB()**: Defines the `Post` table for user-generated content, including text messages and images.
- **createChatTB()**: Sets up the `Chat` table for managing chat messages within the platform.

These functions ensure the necessary data structures are in place to support user interactions, academic data organization, and communication features on CollNet.

## Data Deletion Handling
The **Include Section** also provides functionality for managing data deletion within the CollNet project. Specific scripts are responsible for securely deleting items from the database:

- **delete_saved.php**: This script deletes a saved item based on its ID. It sanitizes the input using `FILTER_SANITIZE_NUMBER_INT` to prevent injection attacks, prepares the SQL delete statement with placeholders to ensure security, and executes the deletion using prepared statements.

- **delete_comment.php**: This script handles the deletion of comments. It verifies that the user requesting deletion is the original author of the comment by checking session data and matching it with the comment's author ID in the database. If the verification is successful, the comment is securely deleted using a prepared SQL statement; otherwise, the deletion request is denied.
- **deletepost.php**: Handles the deletion of posts from the database. It verifies if the current user (session ID) is the author of the post before allowing deletion. Additionally, it removes associated 'like' and 'comment' notifications related to the post.

These deletion scripts ensure data integrity and user authentication while preventing unauthorized access or data manipulation within the CollNet platform.

## Emoji Reaction Feature
This[- **emoticons.php**, **emoticons_c_m.php**] PHP script dynamically generates a set of emoji reaction icons for comments. It retrieves the image path and the comment ID from the POST request and displays clickable emoji icons. When an emoji is clicked, it triggers the cEmoji() JavaScript function, passing the comment ID and the selected emoji.
## Network Interactive Features[endJScodes.php]
The use of jQuery AJAX for asynchronous requests, enabling real-time updates and server communication without page reloads.The code uses PHP for server-side variables and paths, while JavaScript (with jQuery) handles the frontend interactions and dynamic content updates.
- **Post Management**:Fetch, like/unlike, edit, save, delete, comment, share, and report posts.
- **User Interactions**:Follow/unfollow users, upload/manage profile and cover photos, rate pages, and search for users.
- **Messaging System**:Real-time messaging, typing indicators, message seen status, emoji support, contact list management, and message search.
- **UI Features**:Image lightbox, loading indicators, error handling, emoji picker, and comment editing.
Ajax Implementation:
  ## Follow/Unfollow Functionality[**f_action.php**]
This PHP script implements a **Follow/Unfollow** feature, allowing users to follow or unfollow other users. It performs the following actions:
- **Session Handling & Input Validation**: The user ID is fetched and sanitized from the POST request.  
- **Follow/Unfollow Logic**:
   - If the user is already following, it removes the follow record, updates the follower count, and deletes any follow-related notifications.
   - If the user is not following, it adds the follow record, updates the follower count, and sends a notification to the target user.  
- **Button Update**: After each action, the follow button is updated with either "Follow" or "Following".
- **Notification**: A notification is sent to the target user when someone follows them.
The script enables dynamic following, unfollowing, updating of follower counts, and managing notifications without page reloads.

## Fetch Section

- **fetchTrending.php**: Displays the top 6 users by follower count, including profile images, full names, usernames, and a verification badge for verified users.

- **fetch_comments.php**: Retrieves comments for a specific post based on the post ID. For each comment, it fetches the comment content, time, and author details (including profile picture, username, and verification status). The content is processed to replace emoticons and hashtags with appropriate links. Additionally, it checks if the comment was edited and displays the time of the last edit. Each comment includes options to edit or delete (if the comment author is the current user), and a report option if the comment author is someone else.

- **fetch_notifybox.php**: Handles notifications for the logged-in user, fetching and displaying notifications based on their type (like, comment, share, star, follow). Notifications are marked as seen and displayed with user details, including profile image, post content, and time. The script checks for unseen notifications and returns the count of those notifications. It fetches relevant information for each notification type, such as post content for likes and shares, and user details for follows and stars.

- **fetch_posts.php**: Fetches posts from the database, displaying user profile photo, username, timestamp, post content, and interaction counts (like, comment, share). The posts include privacy settings (public, followers, private) and support actions like like/unlike, comment system with emoji support, post sharing, and editing. The posts are formatted with text, hashtags, URLs, and embedded content (e.g., YouTube videos). The timestamp is converted to a "time ago" format, and privacy indicators (globe, lock icons) show post privacy. Special features like image lightbox functionality are also supported.

- **fetch_posts_home.php**: Fetches posts for the home feed by retrieving posts made by users the logged-in user follows and their own posts. The posts are filtered based on privacy settings, with posts from followed users and the logged-in user displayed. It uses a limit to fetch posts and includes functionality to view them. If no posts are found, it returns "0".

- **fetch_posts_saved.php**: Retrieves saved posts for the logged-in user. The posts are fetched in descending order of the saved time. It displays post content, user information, and allows the user to delete saved posts. Each saved post includes the author's name, username, a link to view the full post, and an option to remove the post from saved posts.

- **fetch_posts_user.php**: Retrieves posts specific to a user, considering their follower status and privacy settings. It checks if the logged-in user follows the target user and adjusts the post visibility accordingly. The posts are fetched with privacy restrictions, displaying only public or followers' posts. If the user has no posts, it returns "0".

- **fetch_user_info.php**: Fetches detailed user information, including the user's ID, full name, username, email, password, profile pictures (user photo and cover photo), work, school, country, birthday, verification status, website, biography, and language. It also includes admin status and online presence.


