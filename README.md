# User Management System

This project is a user management system that includes user registration, login, and user information management functionalities. It is built using Spring Boot for the backend and Vue3 for the frontend.

## Features

1. **User Registration and Login**
   - Internal employees log in using their employee number, name, and department.
   - External employees register using their name, date of birth, contact information, and store code.
   - Users can update their personal information, such as name, email, phone number, store code, and password.
   - Consent form for personal information usage and dormant account management feature during the first login.

2. **User Information Management**
   - View, edit, and register user details.
   - Update existing employee information, such as department transfers or position changes.
   - Record the history of user information modifications.
   - Change user permissions, allowing specific users to be switched to different roles.
   - Bulk user registration and course enrollment functionality.
   - Monitor and control learners' teaching and learning activities.
   - View and search user login status and monitor login activity.

3. **Role-based Access Control**
   - Manage user roles and permissions.
   - Assign either administrator or general user roles to users.
   - Administrators can modify or delete other users' information.
   - User interface for administrators to manage user roles and permissions easily.

## System Requirements

- Maven for building the project.
- Spring Boot for the backend.
- Vue3 for the frontend.
- HSQLDB for the database.

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/githubnext/workspace-blank.git
   cd workspace-blank
   ```

2. **Backend Setup:**
   - Navigate to the `backend` directory:
     ```bash
     cd backend
     ```
   - Build the backend project using Maven:
     ```bash
     mvn clean install
     ```
   - Run the Spring Boot application:
     ```bash
     mvn spring-boot:run
     ```

3. **Frontend Setup:**
   - Navigate to the `frontend` directory:
     ```bash
     cd ../frontend
     ```
   - Install the dependencies:
     ```bash
     npm install
     ```
   - Run the Vue3 application:
     ```bash
     npm run serve
     ```

## Running the Project

1. **Start the backend server:**
   ```bash
   cd backend
   mvn spring-boot:run
   ```

2. **Start the frontend server:**
   ```bash
   cd frontend
   npm run serve
   ```

3. **Access the application:**
   - Open your web browser and navigate to `http://localhost:8080` for the backend API.
   - Open your web browser and navigate to `http://localhost:8081` for the frontend application.

## License

This project is licensed under the MIT License.
