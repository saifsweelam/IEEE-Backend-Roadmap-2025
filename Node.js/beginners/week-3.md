# Node.js Beginners Week 3

## Main Topics

* Regular Expressions
    - [Net Ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g6m_6Sld9Q4jzqdqHd2HiD)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [134:146]
* Set, Map, WeakSet, WeakMap
    - [Traversy Media](https://www.youtube.com/watch?v=ycohYSx5h9w)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [123:133]
* Destructing
    - [freeCodeCamp](https://www.youtube.com/watch?v=-vR3a11Wzt0)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [115:122]
* Closure
    - [Web Dev Simplified](https://www.youtube.com/watch?v=3a0I8ICR1Vg)
    - [Unique Coderz Academy](https://www.youtube.com/watch?v=rXwxONbgBr0)

## Extra Resources

* Spread Operator
    - [Yallacode](https://www.youtube.com/watch?v=8h3B5ExWCR0)
* Debugging JavaScript in browser
    - [xplodivity](https://www.youtube.com/watch?v=ZaOZFkHTloM)


## Task (30 pts.)

### Theoritical **(2.5 pts. each)**

* Compare between the three types of quantifiers in regular expressions (`?`, `+`, `*`).
* What are the characters that can be represented by `\w` and `\b` in a regular expression?
* Compare between the `Map` and `WeakMap` according to the way they save keys and values.
* Write an example of a string which matches the following pattern:
    ```js
    const regex = /^(0[1-9]|[12]\d|3[01])[-\/](0[1-9]|1[0-2])[-\/]\d{4}$/;
    ```
    and write another string that violates the following pattern:
    ```js
    const regex = /^(?!.*\bieee\b).+$/i;
    ```

### Practical **(5 pts. each)**

* Use object and array destructing to get the values: `"Zamalek"` and `"4th"`. Your solution should be 2 lines of code maximum.
    ```js
    const user = {
        name: "Ashraf Ben Sharqy",
        age: 29,
        teams: ["Wydad", "Al Hilal", "Zamalek", "Al Gazira", "Al-Rayyan"],
        nationalTeam: {
            name: "Morroco",
            best: {
                africanCupOfNations: ["Champion", 2018],
                worldCup: ["4th", 2022],
            }
        }
    }
    ```

* Given the object `player`:
    ```js
    {
        name: "Samir Kamona",
        club: "Al Ahly",
        score: 25
    }
    ```
    Use the spread operator to create a new object `fantasyPlayer`, which has the `score` set to `50` and has a `position` attribute set to `"ST"`. Make sure the original object remains unchanged.

* Write a function that takes an array of items, filters all elements starting with `hand` and ending with `s` or `y` or `le` (case insensitive). There may be other characters in between.

    Tip: Use Regular Expressions

    #### Example:
    ##### Input:
    ```js
    ['handOn', 'hands', 'hanDLes', 'Handcuffs', 'handmade', 'in-hands', 'HANDINGLY']
    ```
    ##### Output:
    ```js
    ['hands', 'hanDLes', 'Handcuffs', 'HANDINGLY']
    ```

* Applying the concept of closures, create a counter using JavaScript and HTML. The counter should be able to increment, decrement, and reset its value, demonstrating the practical use of closures to maintain state between function calls.