
Built by https://www.blackbox.ai

---

```markdown
# iSearch Web Application

## Project Overview
iSearch is a web application designed to provide users with functionalities for account management, profile updates, and submission of academic papers. The application leverages Flask as its web framework, SQLAlchemy for database interactions, and Flask-Login for user session management. Users can create accounts, log in, upload documents, and manage their profiles while enjoying secure password hashing and email verification features.

## Installation

### Prerequisites
Before you begin, ensure you have the following installed:
- Python 3.x
- pip (Python package installer)

### Clone the repository
```bash
git clone https://github.com/your-username/isearch.git
cd isearch
```

### Install dependencies
Install the required Python packages using pip:
```bash
pip install -r requirements.txt
```

### Set up the database
Initialize the SQLite database and create the necessary tables by running:
```bash
python init_db.py
```
This will also create an admin user if it does not already exist.

## Usage

### Running the App
To start the Flask application, run the following command:
```bash
python app.py
```
You can access the application by navigating to `http://localhost:8000` in your web browser.

### Endpoints
- **/login:** Login page for existing users.
- **/create_account:** Page for new users to create an account.
- **/user_home:** User dashboard after logging in.
- **/profile:** User profile management page.
- **/logout:** Endpoint for logging out the user.
- **/verify_email/<token>:** Endpoint to verify user email addresses.

## Features
- User authentication (login, logout, registration).
- Profile management including password and email updates.
- Secure password storage using hashing.
- Email verification for email address changes.
- Upload functionality for academic papers (with file type restrictions).
- Admin user creation during database initialization.

## Dependencies
The application requires the following dependencies, which are listed in `requirements.txt`:
- Flask
- Flask-Login
- Flask-SQLAlchemy
- Flask-Migrate
- Werkzeug
- SQLAlchemy

Note: Ensure you have the correct versions of these packages for compatibility.

## Project Structure
```plaintext
iSearch/
│
├── app.py                # Main application script
├── app_backup.py         # Backup version of the application
├── init_db.py            # Script to initialize the database
├── models.py             # SQLAlchemy models for the application
├── requirements.txt       # List of required Python packages
└── templates/            # HTML templates for rendering views
    ├── create_account.html
    ├── login.html
    ├── profile.html
    └── user_home.html
```

## License
This project is licensed under the MIT License - see the LICENSE file for details.
```