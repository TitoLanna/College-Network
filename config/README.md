# CollNet Project

## Overview
CollNet is a PHP-based web application that connects to a MySQL database. It includes multilingual support, user session management, and verification badge functionality.

## Prerequisites
- PHP 7.0 or higher
- MySQL Database
- Apache or NGINX server

## Database Configuration
1. **Database Name:** `CollNet`
2. **Default Credentials:**
   - **Server Name:** `localhost`
   - **Username:** `root`
   - **Password:** *(empty)*

Ensure your MySQL server has a database named `CollNet`.

## Installation
1. Clone the repository:
   ```bash
   git clone <(https://github.com/TitoLanna/College-Network/tree/main)>
   ```
2. Navigate to the project directory.
3. Place the project files in your web server’s root directory (e.g., `htdocs` for XAMPP).
4. Start your Apache and MySQL servers.

## Configuration
- **Database Connection:** Configured in the `config.php` file.
- **Language Settings:** Managed via `langs/set_lang.php`.
- **Session Management:** Handled in the main PHP script.

## Features
- **Database Connection:** Uses PDO with error handling.
- **Multilingual Support:** Dynamically loads language files.
- **User Verification Badge:** Displays a verified icon for verified users.
- **Session Validation:** Automatically logs out users with deleted accounts.

## Usage
1. Open your browser and go to `http://localhost/CollNet`.
2. Login or register to access features.

## Troubleshooting
- **Database Connection Failed:** Check your MySQL credentials and ensure the server is running.
- **Session Issues:** Verify PHP sessions are enabled in your `php.ini` file.




