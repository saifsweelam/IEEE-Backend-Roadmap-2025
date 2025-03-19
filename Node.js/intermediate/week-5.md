# Node.js Intermediate Week 5

## Main Topics

* Password Protection (Concept)
    - [Studying With Alex](https://www.youtube.com/watch?v=qgpsIBLvrGY)

* `bcrypt` in Node.js
    - [Sam Meech-Ward](https://www.youtube.com/watch?v=AzA_LTDoFqY)
    - [Index Academy](https://www.youtube.com/watch?v=YYHtHbJnVEU)

* Session-based Authentication
    - [The Full Stack Junkie](https://www.youtube.com/watch?v=TDe7DRYK8vU)

* File Uploads
    - [PedroTech](https://www.youtube.com/watch?v=wIOpe8S2Mk8)
    - [Youssef Abbas](https://www.youtube.com/watch?v=j9ibqDLmKZs)

* Cloud Storage (e.g. Cloudinary)
    - [Youssef Abbas](https://www.youtube.com/watch?v=kvmQRkEj5h0)
    - [James Q Quick](https://www.youtube.com/watch?v=Rw_QeJLnCK4)
    - [OsmaniDev](https://m.youtube.com/watch?v=3Gj_mL9JJ6k)

## Task


### Multiple Choice Questions (5 marks)

1. What is the primary purpose of using `bcrypt` in password protection?
    - a) To encrypt database connections
    - b) To compress password strings
    - c) To securely hash and salt passwords
    - d) To validate email formats

2. In session-based authentication, what does the server typically store?
    - a) The user's entire profile
    - b) A unique session identifier
    - c) The user's password
    - d) All user login attempts

3. Which method is most secure for handling user passwords?
    - a) Storing passwords in plain text
    - b) Using MD5 hashing
    - c) Using symmetric encryption
    - d) Using bcrypt with salt

4. When uploading files to cloud storage like Cloudinary, what is typically transmitted?
    - a) The entire file path
    - b) A file reference or unique identifier
    - c) The complete file content
    - d) User authentication tokens only

5. What is a key advantage of session-based authentication?
    - a) Reduced server load
    - b) Stateless authentication
    - c) Ability to track user state
    - d) Immediate token expiration

### Written Questions (10 marks)

1. Explain the concept of password salting and why it's crucial in password protection. Describe how it enhances security against rainbow table attacks. (2 marks)

2. Compare and contrast session-based authentication with token-based authentication. Discuss the pros and cons of each approach in web application design. (2 marks)

3. Describe the process of file upload in a Node.js application. What are the key considerations for handling file uploads securely? (2 marks)

4. How does Cloudinary help in managing and optimizing image storage for web applications? Discuss its key features and benefits. (2 marks)

5. Explain the role of middleware in implementing session-based authentication in Express.js. Provide a brief code snippet demonstrating its implementation. (2 marks)

### Coding Task: Password Hashing Functions (5 marks)

Implement two functions in Node.js using `bcrypt`:

1. `hashPassword(password)`: A function that takes a plain text password and returns a securely hashed password.
2. `validatePassword(inputPassword, hashedPassword)`: A function that compares an input password with a stored hashed password.

Requirements:
- Use `bcrypt` for hashing
- Handle potential errors
- Implement appropriate salt rounds (minimum 10)
- Provide type checking and input validation

Example structure:
```javascript
const bcrypt = require('bcrypt');

async function hashPassword(password) {
    // Implement secure password hashing
}

async function validatePassword(inputPassword, hashedPassword) {
    // Implement password validation
}
```

### Mini Project: Gallery App with Session-based Authentication (10 marks)

Create a Gallery App with the following features:

#### Authentication Requirements:
- Implement user registration and login using session-based authentication
- Secure routes to prevent unauthorized access
- Create a middleware to check user sessions

#### Gallery Functionality:
- Allow authenticated users to upload images to Cloudinary
- Display uploaded images in a grid layout
- Implement delete functionality for user's own images

#### Technical Requirements:
- Implement `express-session` for session management
- Use Cloudinary for image storage
- Implement error handling
- Create a responsive frontend (can use EJS or similar templating)

#### Evaluation Criteria:
- Authentication security (4 marks)
- Image upload and management (3 marks)
- Code quality and error handling (2 marks)
- User experience and interface (1 mark)
