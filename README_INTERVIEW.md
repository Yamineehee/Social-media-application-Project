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

## Interview Ready Prep Questions

### Node.js Theory Questions
1. **What is Node.js?**  
   Node.js is a runtime environment that allows JavaScript to run on the server-side. It uses the V8 engine from Chrome and provides non-blocking I/O operations, making it efficient for scalable applications.

2. **Explain the event loop in Node.js.**  
   The event loop is the core mechanism that handles asynchronous operations. It continuously checks the call stack and message queue, executing callbacks when the stack is empty, enabling non-blocking I/O.

3. **What is npm?**  
   npm (Node Package Manager) is the default package manager for Node.js, used to install, manage, and share JavaScript packages and dependencies.

4. **How does Node.js handle concurrency?**  
   Node.js uses a single-threaded event loop with asynchronous I/O, allowing it to handle multiple connections concurrently without creating new threads for each request.

5. **What are streams in Node.js?**  
   Streams are objects that allow reading or writing data in chunks, useful for handling large files or real-time data without loading everything into memory.

### JavaScript Detailed Questions
1. **Explain closures in JavaScript.**  
   A closure is a function that has access to its own scope, the outer function's scope, and the global scope. It allows inner functions to access variables from their containing functions even after the outer function has returned.

2. **What is the difference between `var`, `let`, and `const`?**  
   - `var` is function-scoped and can be redeclared.  
   - `let` is block-scoped and can be reassigned but not redeclared in the same scope.  
   - `const` is block-scoped and cannot be reassigned or redeclared.

3. **What are promises and async/await?**  
   Promises represent the eventual completion of an asynchronous operation. Async/await is syntactic sugar for promises, allowing asynchronous code to be written synchronously.

4. **Explain prototypal inheritance.**  
   In JavaScript, objects inherit properties and methods from other objects through prototypes. Each object has a prototype chain that it follows to find properties.

5. **What is the `this` keyword?**  
   `this` refers to the object that is executing the current function. Its value depends on how the function is called (e.g., method call, function call, constructor).

### API Writing Questions
1. **How to create a basic REST API in Express?**  
   ```javascript
   const express = require('express');
   const app = express();
   app.use(express.json());

   app.get('/api/users', (req, res) => {
     // Logic to get users
     res.json({ users: [] });
   });

   app.post('/api/users', (req, res) => {
     // Logic to create user
     res.status(201).json({ message: 'User created' });
   });

   app.listen(3000, () => console.log('Server running'));
   ```

2. **How to handle authentication in an API?**  
   Use middleware to verify JWT tokens:  
   ```javascript
   const jwt = require('jsonwebtoken');
   const authMiddleware = (req, res, next) => {
     const token = req.header('Authorization');
     if (!token) return res.status(401).send('Access denied');
     try {
       const verified = jwt.verify(token, 'secretKey');
       req.user = verified;
       next();
     } catch (err) {
       res.status(400).send('Invalid token');
     }
   };
   ```

3. **How to handle errors in Express?**  
   Use error-handling middleware:  
   ```javascript
   app.use((err, req, res, next) => {
     console.error(err.stack);
     res.status(500).send('Something broke!');
   });
   ```

4. **What is middleware in Express?**  
   Middleware functions have access to the request and response objects and can modify them or end the request-response cycle. They are used for logging, authentication, parsing, etc.

5. **How to connect to a database in a Node.js API?**  
   Using Mongoose for MongoDB:  
   ```javascript
   const mongoose = require('mongoose');
   mongoose.connect('mongodb://localhost/mydb', { useNewUrlParser: true });
   ```

This project demonstrates full-stack development skills, integration of AI services, and best practices in modern web application architecture.
