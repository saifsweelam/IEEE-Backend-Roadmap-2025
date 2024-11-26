# Node.js Beginners Week 5

## Main Topics

* Asynchronous Programming
    - [Net Ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9jx2TTZk3IGWKSbtugYdrlu)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [169:188]

* Creational Design Patterns (Factory, Singleton, Builder)
    - [Playlist](https://www.youtube.com/playlist?list=PLNE3WjwctlOz3Gx66tO5wxXu2C5E3Oj8i) [1:5]

## Extra Resources

* APIs
    - [Tarmeez](https://www.youtube.com/watch?v=L1V818vAE7w)
* JSON
    - [Web Dev Simplified](https://www.youtube.com/watch?v=iiADhChRriM)
    - [Tarmeez](https://www.youtube.com/watch?v=SE4ZnstntP0)


## Task (30 pts.)

* **(2 pts.)** Explain the difference between synchronous and asynchronous code.

* **(3 pts.)** Compare between `fetch` function and `XMLHttpRequest` class using [Numbers API](http://numbersapi.com) to call the API and print the response out to the console.

* **(3 pts.)** Waleed has the Imparnumerophobia, which means he fears the odd numbers. Waleed asked you to design a program for him that modifies the strings by replacing any odd number with the word `"BEEP"`. Help him implement this program using your knowledge in regular expressions.

    Example:
    ```js
    "I have 12 cars, 11 of which are 89 years old"
    ```
    Should be
    ```js
    "I have 12 cars, BEEP of which are BEEP years old"
    ```

* **(5 pts.)** Using [Star Wars API Documentation](https://swapi.dev/documentation), write a program that gets the planet name of the character with ID **4**

* **(5 pts.)** One day Seif visited the fake store to buy some fake products.

    Seif bought:
    * 3 items of product 1
    * 4 items of product 4
    * 5 items of product 3

    Seif is bad at math, can you help him calculate the total price of the products?

    Utilize the [Fake Store API Documentation](https://fakestoreapi.com/)

* **(4 pts.)** The following code suffers from callback hell. The callbacks are nested in a confusing way. Solve the callback hell problem using each of:
    * Promise Chaining

    * Async/Await Syntax

    ```js
    setTimeout(() => {
        console.log("Hey there!");

        setTimeout(() => {
            console.log("This code will help you understand");

            setTimeout(() => {
                console.log("Asynchronous Programming");

                setTimeout(() => {
                    console.log("What The Callback Hell!!!");

                    setTimeout(() => {
                        console.log("I AM STUCK");
                    }, 1000);
                }, 3000);
            }, 2000);
        }, 3000);
    }, 5000);
    ```

* **(5 pts.)** There's an application made for a study group where there's a `Student` class. Each student can have an instructor, but due to financial setbacks the study group can only hire 1 instructor who can work for multiple students. If all students don't need an instructor, then there's no need to hire one.
    
    You notice that this example fulfills the description of the singleton design pattern. Implement the classes `Student` and `Instructor` to apply the case as described.

* **(3 pts.)** Describe factory design pattern using an example of your own.