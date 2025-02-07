# Node.js Intermediate Week 1

## Main Topics

* Typescript Syntax
    - [Net Ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gUgr39Q_yD6v-bSyMwKPUI)
    - [Youssef Abbas](https://www.youtube.com/playlist?list=PL5gCk5NdNx5_QxWasJ3msGjlpB7hs1-nF)
* Setting up a TS project
    - [Colt Steele](https://www.youtube.com/watch?v=qy8PxD3alWw)
* Express & TypeScript
    - [Anson the Developer](https://www.youtube.com/watch?v=Be7X6QJusJA)
* `tsx` vs. `ts-node`
    - [TypeScript TV with Benny](https://www.youtube.com/watch?v=-7dNs1ggKRs)
* MVC file structure
    - [PedroTech](https://www.youtube.com/watch?v=Cgvopu9zg8Y)
    - [Courses 4 Arab](https://www.youtube.com/watch?v=uoHjKX5cmzY)

## Extra Resources

* TypeScript Syntax
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAy532K9M_fjiAmrJ0gkCyLJ)
    - [freeCodeCamp](https://www.youtube.com/watch?v=30LWjhZzg50)

## Task (30 pts.)

## Scoring
- Total Points: 30
- Part I (Express Concepts): 10 points
- Part II (TypeScript Knowledge): 10 points
- Part III (Practical Implementation): 10 points

## Part I: Express Fundamentals (10 points)

### Middleware and Routing Analysis
1. **Route Response Prediction** *(2 points)*
   - Predict the response body when accessing `http://localhost:3000/hello`
   
   Given Express Application:
   ```javascript
   const express = require('express');

   const app = express();

   app.use((req,res,next)=>{
       res.write("Hi")
       next();
   })

   app.use('/',(req,res,next)=>{
       res.write("Welcome");
       res.end();
   })

   app.use('/hello',(req,res,next)=>{
       res.write("Hello");
       res.end();
   })

   app.listen(3000,()=>console.log('Listening on port 3000'));
   module.export = app;
   ```

2. **Form Body Parsing** *(2 points)*
   - Identify the correct middleware for parsing HTML form bodies into `req.body`
   - Multiple-choice question:
     - [ ] `bodyParser.urlencoded()`
     - [ ] `bodyParser.json()`
     - [ ] `bodyParser.form()`
     - [ ] `bodyParser.multipart()`

3. **Body Parsing Process** *(2 points)*
   - Explain the process of converting HTML body to a JSON object
   - Describe the initial body submission type

4. **Multipart Parsing** *(2 points)*
   - Explore the `bodyParser.multipart()` method
   - Understand its functionality and use cases

5. **Node.js Threading Model** *(2 points)*
   - Select the most accurate description of Node.js threading and event loop:
     - [ ] Node.js uses multiple threads to handle incoming requests and execute JavaScript code simultaneously.
     - [ ] Node.js follows a single-threaded model that utilizes an event loop for handling I/O operations asynchronously.
     - [ ] Node.js implements a multi-threaded architecture where each request is processed by a dedicated thread.
     - [ ] Node.js event loop handles only synchronous operations, while asynchronous operations are executed in separate threads.

## Part II: TypeScript Knowledge (10 points)

### Type System and Advanced Typing

1. **Union Types** *(1 point)*
   - Define Union types in TypeScript
   - Provide a practical usage example

2. **Type Compatibility** *(1 point)*
   - Analyze type-related code:
   ```typescript
   let x: (string | number)[];
   x.push(123);
   ```
   - Determine if this code will result in an error or not and explain why?

3. **Generic Types** *(1 point)*
   - Define Generic types
   - Provide a practical usage example

4. **Interface Type Flexibility** *(1 point)*
   - Improve this interface by removing the `any` type:
   
   Original Interface:
   ```typescript
   interface User {
       id: any;
       name: string;
       email: string;
   }
   ```

   Possible Improvements:
   ```typescript
   // Option 1
   interface User {
       id: string | number;
       name: string;
       email: string;
   }

   // Option 2
   interface User<UserIdType> {
       id: UserIdType;
       name: string;
       email: string;
   }

   // Option 3
   interface <UserIdType>User {
       id: UserIdType;
       name: string;
       email: string;
   }

   // Option 4
   // There is no possible way
   ```

5. **TypeScript Execution Comparison** *(1 point)*
   - Explain the difference between `ts-node` and `tsx`
   - Determine which is better and why

6. **TypeScript Compilation Commands** *(1 point)*
   - Explain the difference between `tsx file.ts` and `tsc file.ts`
   - Identify when to use each command

7. **Type Declaration Handling** *(2 point)*

Scenario:
You're starting a new TypeScript project and want to use Express. Follow these steps:
1. Create a new project directory
2. Initialize a new Node.js project with `npm init -y`
3. Install Express and TypeScript:
   ```bash
   npm install express
   npm install --save-dev typescript
   ```
4. Create a simple Express application in TypeScript

**Problem**: When you import and use Express, you encounter the following TypeScript error:
```
error TS7016: Could not find a declaration file for module 'express'.
```
 
- Explain the cause of this error
- Describe the steps to resolve this TypeScript type declaration issue
- Discuss why additional type declaration packages are necessary when working with TypeScript and third-party libraries

8. **Object-Oriented TypeScript Challenge** *(2 points)*
   - Create a `Student` class implementing a `WakesUpEarly` interface
   - Requirements:
     - Interface with `wakeUpEarly()` method returning a string
     - Student class with first name, last name, and grade
     - Implement `wakeUpEarly()` method with a personal wake-up description
   - Submit solution on CodePen

## Part III: Practical TypeScript Project (10 points)

### Sticky Notes Reimplementation

#### Requirements
- Reimplement the TODO App task from [Level 1 Week 7](https://github.com/saifsweelam/IEEE-Backend-Roadmap-2025/blob/main/Node.js/beginners/week-7.md)
- Use TypeScript exclusively
- Implement MVC (Model-View-Controller) file structure
- DON'T USE ```any``` TYPE

#### Configuration Checklist
- Properly configured TypeScript config files
- `package.json` with working `build` and `start` scripts
- Add build directory to `.gitignore`

---


## Bonus Questions

1. **TypeScript Validation:**
Why do we need additional validators when using TypeScript, even though it has its own type system?

2. **Type Annotations:**
Search for JavaScript Type Comments (JSDoc), then explain the difference between using Type Comments in JavaScript and using TypeScript.