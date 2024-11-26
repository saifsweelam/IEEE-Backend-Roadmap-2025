# Node.js Beginners Week 1

## Main Topics

* JavaScript Basics
    - [Net Ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9haFPT7J25Q9GRB_ZkFrQAc) [1:3]
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [1:56]

## Extra Resources

* `var` vs. `let` vs. `const`
    - [Web Dev Simplified](https://www.youtube.com/watch?v=9WIJQDvt4Us)
* JavaScript Arrays
    - [Dave Gray](https://www.youtube.com/watch?v=0SyTDl4pb4w)


## Task


### Theoritical
* Explain the difference between `==` and `===` in JavaScript.
* Hamed is simply trying to sort an array of numbers but unfortunately this sort method isn't working as expected. Can you tell Hamed the reason for this behavior and how to implement it in a right way?
    ```js
    const arr = [10, 5, 11];
    arr.sort();
    ```
* Answer few MCQ questions in the submission form.

### Practical
* Write a JavaScript program that converts temperature from Celsius to Fahrenheit.

* Write a JavaScript program that takes an array and updates it in place. Each Element in the array is a string or a number. If it's a number, you should multiply it by 3. If it's a string, you should make the first letter uppercase and the rest lowercase.
    
    **Example:**

    Input:
    ```js
    let arr = [19, "dreams", "PlayGround", 2, "xD", "i"];
    ```
    Output:
    ```js
    [57, "Dreams", "Playground", 6, "Xd", "I"]
    ```

* Adel wrote a secret message that he didn't want anyone to read easily. To make it difficult to understand, he reversed it. He then thought that it wasn't enough, so he wanted to perform another minor change that would make it unrecognizable. Write a JavaScript program that takes a string $s$ and prints it again after reversing it and making all vowel letters uppercase.
    
    **Example:**

    Input:
    ```js
    let s = "Hey There, I'm glad to have you";
    ```
    Output:
    ```
    UOy EvAh Ot dAlg m'I ,ErEhT yEH
    ```

* Write a JavaScript program that takes a string and an array of forbidden letters. Your program should print the string after removing the forbidden letters from it and make all letters separated by hiphens `-`.

    **Example:**

    Input:
    ```js
    let text = "Please";
    let forbiddenLetters = ['r', 'x', 'p', 'a'];
    ```
    Output:
    ```
    l-e-s-e
    ```