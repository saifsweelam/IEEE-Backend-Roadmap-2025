# Entry Level Week 8

## Main Topics

* Database Indexes
    - [Metigator](https://www.youtube.com/watch?v=F3jRzYhjW7k)
    - [Tech Vault](https://www.youtube.com/playlist?list=PLE8kQVoC67PzGwMMsSk3C8MvfAqcYjusF) [Videos 5-8]

* Database Transactions (Theory)
    - [Tech Vault](https://www.youtube.com/playlist?list=PLE8kQVoC67PzGwMMsSk3C8MvfAqcYjusF) [Videos 17-18]
    - [Mohamed El Desouki](https://www.youtube.com/playlist?list=PL1DUmTEdeA6Lg6CXlnxEDhwpmWB0QaDh5) [Videos 2-16]

* Database Transactions (Practical)
    - [WiseOwlTutorials](https://www.youtube.com/watch?v=is03uRYFgqc) **SQL Server**
    - [Muhammed Esa](https://www.youtube.com/watch?v=p5L--OlZST0) **SQL Server**
    - [Software Nuggets](https://www.youtube.com/watch?v=DvJq4L41ru0) 
    **PostgreSQL**
    - [Bro Code](https://www.youtube.com/watch?v=GOQVlrQohtM) **MySQL**

* Database Concurrency & Locks
    - [Tech Vault](https://www.youtube.com/playlist?list=PLE8kQVoC67PzGwMMsSk3C8MvfAqcYjusF) [Videos 19-22]
    - [Mohamed El Desouki](https://www.youtube.com/playlist?list=PL1DUmTEdeA6Lg6CXlnxEDhwpmWB0QaDh5) [Videos 17-30]

## Extra Resources

* Database Indexes, Transactions and Locks
    - [CS50](https://www.youtube.com/playlist?list=PLhQjrBD2T382v1MBjNOhPu9SiJ1fsD4C0) (Lecture 5)


## Task (30 pts.)

### Database Indexing (14 pts.)

1. Compare between clustered and non-clustered indexes. _(2 pts.)_
2. Assume we have a table called sales with columns (`id`, `rental_date`, `inventory_id`, `customer_id`) and the table has a clustered innoDB index on `id` (primary key) and a B+ tree index on (`rental_date`, `inventory_id`).

    A clustered index in innoDB contains the entire row (all columns) in its leaf nodes while a B+ tree index in innoDB contains only the indexed columns (`rental_date`, `inventory_id`) and the primary key (`id`) in its leaf node. 
    
    How many index lookups (index access) will each of the following queries perform? **From Instabug Internship Assesment 2024** _(6 pts.)_

    1. ```sql
        SELECT * FROM sales WHERE id = 5;
        ```
    2. ```sql
        SELECT * FROM sales WHERE rental_date = "2021-01-01";
        ```
    3. ```sql
        SELECT inventory_id FROM sales WHERE rental_date = "2021-01-01";
        ```
    4. ```sql
        SELECT rental_date FROM sales WHERE inventory_id = 126;
        ```
    5. ```sql
        SELECT * FROM sales WHERE inventory_id = 126 and rental_date = "2021-01-01";
        ```
3. You are given a database table `Orders` with the following schema: _(6 pts.)_
    ```sql
    Orders(
        order_id INT PRIMARY KEY,
        customer_id INT,
        product_id INT,
        quantity INT,
        order_date DATE,
        shipping_address TEXT,
        total_price DECIMAL(10, 2)
    )
    ```

    The database is currently experiencing performance issues due to frequent and slow queries. Indexing is not yet implemented on any column. You're not allowed to rewrite the queries—your only task is to improve performance by choosing which indexes to create.

    You have access to the following workload statistics:

    - A dashboard page loads the last 20 orders by `order_date` DESC and displays them to users.

    - A reporting job runs daily to calculate total revenue per product in the last 30 days.

    - A support tool looks up orders by `order_id` to help resolve customer issues.

    - An analytics system filters orders by `customer_id` to analyze customer purchasing behavior.

    - Occasionally, admins check for suspiciously high `total_price` values (e.g., above $10,000) across all orders.

    You're allowed to create at most 3 indexes (including composite ones).

    Which columns would you index, and why? Justify your choices based on query patterns and index design principles.


### Database Transactions (10 pts.)

1. You're designing the backend for a banking system. A customer initiates a fund transfer of $500 from Account A to Account B. The transfer operation is implemented as a single transaction: _(4 pts.)_

    Transaction Steps:
    1. Check if Account A has at least $500.
    2. Deduct $500 from Account A.
    3. Add $500 to Account B.
    4. Record the transaction in the logs.

    Unfortunately, a power outage happens right after step 2, before any of the remaining steps complete.

    - Which ACID properties are violated in this scenario? Explain briefly.
    - How can each ACID property be ensured or restored in this context?
    - Suppose two users try to transfer funds from the same account at the same time. Which ACID property would prevent data corruption?
    - Imagine the system crashes but recovers using a transaction log. Which ACID property makes this possible, and how?

2. You are a database engineer at a bank. Two transactions are being executed concurrently on the same database: _(6 pts.)_

    **T1**
    ```sql
    READ(A)  
    A = A + 100  
    WRITE(A)  
    READ(B)  
    B = B - 50  
    WRITE(B)
    ```

    **T2**
    ```sql
    READ(B)  
    B = B + 200  
    WRITE(B)  
    READ(A)  
    A = A - 150  
    WRITE(A)
    ```

    **Schedule**
    ```sql
    1. READ(A) by T1  
    2. READ(B) by T2  
    3. A = A + 100 by T1  
    4. B = B + 200 by T2  
    5. WRITE(B) by T2  
    6. WRITE(A) by T1  
    7. READ(B) by T1  
    8. B = B - 50 by T1  
    9. WRITE(B) by T1  
    10. READ(A) by T2  
    11. A = A - 150 by T2  
    12. WRITE(A) by T2
    ```

    - Is the schedule conflict-serializable? Justify your answer.
    - If not serializable, suggest a reordering of operations that would make the schedule conflict-serializable while maintaining as much concurrency as possible.



### Database Concurrency & Locks (6 pts.)

1. You're building a small library system. Two users, Alice and Bob, are trying to borrow the same book at the same time. _(4 pts.)_

    The transaction for borrowing a book looks like this:

    1. Check if the book is available.
    2. Mark the book as "borrowed". 
    3. Save the changes to the database.

    Right now, your system doesn't use any locks.

    - What could go wrong if Alice and Bob run this transaction at the same time without any locks?
    - If your system uses a shared lock for reading and an exclusive lock for writing, which type should be used at each step?
    - Why is it important to hold the lock until the transaction is done?

2. Explain the idea behind timestamp ordering algorithm. _(2 pts.)_