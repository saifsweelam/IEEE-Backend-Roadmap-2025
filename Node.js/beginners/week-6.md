# Node.js Beginners Week 6

## Main Topics

* Introduction to Node.js & NPM
    - [CodeZone](https://www.youtube.com/watch?v=Bzzp0q0T5oM)
    - [Dave Gray](https://www.youtube.com/playlist?list=PL0Zuz27SZ-6PFkIxaJ6Xx_X46avTM1aYw) [1, 3]

* File System
    - [CodeZone](https://www.youtube.com/watch?v=EBSauYMP5j4) [First Hour]
    - [Dave Gray](https://www.youtube.com/watch?v=yQBw8skBdZU)

* Building CLI tools with Node.js
    - [CodeZone](https://www.youtube.com/watch?v=EBSauYMP5j4) [Last Hour]
    - [Dev tips by MoHo](https://www.youtube.com/watch?v=CfS6eOBe8AY)

* Building HTTP Servers with Node.js
    - [KMR Script](https://www.youtube.com/watch?v=qspfvLYTQ1Y)
    - [Dave Gray](https://www.youtube.com/watch?v=3ZAKY-CDKog)

* Node.js Event Loop and Call Stack
    - [CodeZone](https://www.youtube.com/watch?v=O7p1JfJT_es)
    - [JSConf](https://www.youtube.com/watch?v=8aGhZQkoFbQ)


## Extra Resources

* JavaScript Recap with Node.js
    - [Tech With Tim](https://www.youtube.com/watch?v=E3XxeE7NF30)


## Task (30 pts.)

1. **(2 pts.)** According to your understanding; explain what's the difference between `fs.readFile` and `fs.readFileSync` methods.

2. **(2 pts.)** Explain with examples the difference between installing a package as a normal dependency vs. as a development dependency with `npm`.

3. **(2 pts.)** What is the purpose of the `node_modules` folder, and why should it typically be excluded from version control systems like Git?

4. **(4 pts.)** Break through this `package.json` file and explain its contents.
    ```json
    {
        "name": "url-shortener-app",
        "version": "0.0.0",
        "private": true,
        "scripts": {
            "start": "node ./bin/www",
            "start:dev": "nodemon ./bin/www"
        },
        "dependencies": {
            "cookie-parser": "~1.4.4",
            "debug": "~2.6.9",
            "dotenv": "^16.4.4",
            "ejs": "^3.1.9",
            "express": "^4.18.2",
            "http-errors": "~1.6.3",
            "mongodb": "^6.3.0",
            "mongoose": "^8.1.3",
            "morgan": "~1.9.1",
            "shortid": "^2.2.16",
            "valid-url": "^1.0.9"
        },
        "devDependencies": {
            "nodemon": "^3.0.1"
        }
    }
    ```

5. **(6 pts.)** Create a Node.js CLI application that uses GitHub API to get the repositories of a single user.

    The application should take the username from the user input in the console, then call GitHub API to get the repositories of this user. Then store the repository names in a file `<username>.txt`.

    GitHub API Endpoint:
    ```
    https://api.github.com/users/<username>/repos
    ```

    Note: Don't forget to add `node_modules` directory to `.gitignore` file

6. **(5 pts.)** Implement a cloud calculator using the HTTP module.

    The request url form will be: `/[operation]?a=[num1]&b=[num2]`

    The calculator must support the following operations:

    * `add`: send $a + b$
    * `subtract`: send $a - b$
    * `multiply`: send $a * b$
    * `divide`: send $a / b$

    #### Example
    ```
    GET http://localhost:3000/add?a=3&b=6
    ```
    #### Response
    ```
    9
    ```

7. **(5 pts.)** Create a CLI file search application using Node.js. The application takes the file name and a query string as parameters, and prints the line which contains this string. If the string can't be found, the application should print `"THAT'S NOT FUNNY"`.

8. **(4 pts.)** Explain using code the difference between using CommonJS modules and the new EcmaScript modules, and show how to switch between them.