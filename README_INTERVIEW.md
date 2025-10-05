# Social Media Application - Interview Overview

## Project Description
This project is a full-stack social media application designed to provide users with a platform to connect, share posts, and interact with friends. It features user authentication, post creation with multimedia support, friend management, and AI-powered content generation.

## Technologies Used
- Frontend: React, Redux, React Router, Tailwind CSS
- Backend: Node.js, Express, MongoDB, Mongoose
- Authentication: JWT, password hashing
- AI Integration: Google Generative AI for post caption generation
- Security: Helmet, CORS, error handling middleware

## Key Features
- User registration, login, email verification, and password reset
- Create, like, comment, and delete posts with image upload support
- Send, accept, and manage friend requests
- Profile viewing and editing with friend suggestions
- AI-generated social media captions for enhanced user engagement

## Execution and Testing
1. **Backend**
   - Navigate to the `server` directory.
   - Install dependencies with `npm install`.
   - Configure environment variables in a `.env` file.
   - Start the server using `npm start`.
   - The backend listens on port 8800 and exposes RESTful APIs.

2. **Frontend**
   - Navigate to the `client` directory.
   - Install dependencies with `npm install`.
   - Configure environment variables in a `.env` file (including API base URL and AI API key).
   - Start the React app using `npm start`.
   - The app runs on `http://localhost:3000` and communicates with the backend.

3. **Testing**
   - Manual testing can be performed by interacting with the UI.
   - API endpoints can be tested using tools like Postman.
   - Redux DevTools can be used to inspect state changes.

## Maintenance and Extension
- The project is modular with clear separation between frontend and backend.
- Adding new features involves creating new React components and backend controllers/routes.
- State management is centralized in Redux slices for scalability.
- Security and error handling are implemented globally for robustness.

This project demonstrates full-stack development skills, integration of AI services, and best practices in modern web application architecture.
