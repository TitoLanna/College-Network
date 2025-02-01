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

## Database and Table Management
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

These deletion scripts ensure data integrity and user authentication while preventing unauthorized access or data manipulation within the CollNet platform.

