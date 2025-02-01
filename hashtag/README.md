# CollNet Hashtag Page

CollNet is a social networking platform designed to help users meet new friends and stay connected with family and people of interest anytime, anywhere. This specific module handles hashtag-related functionality within the CollNet ecosystem.

## Features
- Dynamic hashtag-based post search
- Secure session management
- Responsive layout with CSS styling
- Multilingual support
- Dynamic image path handling

## Prerequisites
- PHP 7.x or higher
- MySQL database
- Web server (e.g., Apache, Nginx)

## Installation
1. Clone the repository:
   ```bash
   git clone (https://github.com/TitoLanna/College-Network/tree/main)
   ```
2. Navigate to the project directory:
   ```bash
   cd collnet
   ```
3. Configure the database connection in `config/connect.php`.
4. Ensure `imgs/`, `../imgs/`, or `../../imgs/` directories exist for image assets.
5. Start the server:
   ```bash
   php -S localhost:8000
   ```

## Usage
1. Log in to the platform.
2. Navigate to the hashtag page via URL:
   ```
   http://localhost:8000/path/to/hashtag.php?tag=example
   ```
3. The page will display posts containing the specified hashtag.

## File Structure
- `config/connect.php`: Database connection settings
- `includes/`: Common reusable components (e.g., navbar, time functions)
- `imgs/`: Directory for image assets
- `hashtag.php`: Core script for hashtag functionality

## Security Considerations
- Input sanitization using `htmlentities()` to prevent XSS attacks
- Session validation to restrict unauthorized access
- Prepared statements to prevent SQL injection

## Contribution
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.



## Author
Matthias Anum Otoo

