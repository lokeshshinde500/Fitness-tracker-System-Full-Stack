sorry , i dont know but my backend not show in this directory please refer this repo link for backend code.
backend repo : https://github.com/lokeshshinde500/Fitness-tracker-System-Backend

## Frontend API URL

## Backend API URL

https://fitness-tracker-system-backend.onrender.com/

### Sample creadentials for login

email : a@gmail.com
role : admin
Pasaword : 123

# API Endpoints Documentation

This document outlines the available API endpoints for the fitness program application.

## Authentication Routes

### POST /auth/register

- **Description**: Register a new user.
- **Request Body**:
  - `name`: String
  - `email`: String
  - `role`: admin / user
  - `password`: String

### POST /auth/login

- **Description**: Log in a user and return a token.
- **Request Body**:
  - `name`: String
  - `role`: admin / user
  - `password`: String

### GET /auth/profile

- **Description**: Get the authenticated user's profile.
- **Authentication Required**: Yes (Token required)

## Admin Routes

### GET /admin/users

- **Description**: Get all users (excluding admins).

### GET /admin/:id/user

- **Description**: Get a single user by their ID.

### POST /admin/fitnessProgram

- **Description**: Create a new fitness program.
- **Request Body**:
  - Program details (varies based on implementation)

### GET /admin/fitnessProgram

- **Description**: View all fitness programs.

### GET /admin/fitnessProgram/admin

- **Description**: View fitness programs created by admin.

### GET /admin/:id/fitnessProgram

- **Description**: View a single fitness program by ID.

### DELETE /admin/:id/fitnessProgram

- **Description**: Delete a fitness program by ID.

### PATCH /admin/:id/fitnessProgram

- **Description**: Update a fitness program by ID.
- **Request Body**:
  - Updated program details (varies based on implementation)

## User Routes

### POST /user/goals

- **Description**: Create a new goal.
- **Request Body**:
  - Goal details (varies based on implementation)

### GET /user/goals

- **Description**: Get all goals for the authenticated user.

### GET /user/goals/:id

- **Description**: Get a single goal by ID.

### DELETE /user/goals/:id

- **Description**: Delete a goal by ID.

### PATCH /user/goals/:id

- **Description**: Update a goal by ID.
- **Request Body**:
  - Updated goal details (varies based on implementation)

## Middleware

- **authenticate**: Ensures the user is authenticated.
- **isAdmin**: Ensures the user is an admin.

## Notes

- All admin routes require authentication and admin privileges.

# Project Dependencies

This document lists the dependencies used in the project, along with a brief description of each.

## Dependencies

1. **bcrypt**: `^5.1.1`

   - A library to help hash passwords and manage secure password storage.

2. **cors**: `^2.8.5`

   - Middleware for enabling Cross-Origin Resource Sharing (CORS) in your Express application, allowing you to configure which origins can access your API.

3. **dotenv**: `^16.4.5`

   - A module that loads environment variables from a `.env` file into `process.env`, facilitating configuration management.

4. **express**: `^4.21.1`

   - A fast, unopinionated, minimalist web framework for Node.js, used to build APIs and web applications.

5. **jsonwebtoken**: `^9.0.2`

   - A library for generating and verifying JSON Web Tokens (JWT), which are commonly used for authentication and authorization in web applications.

6. **mongodb**: `^6.9.0`

   - The official MongoDB driver for Node.js, allowing you to connect and interact with MongoDB databases.

7. **mongoose**: `^8.7.1`
   - An Object Data Modeling (ODM) library for MongoDB and Node.js, providing a schema-based solution to model your application data.

## Installation

To install all dependencies:

### bash command

npm install

### Run code

Frontend : npm run dev

Backend : npm run dev
