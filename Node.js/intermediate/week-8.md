# Node.js Intermediate Week 8

## Main Topics

* Exposing API Query Features
    - [procademy](https://www.youtube.com/playlist?list=PL1BztTYDF-QPdTvgsjf8HOwO4ZVl_LhxS) [Videos 74:87]
    - [Index Academy](https://www.youtube.com/playlist?list=PLDQ11FgmbqQNFuGQTKbAIGEyOKWUGBs6i) [Videos 70:84]

* API Security
    - [freeCodeCamp](https://www.youtube.com/watch?v=YYe0FdfdgDU)
    - [Ahmed Elemam](https://www.youtube.com/watch?v=a0g8rI4j4qc)

* Security Middlewares (1) - Helmet
    - [michael_jpm](https://www.youtube.com/watch?v=3Y1u0E1Bpss)
    - [procademy](https://www.youtube.com/watch?v=Abqcisad-QM)

* Security Middlewares (2) - CORS
    - [Web Dev Simplified](https://www.youtube.com/watch?v=PNtFSVU-YTI)
    - [KMR Script](https://www.youtube.com/watch?v=JvYxywpnaK8)

* Security Middlewares (3) - Rate Limiting
    - [Raddy](https://www.youtube.com/watch?v=VZZLiVccwKk)
    - [procademy](https://www.youtube.com/watch?v=Lt8W5VPkDxs)
    - [Web Dev Cody](https://www.youtube.com/watch?v=D770heiyxdc) (Customized Approach)


## Task (40 pts.)

1. Add API Query Features to the API you implemented in the last 2 weeks. _(5 pts.)_

2. Choose one of the OWASP Top 10 vulnerabilities and write an article about it on medium or a similar blogging website. Include a clear definition of the vulnerability, how it works, and how to prevent it. Use examples from express.js applications. _(7 pts.)_

3. Explain the difference between each of these types of pagination with examples: _(5 pts.)_
    - Offset-based pagination
    - Cursor-based pagination
    - Keyset-based pagination
    - Page-based pagination
    - Time-based pagination

4. You want to prevent duplicate users registering with the same email using case differences (e.g., `John@Email.com` vs `john@email.com`). Use mongoose middlewares/hooks to implement this. _(5 pts.)_
    - Write a middleware function that normalizes the email to lowercase before saving it to the database.
    - Check if the email already exists in the database, ignoring case differences.

5. Mention the name of the security vunerability in each of the following scenarios: _(8 pts.)_
    - A user is able to enter a script tag in the username field of a form, and when the form is submitted, the script executes in the browser of other users who view the page.
    - A web application allows users to upload files, but it does not validate the file type or size. An attacker uploads a malicious executable file, which is then executed on the server.
    - A user is able to access a resource owned by another user by manipulating the URL or request parameters, even though they are not authorized to do so.
    - A web application does not properly validate user input, allowing an attacker to inject SQL queries into the database, potentially exposing sensitive data or allowing unauthorized access.
    - A token can be reused by an attacker to gain unauthorized access to a user's account, even after the user has logged out or the token has expired.
    - A web application sends a JSON Web Token (JWT) that contains sensitive information, such as user passwords or API keys, in the payload.
    - A user is able to send additional parameters in a request that are not expected by the server, potentially causing unexpected behavior or security vulnerabilities. (like sending a `role` parameter to a user creation endpoint to assign admin privileges)
    - A web application does not properly validate the origin of requests, allowing an attacker to send requests from a different domain and potentially perform unauthorized actions on behalf of the user.

6. Answer the following example using code snippets. You're building a Node.js API for a library application. The API allows users to manage books (title, author, genre) and their borrowings. Mongoose is used for interacting with the database. _(5 pts.)_
    - The API endpoint for retrieving a specific book requires its ID. How can you define the route for this endpoint?
    - The API should allow filtering books by genre. How can you achieve this using Mongoose queries?
    - A user wants to retrieve books published after a specific date. Which Mongoose query operator can be used for this filtering?
    - The API should allow searching books by a keyword in the title or author fields. How can you achieve this using Mongoose queries?

7. Write a manual implementation of the rate limiting middleware. The middleware should limit the number of requests from a single IP address to 100 requests per hour. If the limit is exceeded, return a 429 status code with a message indicating that the rate limit has been exceeded. _(5 pts.)_