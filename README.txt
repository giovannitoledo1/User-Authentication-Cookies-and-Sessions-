User Authentication with Cookies and Sessions
Project Overview
This project is a Node.js application that demonstrates user registration, login, and authentication using bcrypt hashing, sessions, and cookies. Built with Express and PostgreSQL, it securely manages user credentials and preserves authentication status across browsing sessions using Passport.js and express-session.

Key Features
User Registration and Login:

Allows users to register with a unique email and password, which is securely hashed and stored in the database.
Passwords are hashed using bcrypt with a defined salt round for added security.
Session Management:

Implements express-session for session persistence with cookies, allowing users to remain authenticated across multiple requests.
Sessions expire based on defined maxAge in milliseconds, which is set to 1 day.
Persistent Authentication with Passport.js:

Passport and passport-local manage the authentication workflow.
Serializes and deserializes user information, enabling session-based login status.
Protects routes by ensuring only authenticated users can access certain pages.
File Structure
app.js: Main server file that defines all routes, session setup, and authentication.
public/: Directory for static assets like CSS and images.
views/: EJS templates for rendering pages like login, register, and secrets.
Getting Started
Prerequisites
Node.js and npm
PostgreSQL
Installation
Clone the repository:

bash
Copy code
git clone [repository URL]
Install dependencies:

bash
Copy code
npm install
Set up environment variables in a .env file:

DB_USER: Your PostgreSQL username
DB_PASSWORD: Your PostgreSQL password
DB_HOST: Database host (usually localhost)
DB_NAME: Name of the PostgreSQL database
Start the server:

bash
Copy code
node app.js
Usage
Navigate to the registration page to create a new account.
Login with your registered credentials to access the /secrets page.
Your session will persist as long as the browser is open or until you log out.
Dependencies
express: Web server framework
body-parser: Parses incoming request bodies
pg: PostgreSQL client
bcrypt: For password hashing
express-session: For session management with cookies
passport and passport-local: For authentication and session persistence
License
This project is licensed under the MIT License.