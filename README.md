# Social Media Application

## Project Overview
This is a full-stack social media application built with a React frontend and a Node.js/Express backend. The app allows users to register, login, create posts with images, like and comment on posts, send and accept friend requests, and generate AI-powered post captions. The backend uses MongoDB for data storage and provides RESTful APIs for client interaction.

## Architecture and Folder Structure
- **client/**: React frontend application
  - `src/`: React components, pages, Redux slices, utilities, and assets
  - `public/`: Static assets and HTML template
- **server/**: Node.js/Express backend API
  - `controllers/`: Request handlers for auth, posts, users
  - `models/`: Mongoose schemas for users, posts, comments, friend requests, etc.
  - `routes/`: API route definitions
  - `middleware/`: Security, error handling, and authentication middleware
  - `dbConfig/`: Database connection setup
  - `utils/`: Utility functions including email sending and JWT handling
  - `views/build/`: Built React app served as static files

## Main Features and Flow
- **User Authentication**: Register, login, email verification, password reset
- **Posts**: Create, delete, like, comment, and reply on posts
- **Friend Requests**: Send, accept, and view friend requests and suggestions
- **Profile**: View and edit user profile, track profile views
- **AI Post Generation**: Generate social media captions using Google Generative AI
- **Routing**: React Router handles navigation with protected routes for authenticated users

## Important Code Highlights
- `client/src/App.js`: Defines routes and layout with authentication guard
- `client/src/pages/Home.jsx`: Main page for creating posts, viewing feed, friend requests, and AI post generation
- `server/index.js`: Express server setup with middleware and route registration
- `server/controllers/authController.js`: Handles user registration and login with password hashing and JWT
- `server/controllers/postController.js`: Manages post creation, retrieval, likes, comments, and deletion
- `server/controllers/userController.js`: Manages user profile, friend requests, email verification, and password reset

## How to Run the Project

### Prerequisites
- Node.js and npm installed
- MongoDB instance running or accessible

### Backend Setup
1. Navigate to the `server` directory:
   ```bash
   cd server
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file with necessary environment variables (e.g., database URI, JWT secret).
4. Start the backend server:
   ```bash
   npm start
   ```
   The server will run on port 8800 by default.

### Frontend Setup
1. Navigate to the `client` directory:
   ```bash
   cd client
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file with necessary environment variables (e.g., API base URL, Google Gemini API key).
4. Start the React development server:
   ```bash
   npm start
   ```
   The app will open in the browser at `http://localhost:3000`.

## How to Test and Use
- Register a new user or login with existing credentials.
- Create posts with text and optional images.
- Like and comment on posts.
- Send and accept friend requests.
- Use the AI post generation feature to create engaging captions.
- Edit your profile and view friend suggestions.

## Additional Notes
- The backend serves the built React app in production from `server/views/build`.
- The app uses Redux for state management and React Router for navigation.
- Security middleware includes Helmet and CORS configuration.
- Error handling middleware captures and formats API errors.
