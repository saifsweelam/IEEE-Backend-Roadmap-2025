# Entry Level Week 6

## Main Topics

* SQL Joins
    - [Tech Vault](https://www.youtube.com/playlist?list=PLE8kQVoC67Py5LnCUHp_wp2uzbaBZWSmx) [Video 6]
    - [techTFQ](https://www.youtube.com/watch?v=0OQJDd3QqQM)
* SQL Aggregations & Grouping
    - [Michael Fudge](https://www.youtube.com/watch?v=mX61Ww3wRgU)
    - [Mohamed El Desouki](https://www.youtube.com/watch?v=8aNhhMi2ce4)
* SQL Subqueries
    - [techTFQ](https://www.youtube.com/watch?v=nJIEIzF7tDw)
    - [Tech Vault](https://www.youtube.com/playlist?list=PLE8kQVoC67Py5LnCUHp_wp2uzbaBZWSmx) [Video 8]
    - [Mohamed El Desouki](https://www.youtube.com/watch?v=58Lsm9ly7cU)

## Extra Resources

* SQL Joins, Subqueries and Grouping
    - [CS50](https://www.youtube.com/playlist?list=PLhQjrBD2T382v1MBjNOhPu9SiJ1fsD4C0) (Lecture 1)
    - [freeCodeCamp](https://www.youtube.com/watch?v=HXV3zeQKqGY) (Last 2 hours)
* Revision on Queries
    - [Metigator](https://www.youtube.com/watch?v=oSLeuvYxK_Y)

## Task (30 pts.)

> **Note:** Using proper search methods is allowed as long as you don't copy the answers from ChatGPT or similar tools.

1. Solve the following SQL problems: _(10 pts.)_
    - [Game Play Analysis I](https://leetcode.com/problems/game-play-analysis-i/description/)
    - [Department Highest Salary](https://leetcode.com/problems/department-highest-salary/)
    - [Customers Who Never Order](https://leetcode.com/problems/customers-who-never-order/)
    - [Rising Temperature](https://leetcode.com/problems/rising-temperature/description/)
    - [Confirmation Rate](https://leetcode.com/problems/confirmation-rate/description/)
    - [The Report](https://www.hackerrank.com/challenges/the-report/problem)

2. **Dataset Exploration:** You are given a dataset that contains information about cars and their selling prices in a known period of time. The dataset is in `csv` format, you can download it directly from [Kaggle](https://www.kaggle.com/datasets/sidharth178/car-prices-dataset?select=train.csv). Make sure to download the file `train.csv`, then import the data inside the file to a database of your creation. After importing the data, make the following queries on it and provide the results: _(15 pts.)_
    - Find the average price of cars in the dataset.
    - Calculate the number of cars with leather interior that are cheaper than $1400.
    - Get the maximum price of Toyota cars produced in 2011.
    - Sort the car manufacturers according to the average price of their cars descendingly.
    - Calculate the percentage of cars that use petrol fuel only among cars with category `Jeep`.
    - Find the cheapest car(s) in the dataset. (If multiple cars have the same lowest price, return all of them.)
    - Find the percentage of Toyota cars that are above the average price of all cars.

    **Note: You'll need to research the way to import a `csv` file into your database. It will slightly differ between different DBMS.**

3. Compare between different types of SQL Joins (Inner, Left, Right, Full, Cross) and provide a brief explanation of when to use each type. _(5 pts.)_