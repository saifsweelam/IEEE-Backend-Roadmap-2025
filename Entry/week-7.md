# Entry Level Week 7

## Main Topics

* Database Normalization
    - [Tech Vault](https://www.youtube.com/playlist?list=PLE8kQVoC67Py5LnCUHp_wp2uzbaBZWSmx) [Video 5]
    - [Metigator](https://www.youtube.com/watch?v=0Jps8KJSjy4)
    - [CMU Database Group](https://www.youtube.com/watch?v=ltMB_dyhxqk)
* SQL Views
    - [CS50](https://www.youtube.com/playlist?list=PLhQjrBD2T382v1MBjNOhPu9SiJ1fsD4C0) (Lecture 4)
    - [Tech Vault](https://www.youtube.com/playlist?list=PLE8kQVoC67Py5LnCUHp_wp2uzbaBZWSmx) [Videos 9, 10]

## Extra Resources

* Database Design + Projects
    - [Database Star](https://www.youtube.com/playlist?list=PLZDOU071E4v6epq3GS0IqZicZc3xwwBN_)

## Task (30 pts.)

> **Note:** Using proper search methods is allowed as long as you don't copy the answers from ChatGPT or similar tools.

1. This database table is used to store information about customer orders. The table is not normalized. Identify the functional dependencies in the table and normalize it to 1NF, 2NF then 3NF. Provide the new tables for each normalization form. _(5 pts.)_
    
    | OrderID | CustomerName | CustomerPhone | ItemsPurchased                         | TotalAmount |
    |---------|-------------|---------------|----------------------------------------|-------------|
    | 1       | John Doe    | 555-1234      | "Laptop - $1000, Mouse - $20"         | $1020       |
    | 2       | Jane Smith  | 555-5678      | "Keyboard - $50, Monitor - $300"      | $350        |
    | 3       | John Doe    | 555-1234      | "Headphones - $80"                    | $80         |

2. Take a look at the database design examples in the extra resources. Similarly, design a database system for a YouTube clone.

    Your database design should take in consideration fundamental features like users, videos, comments, likes, subscriptions and playlists. _Other additional features are considered out of scope (optional)._

    Write the functional requirements of the database system, then work on the database tables schema. _(10 pts.)_

3. Solve the following SQL problems: _(4 pts.)_
    - [Type of Triangle](https://www.hackerrank.com/challenges/what-type-of-triangle/problem?isFullScreen=true)
    - [Find Products with Valid Serial Numbers](https://leetcode.com/problems/find-products-with-valid-serial-numbers/description/)
    - [Find Students Who Improved](https://leetcode.com/problems/find-students-who-improved/description/)
    - [Percentage of Users Attended a Contest](https://leetcode.com/problems/percentage-of-users-attended-a-contest/description/)

4. What are the main differences in uses between subqueries, CTEs and views in SQL? _(3 pts.)_

5. A movie rental company wants to create a view to help customer service representatives quickly find active rentals. The database has the following tables: _(5 pts.)_
    ```sql
    CREATE TABLE customers (
        customer_id SERIAL PRIMARY KEY,
        name        VARCHAR(100) NOT NULL,
        email       VARCHAR(100) UNIQUE NOT NULL
    );

    CREATE TABLE movies (
        movie_id   SERIAL PRIMARY KEY,
        title      VARCHAR(255) NOT NULL,
        genre      VARCHAR(50) NOT NULL
    );

    CREATE TABLE rentals (
        rental_id   SERIAL PRIMARY KEY,
        customer_id INT REFERENCES customers(customer_id) ON DELETE CASCADE,
        movie_id    INT REFERENCES movies(movie_id) ON DELETE CASCADE,
        rental_date TIMESTAMP DEFAULT NOW(),
        return_date TIMESTAMP -- NULL if not yet returned
    );
    ```

    > The code snippet uses PostgreSQL syntax. If you are using another DBMS, you may need to adjust the syntax accordingly.

    1. Write a SQL statement to create a view called `active_rentals`, which shows only currently rented movies (i.e., those with `return_date` as `NULL`). The view should include:

        - `rental_id`
        - `customer_name`
        - `customer_email`
        - `movie_title`
        - `rental_date`

    2. Explain two benefits of using an SQL view in this scenario.

6. Research what a materialized view is in SQL. Explain the concept and provide an example of when you might use a materialized view. _(3 pts.)_