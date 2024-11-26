# Node.js Beginners Week 4

## Main Topics

* Object Oriented Programming
    - [Net Ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9i5yvDkJgt60vNVWffpblB7)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAzLyvrWPwMw6bbBlTwPxgLF)
* `this` keyword
    - [Programming with Mosh](https://www.youtube.com/watch?v=gvicrj31JOM)
    - [Codehood](https://www.youtube.com/watch?v=_AIK52R6e8M)
* Date and Time
    - [dcode](https://www.youtube.com/watch?v=-eRsWqwcPuk)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [159:163]
* Generator Functions
    - [JSConf](https://www.youtube.com/watch?v=gu3FfmgkwUc)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAy3siU1b04xY24ZlstofO9M) [32:35]
* ES6 Modules
    - [Web Dev Simplified](https://www.youtube.com/watch?v=cRHQNNcYf6s)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAy3siU1b04xY24ZlstofO9M) [38:40]

## Extra Resources

* OOP
    - [procademy](https://www.youtube.com/playlist?list=PL1BztTYDF-QOvKYBBYdjzHISCeaYCAEfH)
* Generator Functions
    - [Yallacode](https://www.youtube.com/watch?v=tx8Jf7OpTB0)
    - [dcode](https://www.youtube.com/watch?v=EzdgkEMvrvA)
* ES6 Modules
    - [Yallacode](https://www.youtube.com/watch?v=LSOkjx7wA_E)


## Task (30 pts.)

* **(5 pts.)** Write examples illustrating the use of each of the following:
    - Static properties
    - Private properties
    - Setters and getters
    - Method chaining

* **(5 pts.)** Explain the difference between `this` keyword's value in the following examples:

    - ```js
        const player = {
            firstName: "Ahmed",
            lastName: "Hafez",
            introduce: () => {
                console.log(`Hey, I'm ${this.firstName} ${this.lastName}`);
            }
        }

        player.introduce();
        ```
    - ```js
        const player = {
            firstName: "Ahmed",
            lastName: "Hafez",
            introduce() {
                console.log(`Hey, I'm ${this.firstName} ${this.lastName}`);
            }
        }

        player.introduce();
        ```
    - ```js
        function introduce() {
            console.log(`Hey, I'm ${this.firstName} ${this.lastName}`);
        }
        const player = {
            firstName: "Ahmed",
            lastName: "Hafez",
            introduce
        }

        player.introduce();
        ```
    - ```js
        function introduce() {
            console.log(`Hey, I'm ${this.firstName} ${this.lastName}`);
        }
        const player = {
            firstName: "Ahmed",
            lastName: "Hafez"
        }

        introduce();
        introduce.call(player);
        ```

* **(5 pts.)** Create a `Vehicle` class which has 3 properties: color, number of wheels and horn. The color defaults to `"blue"`, the default value of number of wheels is `4` and the horn defaults to `"beep beep"`.

    Add a method `honkHorn()` which prints the value of the horn of the vehicle.

    Then create a `Bicycle` subclass that extends the Vehicle class. The `Bicycle` subclass should override Vehicle's constructor function by changing the default values for wheels from `4` to `2` and horn from `'beep beep'` to `'honk honk'`.

    Make each class in a separate module and use them together in a different module (main.js)

    Put your code in a GitHub repository and paste the link below.

* **(5 pts.)** Add the function `addHours()` to the prototype of the `Date` constructor. This function takes a number `H` as an argument and adds `H` hours to the date. Make sure that the function will be added to _ALL_ Date instances not only a single object.

    ```js
    let date = new Date(2022, 10, 3, 12, 38); // 2022-11-03T12:38:00.000Z
    date.addHours(4);
    console.log(date); // 2022-11-03T16:38:00.000Z
    ```

* **(5 pts.)** Implement a generator function that yields the numbers of Fibonacci's sequence starting from the beginning of the sequence.

    The well-known Fibonacci sequence $F(0), F(1), F(2), …$ is defined as follows:

    $F(0) = 0$

    $F(1) = 1$

    For each $i ≥ 2$: $F(i) = F(i−1) + F(i−2)$

* **(5 pts.)** Answer the MCQ questions in the submission form