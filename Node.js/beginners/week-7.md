# Node.js Beginners Week 7

## Main Topics

* Express.js
    - [CodeZone](https://www.youtube.com/watch?v=XRoV7moNSsM)
    - [Net Ninja](https://m.youtube.com/playlist?list=PL4cUxeGkcC9jsz4LDYc6kv3ymONOKxwBU) [6:12]

* Template Engines
    - [KMR Script](https://www.youtube.com/watch?v=t1ovpjismUs)
    - [Net Ninja](https://www.youtube.com/watch?v=yXEesONd_54)

* MongoDB & Mongoose
    - [CodeZone](https://m.youtube.com/watch?v=vjde20smUpM)
    - [Net Ninja](https://m.youtube.com/playlist?list=PL4cUxeGkcC9h77dJ-QJlwGlZlTd4ecZOA)

## Extra Resources

- [Dave Gray (Express.js)](https://www.youtube.com/playlist?list=PL0Zuz27SZ-6PFkIxaJ6Xx_X46avTM1aYw) [6:9]

- [Dave Gray (MongoDB & Mongoose)](https://www.youtube.com/playlist?list=PL0Zuz27SZ-6PFkIxaJ6Xx_X46avTM1aYw) [13:15]


## Task (30 pts.)

- ### Recap Section (10 pts.):
1. **(3 pts.)** Explain the four types of function binding in JavaScript: implicit binding, explicit binding, new binding, and default binding. How do they differ from each other?

2. **(2 pts.)** What will be the output of this code and why?

```JS
let student = { 
   name: "Saleh",
   subjects = ["Math","Science","English"]
}
console.log(typeof typeof student)
```
<br>

3. **(3 pts.)** what the modules and what the differences between ***CommonJS*** modules and ***EJS*** modules?


4. **(2 pts.)** What is the purpose of ***"scripts"*** attribute in package.json?
---

- ### Express Section (10 pts. 2 pts for each question):
1. Define the ***"Middleware"*** term and it's usage in Express.js

2. What are the common reasons that can cause an Express application to hang or become unresponsive? Please provide specific scenarios or examples.

3. what is the method used to parse the response body comes that from **HTML** form?

4. If we access **"/profile/1307?tab=friends&history=off"**
What will be outputted to the backend console?

```JS
app.get('/profile/:userId',(req,res)=>{
    console.log(res.params)
    console.log(req.query)
})
```

5. In a scenario, the user tries to enter the login page while he is already logged in.
You, as the developer, know that he did that by mistake. So you need to send him to the homepage instead. How can you implement that in Express.js?

```JS
a. req.navigate('/')
b. res.navigate('/')
c. res.redirect('/')
d. res.send('/')
```
---

- ### MongoDB Section (10 pts. 2 for each question):

1. What is the default data type of a MongoDB document id?

2. What is the Mongoose model, How to create one and, What are its uses?

3. What will be the output of this code?
```JS
- const x = User.findOne({username:"elgokar"})
- const y = User.find({})
- const z = await User.findById(66eb21a982f34874a0323f7a)

console.log(typeof x)
console.log(typeof y)
console.log(typeof z)
``` 
<br>

4. In the following code 3b3aziz trying to update a user age in the database but it doosn't work as expected, what the problem in his code and how to solve it?

```JS
const updateAge = () => {
    const user = User.findOne({username:"sherbiny"},callback)
    console.log(user.age) //output ===> 20
    user.age=25;
    user.save();
    console.log(user.age) //output ===> 20
}
```

5. How would you add ***validation*** to a Mongoose schema to ensure a string property is **at least 3 characters** long?

---

- ### Practical Task Section (10 pts.):
Create a simple ToDo App which consists of two pages:

1. A page which contains a form to add a new task
2. A page which displays all the tasks, and a link to the other page

### Task criteria:
- Use MongoDB to store the notes.
- Use HTML templates (EJS, Pug, or any of your choice) to render the views for notes.
- **(Bonus):** Add a Delete button for each task to delete it from the database 