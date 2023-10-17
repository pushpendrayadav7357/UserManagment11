
# User Management System

## Frameworks and Language Used


- Database: PostgreSQL
- Language: Java

## Data Flow

### Controller
The controller layer of our application is responsible for handling incoming HTTP requests, processing them, and sending appropriate responses. It utilizes the following functions:

- `registerUser`: Handles user registration by saving user data in the system.
- `loginUser`: Manages user login and authentication, providing access to authorized features.
- `getUserProfile`: Retrieves user profile information.
- `updateUserProfile`: Allows users to update their profile details.
- `deleteUser`: Deletes a user account from the system.
- `getAllUsers`: Fetches a list of all registered users.

### Services
The services layer acts as an intermediary between the controller and the repository. It encapsulates the business logic and performs data validation. It includes the following functions:

- `validateUserData`: Validates user data before user registration.
- `authenticateUser`: Manages user authentication and token generation upon login.
- `authorizeUserAccess`: Ensures that only authorized users can access certain features.
- `encryptPassword`: Secures user passwords by hashing them before storage.
- `sendWelcomeEmail`: Sends a welcome email to newly registered users.

### Repository
The repository layer handles database operations and interactions with our PostgreSQL database. It provides the following functions:

- `createUser`: Saves user data in the database during registration.
- `findUserById`: Retrieves user information by their unique ID.
- `updateUserData`: Updates user details in the database.
- `deleteUserById`: Removes a user's data from the database.
- `findAllUsers`: Retrieves a list of all registered users.

## Database Design

We use a PostgreSQL database to store user-related data. The database includes the following tables:

1. `users`: Contains user information, including their username, email, and hashed password.
2. `user_profiles`: Stores additional user profile details, such as full name, date of birth, and contact information.

## Data Structures Used


- Relational Database: Our system employs a relational database structure to efficiently manage and query user data.

## Project Summary

The User Management System providing user registration, login, and profile management features. User data is securely stored in a PostgreSQL database. The application focuses on ensuring user data security through password encryption and user authorization. It also includes a user-friendly feature of sending welcome emails to new registrants. This project aims to offer robust and secure user management capabilities for various applications and services.
