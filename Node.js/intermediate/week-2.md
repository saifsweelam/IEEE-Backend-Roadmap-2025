# Node.js Intermediate Week 1

## Main Topics

* Server-Side Validation & `express-validator`
    - [Raddy](https://www.youtube.com/watch?v=z8m_Vy_9FIs)
    - [Jan Goebel](https://www.youtube.com/watch?v=7i7xmwowwCY)
    - [Express-validator docs](https://github.com/validatorjs/validator.js)
* Runtime Type Checking / Schema Validation (using Zod)
    - [Web Dev Simplified](https://www.youtube.com/watch?v=L6BE-U3oy80&t=33s&pp=ygUOem9kIHR5cGVzY3JpcHQ%3D)
* Sessions
    - [Anson the Developer](https://www.youtube.com/watch?v=Be7X6QJusJA)
* Flash Messages
    - [TypeScript TV with Benny](https://www.youtube.com/watch?v=-7dNs1ggKRs)
* MVC file structure
    - [PedroTech](https://www.youtube.com/watch?v=Cgvopu9zg8Y)
    - [Courses 4 Arab](https://www.youtube.com/watch?v=uoHjKX5cmzY)

* Environment variables
    - [Environment Variables Part 1](https://www.youtube.com/watch?v=KdFhoEvSAcM)
    - [Environment Variables Part 2](https://www.youtube.com/watch?v=PxshhOKNPpQ)

## 🎯 Task (30 Points)

### 🔹 Scoring Breakdown
- **Total Points: 30**
  - **Part I (Theoretical):** 15 points
  - **Part II (TypeScript Task):** 5 points
  - **Part III (Practical Implementation):** 10 points  

---

### 📝 Part I: Theoretical Questions (15 Points)

1. **What is the Model-View-Controller (MVC) architectural pattern, and what are its benefits?** *(1 point)*  

2. **Define a session and explain its usages.** *(2 points)*  

3. **What is the difference between sessions and cookies, and why should sessions be stored in a database?** *(2 points)*  

4. **Why is server-side validation important even when client-side validation is implemented?** *(2 points)*  

5. **In Express.js, where is server-side validation typically performed in the application flow?** *(1 point)*  

6. **Explain the validation process flow using Zod and how it works.** *(2 points)*  

7. **What is the method used in `express-validator` to define a custom error message?** *(1 point)*  

8. **Which HTTP status code is most appropriate for validation errors?** *(1 point)*  
   - [ ] 400  
   - [ ] 401  
   - [ ] 403  
   - [ ] 405  

9. **What are environment variables, and why are they important?** *(1 point)*  

10. **When storing the `PORT` number in a `.env` file, why should it be explicitly cast to a number?** *(1 point)*  

11. **How can you provide default values for environment variables when using `dotenv`?** *(1 point)*  

---

### ✔️ Part II: TypeScript Task (5 points)

### Challenge Description
Write a TypeScript function that converts an array of binary digits (0s and 1s) into its decimal equivalent.

### Requirements
- Implement using TypeScript
- Create type declarations to ensure array contains only 0s and 1s
- Array input represents binary number (e.g., [0,0,0,1] represents binary 0001)
- Return decimal integer as output

### Example Conversions
```typescript
[0, 0, 0, 1] → 1    // 0001 in binary
[1, 0]       → 2    // 0010 in binary
[1, 0, 1]    → 5    // 0101 in binary
[1, 0, 0, 0] → 8    // 1000 in binary
[0, 0, 0, 2] → Error
```

### Technical Specifications

#### Input Constraints
- Array must only contain 0s and 1s
- Type safety must be enforced via TypeScript
- Array length can be variable
- Array must not be empty

#### Expected Output
- Single integer representing decimal value
- Must handle valid binary numbers of any length

---

### 🏗️ Part III: Practical Implementation (10 Points)

### 🔹 Task: Implement a Simple Signup Form

#### 🛠️ Validation Rules:
* **Full Name:** Must not contain numbers.
* **Email:** Must be a valid email address.
* **Password:**
   * Must be **between 8 and 64 characters**.
   * Must contain **at least one number, one uppercase letter, and one lowercase letter**.
* **Password Confirmation:** Must **match** the password.

#### 📌 Implementation Requirements:
* Perform **server-side validation** using `express-validator` (or `zod`).
* If **validation fails**, redirect to the form again and flash the errors into the page.
* If **validation passes**, respond with **"SUCCESSFUL"**.

#### ♻️ Environment Variables:
* Store the port number in a `.env` file.
* Use **5000** as the **default value** if no port is assigned.
* Ensure the `.env` file is **ignored** by Git.

🎁 **Bonus: Implement it using Typescript & Zod with type infering**