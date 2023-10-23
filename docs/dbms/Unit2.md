# SQL Concepts

- [SQL Concepts](#sql-concepts)
    - [SQL Concepts](#sql-concepts-1)
    - [Basics of SQL](#basics-of-sql)
    - [DDL, DML, DCL](#ddl-dml-dcl)
    - [Structure Creation](#structure-creation)
    - [Alteration](#alteration)
    - [Defining Constraints](#defining-constraints)
    - [Functions](#functions)
    - [Aggregate Functions](#aggregate-functions)
    - [Built-In Functions: Numeric, Date, and String Functions](#built-in-functions-numeric-date-and-string-functions)
    - [Set Operations](#set-operations)
    - [Sub-queries](#sub-queries)
    - [Correlated Sub-queries](#correlated-sub-queries)
    - [Use of GROUP BY, HAVING, and ORDER BY](#use-of-group-by-having-and-order-by)
    - [Join and Its Types](#join-and-its-types)
    - [Exist, Any, All](#exist-any-all)
    - [Views and Their Types](#views-and-their-types)

* * *

### SQL Concepts

**SQL (Structured Query Language)** is a powerful and standardized language used for managing and manipulating relational databases. It enables users to interact with databases to perform various operations, such as retrieving data, inserting records, updating information, and defining database structures. SQL concepts are fundamental to working with relational databases. Here are some key SQL concepts:

**1\. Data Retrieval:**

* SQL allows users to retrieve data from a database using queries. The `SELECT` statement is used for this purpose.
* Example:

sql

`SELECT first_name, last_name FROM employees WHERE department = 'HR';`

**2\. Data Modification:**

* SQL provides statements like `INSERT`, `UPDATE`, and `DELETE` to add, modify, or delete data in a database.
* Example:

sql

`INSERT INTO products (product_name, price) VALUES ('Laptop', 1000);`

**3\. Data Definition:**

* SQL supports Data Definition Language (DDL) statements like `CREATE`, `ALTER`, and `DROP` for defining and managing database structures, such as tables, indexes, and constraints.
* Example:

sql

`CREATE TABLE customers (     customer_id INT PRIMARY KEY,     first_name VARCHAR(50),     last_name VARCHAR(50),     email VARCHAR(100) );`

**4\. Transaction Control:**

* SQL includes statements like `COMMIT`, `ROLLBACK`, and `SAVEPOINT` to manage transactions and ensure data consistency.
* Example:

sql

`BEGIN; -- Start a transaction UPDATE accounts SET balance = balance - 500 WHERE account_id = 123; SAVEPOINT before_withdraw; UPDATE accounts SET balance = balance + 500 WHERE account_id = 456; -- If the next statement fails, you can rollback to the "before_withdraw" savepoint. COMMIT; -- Commit the transaction`

**5\. Security and Access Control:**

* SQL allows administrators to grant or revoke permissions for users and roles to access and manipulate data.
* Example:

sql

`GRANT SELECT, INSERT, UPDATE ON employees TO HR_Manager;`

**6\. Functions:**

* SQL provides various built-in functions for performing operations on data. This includes string functions, numeric functions, and date functions.
* Example:

sql

`SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;`

**7\. Aggregation:**

* SQL supports aggregation functions such as `SUM`, `AVG`, `COUNT`, and `MAX` to perform calculations on groups of data.
* Example:

sql

`SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department;`

**8\. Joins:**

* SQL enables users to combine data from multiple tables using different types of joins, including `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, and `FULL JOIN`.
* Example:

sql

`SELECT employees.first_name, departments.department_name FROM employees INNER JOIN departments ON employees.department_id = departments.department_id;`

**9\. Subqueries:**

* Subqueries, also known as nested queries, allow users to embed one query within another query to retrieve data.
* Example:

sql

`SELECT product_name FROM products WHERE product_id IN (SELECT product_id FROM order_details WHERE order_id = 123);`

**10\. Views:**

* Views are virtual tables that provide a saved query result. They simplify complex queries and provide an additional layer of security.
* Example:

sql

`CREATE VIEW high_salary_employees AS SELECT first_name, last_name, salary FROM employees WHERE salary > 80000;`

**11\. Set Operations:**

* SQL supports set operations like `UNION`, `INTERSECT`, and `EXCEPT` to combine or compare the results of multiple queries.
* Example:

sql

`SELECT product_name FROM products WHERE category = 'Electronics' UNION SELECT product_name FROM products WHERE category = 'Appliances';`

These SQL concepts are the building blocks for working with relational databases and are essential for database management and data manipulation.

* * *

### Basics of SQL

The **Basics of SQL** include foundational concepts and statements that form the core of SQL. Whether you're querying a database, inserting data, or defining its structure, these basics are fundamental to working with SQL. Let's explore these basics in detail:

**1\. SQL Statements:**

* SQL consists of various statements, each with a specific purpose. Common statements include `SELECT`, `INSERT`, `UPDATE`, and `DELETE`.

**2\. SQL Keywords:**

* SQL keywords are reserved words that have specific meanings in SQL statements. Examples include `SELECT`, `FROM`, `WHERE`, and `JOIN`.

**3\. SQL Syntax:**

* SQL has a specific syntax that must be followed for statements to be executed correctly. For example, a basic `SELECT` statement looks like this:

sql

`SELECT column1, column2 FROM table_name WHERE condition;`

**4\. Comments:**

* SQL supports single-line and multi-line comments to document code and provide explanations. Single-line comments start with `--`, and multi-line comments are enclosed in `/* */`.

sql

`-- This is a single-line comment  /*    This is a    multi-line comment */`

**5\. Case Sensitivity:**

* SQL is generally case-insensitive for keywords, but it may be case-sensitive for data. For example, "SELECT" and "select" are equivalent, but "JohnDoe" and "johndoe" are different.

**6\. Data Types:**

* SQL supports various data types for columns, such as `INT` for integers, `VARCHAR` for variable-length character strings, and `DATE` for dates.

**7\. Wildcards:**

* SQL provides wildcard characters like `%` and `_` for pattern matching in `WHERE` clauses. `%` matches any number of characters, and `_` matches a single character.

sql

`SELECT * FROM employees WHERE last_name LIKE 'S%';`

**8\. Functions:**

* SQL includes built-in functions for data manipulation, such as `CONCAT()` for string concatenation and `SUM()` for summing values.

sql

`SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;`

**9\. Sorting and Ordering:**

* SQL allows you to sort query results using the `ORDER BY` clause, which can arrange data in ascending (default) or descending order.

sql

`SELECT product_name, price FROM products ORDER BY price DESC;`

**10\. Grouping:**

* The `GROUP BY` clause is used to group rows that have the same values in specified columns. It is often used with aggregate functions.

sql

`SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department;`

**11\. Aliases:**

* Aliases give columns or tables temporary names. This is often used to make query results more readable or to handle self-joins.

sql

`SELECT employee_id AS ID, first_name || ' ' || last_name AS full_name FROM employees;`

**12\. NULL Values:**

* SQL has special handling for NULL values, which represent missing or unknown data. You can use `IS NULL` or `IS NOT NULL` to filter data accordingly.

sql

`SELECT product_name FROM products WHERE supplier_id IS NULL;`

**13\. Data Modification:**

* SQL supports data modification statements like `INSERT`, `UPDATE`, and `DELETE` for adding, changing, or removing data from a database.

**14\. Constraints:**

* Constraints define rules for the data in a table, ensuring data integrity. Common constraints include `PRIMARY KEY`, `FOREIGN KEY`, and `CHECK`.

sql

`CREATE TABLE employees (     employee_id INT PRIMARY KEY,     first_name VARCHAR(50) NOT NULL,     last_name VARCHAR(50) NOT NULL,     hire_date DATE CHECK (hire_date >= '2000-01-01') );`

**15\. Joins:**

* Joins combine data from multiple tables based on related columns. Common join types include `INNER JOIN`, `LEFT JOIN`, and `RIGHT JOIN`.

sql

`SELECT employees.first_name, departments.department_name FROM employees INNER JOIN departments ON employees.department_id = departments.department_id;`

**16\. Subqueries:**

* Subqueries are nested queries within a larger query. They are used to retrieve data based on results from another query.

sql

`SELECT product_name FROM products WHERE product_id IN (SELECT product_id FROM order_details WHERE order_id = 123);`

**17\. Views:**

* Views are virtual tables generated by a query. They simplify complex queries and provide an additional layer of security.

sql

`CREATE VIEW high_salary_employees AS SELECT first_name, last_name, salary FROM employees WHERE salary > 80000;`

These basic SQL concepts and statements are the foundation for more advanced SQL operations and queries. They are essential for anyone working with databases and data retrieval.

* * *

### DDL, DML, DCL

In SQL, there are three main categories of SQL statements that serve different purposes: Data Definition Language (DDL), Data Manipulation Language (DML), and Data Control Language (DCL). Each category has specific commands for performing tasks related to the structure of a database, data manipulation, and data security. Let's explore these categories and their commands in detail:

**1\. Data Definition Language (DDL):**

* DDL is used to define and manage the structure of a database. It includes commands for creating, altering, and deleting database objects, such as tables, indexes, and constraints.

**Key DDL Commands:**

* `CREATE TABLE`: This command is used to create a new table in the database. It specifies the table's name, columns, data types, and constraints.
* Example:

sql

`CREATE TABLE employees (     employee_id INT PRIMARY KEY,     first_name VARCHAR(50),     last_name VARCHAR(50),     hire_date DATE );`

* `ALTER TABLE`: The `ALTER TABLE` command is used to modify an existing table's structure. You can add, modify, or delete columns, and apply constraints.
* Example:

sql

`ALTER TABLE employees ADD COLUMN salary DECIMAL(10, 2);`

* `DROP TABLE`: This command is used to delete a table and all its data from the database.
* Example:

* `CREATE INDEX`: It is used to create an index on one or more columns of a table to improve query performance.
* Example:

sql

`CREATE INDEX idx_employee_last_name ON employees(last_name);`

* `CREATE CONSTRAINT`: Constraints are rules applied to columns to ensure data integrity. Common constraints include `PRIMARY KEY`, `FOREIGN KEY`, and `CHECK`.
* Example:

sql

`ALTER TABLE orders ADD CONSTRAINT fk_customer_id FOREIGN KEY (customer_id) REFERENCES customers (customer_id);`

**2\. Data Manipulation Language (DML):**

* DML is used to manipulate data in the database. It includes commands for inserting, updating, and deleting data, as well as querying data.

**Key DML Commands:**

* `SELECT`: The `SELECT` statement is used to retrieve data from one or more tables in the database.
* Example:

sql

`SELECT first_name, last_name FROM employees WHERE department = 'HR';`

* `INSERT INTO`: This command is used to add new rows of data into a table.
* Example:

sql

`INSERT INTO products (product_name, price) VALUES ('Laptop', 1000);`

* `UPDATE`: The `UPDATE` statement is used to modify existing data in a table.
* Example:

sql

`UPDATE employees SET salary = salary * 1.1 WHERE department = 'Sales';`

* `DELETE FROM`: This command is used to remove one or more rows from a table.
* Example:

sql

`DELETE FROM products WHERE product_id = 123;`

**3\. Data Control Language (DCL):**

* DCL is used to control access to the data within the database. It includes commands for granting and revoking permissions.

**Key DCL Commands:**

* `GRANT`: The `GRANT` command is used to give specific permissions to users or roles. Permissions include SELECT, INSERT, UPDATE, DELETE, and more.
* Example:

sql

`GRANT SELECT, INSERT ON employees TO HR_Manager;`

* `REVOKE`: The `REVOKE` command is used to take back previously granted permissions from users or roles.
* Example:

sql

`REVOKE INSERT ON products FROM Marketing_Team;`

* `COMMIT`: The `COMMIT` command is used to save changes made during a transaction to the database.
* Example:

sql

`BEGIN; -- Start a transaction -- Perform data changes COMMIT; -- Save changes to the database`

* `ROLLBACK`: The `ROLLBACK` command is used to undo changes made during a transaction and return the database to its previous state.
* Example:

sql

`BEGIN; -- Start a transaction -- Perform data changes ROLLBACK; -- Undo changes and discard the transaction`

Understanding these DDL, DML, and DCL commands is essential for effectively managing databases and controlling access to data. They are the foundation of SQL operations for creating, modifying, and interacting with databases.

* * *

### Structure Creation

**Structure Creation** in SQL refers to the process of defining and creating the basic building blocks of a database, including tables, columns, data types, and constraints. Structuring a database is a critical step in database design, as it determines how data will be organized and stored. Let's explore the key aspects of structure creation:

**1\. Creating Tables:**

* Tables are the primary data storage containers in a relational database. They consist of rows and columns, where each row represents a record, and each column represents a field. You create tables using the `CREATE TABLE` statement.

**Example:**

sql

`CREATE TABLE employees (     employee_id INT PRIMARY KEY,     first_name VARCHAR(50),     last_name VARCHAR(50),     hire_date DATE );`

In the example above, we created a table named "employees" with columns for employee ID, first name, last name, and hire date.

**2\. Data Types:**

* Each column in a table has a specified data type that defines the kind of data it can store. Common data types include `INT` for integers, `VARCHAR` for variable-length character strings, and `DATE` for date values.

**Example:**

sql

`CREATE TABLE products (     product_id INT PRIMARY KEY,     product_name VARCHAR(100),     price DECIMAL(10, 2),     release_date DATE );`

In this example, we defined the data types for the "products" table columns, including product ID, product name, price, and release date.

**3\. Primary Keys:**

* A primary key is a column or set of columns that uniquely identifies each row in a table. It enforces data integrity and ensures that records are unique. You define a primary key using the `PRIMARY KEY` constraint.

**Example:**

sql

`CREATE TABLE customers (     customer_id INT PRIMARY KEY,     first_name VARCHAR(50),     last_name VARCHAR(50),     email VARCHAR(100) );`

Here, the "customer\_id" column is designated as the primary key for the "customers" table.

**4\. Constraints:**

* Constraints are rules applied to columns to maintain data integrity. Common constraints include `UNIQUE`, `NOT NULL`, and `CHECK`.

**Example:**

sql

`CREATE TABLE orders (     order_id INT PRIMARY KEY,     order_date DATE,     customer_id INT,     total_amount DECIMAL(10, 2) CHECK (total_amount >= 0) );`

In this example, we applied a `CHECK` constraint to the "total\_amount" column to ensure that it's always non-negative.

**5\. Indexes:**

* Indexes are used to improve the speed of data retrieval operations, such as searching and filtering. You can create indexes on one or more columns using the `CREATE INDEX` statement.

**Example:**

sql

`CREATE INDEX idx_employee_last_name ON employees(last_name);`

In this case, an index is created on the "last\_name" column of the "employees" table to speed up searches based on last names.

**6\. Foreign Keys:**

* Foreign keys establish relationships between tables by linking a column in one table to the primary key column in another table. This enforces referential integrity.

**Example:**

sql

`CREATE TABLE order_details (     order_detail_id INT PRIMARY KEY,     order_id INT,     product_id INT,     quantity INT,     FOREIGN KEY (order_id) REFERENCES orders(order_id),     FOREIGN KEY (product_id) REFERENCES products(product_id) );`

In the "order\_details" table, the "order\_id" and "product\_id" columns are foreign keys, referencing the primary keys in the "orders" and "products" tables.

Creating the structure of a database is a crucial aspect of SQL, as it defines how data will be organized, stored, and related within the database. Properly designed database structures are essential for data integrity and efficient data retrieval.

* * *

### Alteration

**Alteration** in SQL refers to the process of modifying an existing database structure, such as tables, columns, and constraints. It allows you to make changes to the database schema to accommodate evolving requirements or correct errors. Altering the structure of a database should be done carefully to ensure data integrity. Let's explore the key aspects of database alteration:

**1\. Adding Columns:**

* You can add new columns to an existing table using the `ALTER TABLE` statement with the `ADD COLUMN` clause.

**Example:**

sql

`ALTER TABLE employees ADD COLUMN salary DECIMAL(10, 2);`

In this example, we add a "salary" column to the "employees" table.

**2\. Modifying Columns:**

* You can modify the properties of existing columns, such as changing the data type or constraints, using the `ALTER TABLE` statement.

**Example:**

sql

`ALTER TABLE employees ALTER COLUMN hire_date SET DATA TYPE DATE;`

Here, we change the data type of the "hire\_date" column to `DATE`.

**3\. Dropping Columns:**

* Columns that are no longer needed can be dropped from a table using the `ALTER TABLE` statement with the `DROP COLUMN` clause.

**Example:**

sql

`ALTER TABLE employees DROP COLUMN middle_name;`

In this example, the "middle\_name" column is removed from the "employees" table.

**4\. Adding Constraints:**

* You can add constraints to columns in an existing table using the `ALTER TABLE` statement.

**Example:**

sql

`ALTER TABLE orders ADD CONSTRAINT fk_customer_id FOREIGN KEY (customer_id) REFERENCES customers(customer_id);`

In this case, we add a foreign key constraint to the "customer\_id" column in the "orders" table, referencing the "customer\_id" column in the "customers" table.

**5\. Removing Constraints:**

* Constraints can be removed from columns using the `ALTER TABLE` statement with the `DROP CONSTRAINT` clause.

**Example:**

sql

`ALTER TABLE products DROP CONSTRAINT product_price_check;`

Here, we remove the `CHECK` constraint named "product\_price\_check" from the "products" table.

**6\. Renaming Tables:**

* You can change the name of an existing table using the `ALTER TABLE` statement with the `RENAME TO` clause.

**Example:**

sql

`ALTER TABLE old_table_name RENAME TO new_table_name;`

In this example, the table "old\_table\_name" is renamed to "new\_table\_name."

**7\. Renaming Columns:**

* Columns within a table can be renamed using the `ALTER TABLE` statement with the `RENAME COLUMN` clause.

**Example:**

sql

`ALTER TABLE employees RENAME COLUMN first_name TO employee_first_name;`

Here, the "first\_name" column is renamed to "employee\_first\_name" in the "employees" table.

**8\. Changing Data Types:**

* You can alter the data type of a column using the `ALTER TABLE` statement with the `ALTER COLUMN` clause.

**Example:**

sql

`ALTER TABLE products ALTER COLUMN release_date SET DATA TYPE DATE;`

In this example, we change the data type of the "release\_date" column to `DATE`.

Database alteration is a necessary process to adapt to changing business requirements and maintain data integrity. It allows you to evolve the database structure while preserving the existing data.

* * *

### Defining Constraints

**Constraints** in SQL are rules or conditions applied to columns or tables to ensure data integrity, accuracy, and consistency. Constraints define limits and relationships within the data, and they are used to prevent the entry of incorrect or inconsistent data. Let's explore common types of constraints and how they are defined in SQL:

**1\. Primary Key Constraint:**

* A **Primary Key Constraint** ensures that each row in a table is uniquely identifiable. It enforces the uniqueness and non-nullability of the specified column(s).
* Primary keys are used to create relationships between tables and identify records.
* Example:

sql

`CREATE TABLE students (     student_id INT PRIMARY KEY,     first_name VARCHAR(50) NOT NULL,     last_name VARCHAR(50) NOT NULL );`

In this example, the "student\_id" column is designated as the primary key.

**2\. Unique Constraint:**

* A **Unique Constraint** enforces the uniqueness of values in a column, but unlike the primary key, it allows null values.
* It ensures that no two rows can have the same value in the specified column(s).
* Example:

sql

`CREATE TABLE employees (     employee_id INT UNIQUE,     first_name VARCHAR(50) NOT NULL,     last_name VARCHAR(50) NOT NULL );`

Here, the "employee\_id" column has a unique constraint.

**3\. Foreign Key Constraint:**

* A **Foreign Key Constraint** establishes a relationship between two tables by enforcing referential integrity. It ensures that values in one table's column match the values in another table's primary key.
* Example:

sql

`CREATE TABLE orders (     order_id INT PRIMARY KEY,     customer_id INT,     order_date DATE,     FOREIGN KEY (customer_id) REFERENCES customers(customer_id) );`

In this case, the "customer\_id" column in the "orders" table references the "customer\_id" column in the "customers" table.

**4\. Check Constraint:**

* A **Check Constraint** defines conditions that values in a column must satisfy. It allows you to restrict the range of valid values.
* Example:

sql

`CREATE TABLE products (     product_id INT PRIMARY KEY,     product_name VARCHAR(100) NOT NULL,     price DECIMAL(10, 2) CHECK (price > 0) );`

The check constraint ensures that the "price" column contains positive values.

**5\. Not Null Constraint:**

* A **Not Null Constraint** enforces that a column cannot contain null values. It ensures that every row must have a value in the specified column.
* Example:

sql

`CREATE TABLE customers (     customer_id INT PRIMARY KEY,     first_name VARCHAR(50) NOT NULL,     last_name VARCHAR(50) NOT NULL );`

In this example, both the "first\_name" and "last\_name" columns must have non-null values.

**6\. Default Constraint:**

* A **Default Constraint** provides a default value for a column if no value is specified during an insert operation.
* Example:

sql

`CREATE TABLE orders (     order_id INT PRIMARY KEY,     order_date DATE DEFAULT CURRENT_DATE );`

The "order\_date" column will have the current date as its default value if not specified.

**7\. Check Constraint for Date Range:**

* Check constraints can also be used to ensure that date values fall within a specific range.
* Example:

sql

`CREATE TABLE employees (     employee_id INT PRIMARY KEY,     hire_date DATE CHECK (hire_date >= '2000-01-01' AND hire_date <= '2023-12-31') );`

In this example, the check constraint ensures that the "hire\_date" falls within the specified date range.

Constraints are essential for maintaining data quality and consistency in a database. They help prevent errors, enforce relationships between tables, and ensure that data conforms to business rules and requirements.

* * *

### Functions

In SQL, **functions** are pre-defined operations that can be applied to data in the database. Functions allow you to perform calculations, manipulate strings, work with dates, and more. They are commonly used in SQL queries to transform and retrieve data. Here are some key aspects of SQL functions:

**1\. Built-In Functions:**

* SQL provides a wide range of built-in functions that are available for use. These functions are categorized into various types, including numeric functions, string functions, date functions, and more.

**2\. Numeric Functions:**

* Numeric functions perform operations on numeric values. Common numeric functions include `SUM`, `AVG`, `MIN`, `MAX`, and `COUNT`.

**Example:**

sql

`SELECT AVG(salary) AS avg_salary FROM employees;`

This query calculates the average salary of employees.

**3\. String Functions:**

* String functions manipulate text data. Examples of string functions include `CONCAT`, `SUBSTRING`, `UPPER`, `LOWER`, and `LENGTH`.

**Example:**

sql

`SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;`

The `CONCAT` function combines the first name and last name into a full name.

**4\. Date Functions:**

* Date functions are used to work with date and time data. Some common date functions include `CURRENT_DATE`, `DATE_FORMAT`, `DATEADD`, and `DATEDIFF`.

**Example:**

sql

`SELECT DATE_FORMAT(order_date, '%Y-%m-%d') AS formatted_date FROM orders;`

The `DATE_FORMAT` function formats the order date in a specific pattern.

**5\. Aggregate Functions:**

* Aggregate functions are used with the `GROUP BY` clause to perform calculations on groups of data. They include `SUM`, `AVG`, `MIN`, `MAX`, and `COUNT`.

**Example:**

sql

`SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department;`

This query calculates the average salary for each department.

**6\. User-Defined Functions (UDFs):**

* Some database management systems allow you to create your own user-defined functions. UDFs are custom functions created by users to perform specific tasks that are not covered by built-in functions.

**Example:**

sql

`-- Creating a simple UDF in PostgreSQL CREATE FUNCTION add_two_numbers(a INT, b INT) RETURNS INT AS $$ BEGIN   RETURN a + b; END; $$ LANGUAGE plpgsql;  -- Using the UDF SELECT add_two_numbers(5, 3) AS result;`

In this example, a user-defined function `add_two_numbers` is created to add two integers.

**7\. Case Expression:**

* The `CASE` expression is a powerful feature that allows conditional logic within a query. It can be used to perform different actions based on specified conditions.

**Example:**

sql

`SELECT   order_id,   CASE     WHEN total_amount > 1000 THEN 'High Value'     WHEN total_amount > 500 THEN 'Medium Value'     ELSE 'Low Value'   END AS order_category FROM orders;`

The `CASE` expression categorizes orders based on their total amount.

Functions in SQL are versatile and enable you to perform various operations on data, transforming and retrieving information as needed for your specific queries and reporting requirements. Whether you need to perform calculations, format data, or apply conditional logic, SQL functions provide the tools to get the job done.

* * *

### Aggregate Functions

**Aggregate functions** in SQL are used to perform calculations on sets of values and return a single result. These functions are often used in conjunction with the `GROUP BY` clause to summarize data and generate reports. Here are some key aggregate functions in SQL:

**1\. SUM:**

* The `SUM` function calculates the sum of a set of numeric values.

**Example:**

sql

`SELECT department, SUM(salary) AS total_salary FROM employees GROUP BY department;`

This query calculates the total salary for each department.

**2\. AVG:**

* The `AVG` function calculates the average of a set of numeric values.

**Example:**

sql

`SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department;`

This query calculates the average salary for each department.

**3\. MIN:**

* The `MIN` function returns the minimum (lowest) value in a set of values.

**Example:**

sql

`SELECT department, MIN(salary) AS min_salary FROM employees GROUP BY department;`

This query finds the lowest salary in each department.

**4\. MAX:**

* The `MAX` function returns the maximum (highest) value in a set of values.

**Example:**

sql

`SELECT department, MAX(salary) AS max_salary FROM employees GROUP BY department;`

This query finds the highest salary in each department.

**5\. COUNT:**

* The `COUNT` function counts the number of rows in a set of values. It can be used to count all rows or specific rows based on conditions.

**Example:**

sql

`SELECT department, COUNT(*) AS employee_count FROM employees GROUP BY department;`

This query counts the number of employees in each department.

**6\. GROUP\_CONCAT (for databases that support it):**

* The `GROUP_CONCAT` function concatenates values from multiple rows into a single string, separated by a specified delimiter.

**Example (MySQL):**

sql

`SELECT department, GROUP_CONCAT(last_name ORDER BY last_name ASC) AS employee_list FROM employees GROUP BY department;`

This query creates a list of employees' last names in each department, sorted alphabetically.

Aggregate functions are particularly useful when you need to summarize data or generate reports that provide insights into the overall trends and characteristics of your dataset.

* * *

### Built-In Functions: Numeric, Date, and String Functions

SQL provides a variety of **built-in functions** that allow you to manipulate data within your queries. These functions are categorized into different types, including numeric functions, date functions, and string functions. Let's explore these functions in more detail:

**Numeric Functions:**

1. **SUM:** The `SUM` function calculates the sum of all values in a numeric column.

sql

`SELECT SUM(total_sales) AS total_revenue FROM sales;`

2. **AVG:** The `AVG` function computes the average of numeric values in a column.

sql

`SELECT AVG(salary) AS avg_salary FROM employees;`

3. **MIN:** The `MIN` function returns the minimum (lowest) value in a numeric column.

sql

`SELECT MIN(stock_price) AS lowest_price FROM stocks;`

4. **MAX:** The `MAX` function returns the maximum (highest) value in a numeric column.

sql

`SELECT MAX(temperature) AS max_temp FROM weather_data;`

5. **ROUND:** The `ROUND` function rounds a numeric value to a specified number of decimal places.

sql

`SELECT product_name, ROUND(price, 2) AS rounded_price FROM products;`

**Date Functions:**

1. **CURRENT\_DATE:** The `CURRENT_DATE` function retrieves the current date.

sql

`SELECT CURRENT_DATE AS current_date;`

2. **DATE\_FORMAT:** The `DATE_FORMAT` function formats a date according to a specific format.

sql

`SELECT DATE_FORMAT(order_date, '%Y-%m-%d') AS formatted_date FROM orders;`

3. **DATEDIFF:** The `DATEDIFF` function calculates the difference in days between two dates.

sql

`SELECT DATEDIFF(end_date, start_date) AS days_difference FROM projects;`

4. **DATEADD (for databases that support it):** The `DATEADD` function adds a specific number of units (days, months, etc.) to a date.

sql

`SELECT DATEADD(MONTH, 3, order_date) AS future_date FROM orders;`

**String Functions:**

1. **CONCAT:** The `CONCAT` function combines two or more strings into a single string.

sql

`SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;`

2. **SUBSTRING:** The `SUBSTRING` function extracts a portion of a string.

sql

`SELECT SUBSTRING(description, 1, 50) AS short_description FROM products;`

3. **UPPER and LOWER:** The `UPPER` function converts a string to uppercase, and the `LOWER` function converts it to lowercase.

sql

`SELECT UPPER(product_name) AS uppercase_name FROM products; SELECT LOWER(email) AS lowercase_email FROM customers;`

4. **LENGTH:** The `LENGTH` function returns the length (number of characters) of a string.

sql

`SELECT product_name, LENGTH(product_name) AS name_length FROM products;`

These built-in functions make SQL a powerful language for manipulating and transforming data, allowing you to perform a wide range of operations on your database records.

* * *

### Set Operations

**Set operations** in SQL allow you to combine the results of multiple queries or compare the results of two or more queries. These operations include `UNION`, `INTERSECT`, and `EXCEPT` (or `MINUS`, depending on the database system). Let's explore how these set operations work:

**1\. UNION:**

* The `UNION` operation combines the result sets of two or more `SELECT` statements into a single result set. It removes duplicate rows by default.

**Example:**

sql

`SELECT first_name, last_name FROM employees UNION SELECT first_name, last_name FROM contractors;`

In this example, the `UNION` operation combines the names of employees and contractors into a single result set, removing duplicate names.

**2\. INTERSECT:**

* The `INTERSECT` operation returns only the rows that are common to the result sets of two or more `SELECT` statements. It effectively finds the intersection of the result sets.

**Example:**

sql

`SELECT product_name FROM inventory INTERSECT SELECT product_name FROM order_details;`

This query retrieves the product names that are both in the inventory and the order details.

**3\. EXCEPT (MINUS in some database systems):**

* The `EXCEPT` operation (or `MINUS`) returns the rows that are in the first result set but not in the second result set. It effectively subtracts one result set from another.

**Example:**

sql

`SELECT customer_name FROM customers EXCEPT SELECT customer_name FROM VIP_customers;`

This query returns the names of customers who are not in the VIP customers list.

Set operations are useful for comparing and combining data from multiple sources or for deduplicating data. They are valuable tools for working with large datasets and ensuring data consistency.

* * *

### Sub-queries

**Sub-queries**, also known as nested queries or subselects, are queries that are embedded within another query. Sub-queries are a powerful SQL feature that allows you to retrieve data from one query and then use that result within another query. Here are some important concepts related to sub-queries:

**1\. Sub-query Types:**

* **Scalar Sub-query:** Returns a single value. It can be used in the `SELECT` list, in a condition, or in a comparison.
* **Row Sub-query:** Returns one or more rows of data and can be used in a condition with operators like `IN`, `ANY`, or `ALL`.
* **Table Sub-query:** Returns a table result, which can be used as a virtual table within the main query.

**2\. Use in the `WHERE` Clause:**

* Sub-queries are often used in the `WHERE` clause to filter the results based on a condition derived from the sub-query.

**Example (Scalar Sub-query in WHERE Clause):**

sql

`SELECT product_name, price FROM products WHERE price > (SELECT AVG(price) FROM products);`

This query retrieves products with prices greater than the average price of all products.

**3\. Use with Comparison Operators:**

* Sub-queries can be used with comparison operators like `=`, `>`, `<`, and others, to compare values or conditions.

**Example (Row Sub-query with Comparison):**

sql

`SELECT customer_name FROM customers WHERE customer_id IN (SELECT customer_id FROM orders WHERE order_date > '2023-01-01');`

This query retrieves customer names who have placed orders after a specific date.

**4\. Use in the `FROM` Clause:**

* Sub-queries can be used in the `FROM` clause to create a temporary table that can be queried further.

**Example (Table Sub-query in FROM Clause):**

sql

`SELECT AVG(salary) AS avg_salary FROM (SELECT salary FROM employees WHERE department = 'Sales') AS sales_employees;`

This query calculates the average salary of employees in the Sales department.

**5\. Correlated Sub-queries:**

* A **correlated sub-query** is a sub-query that refers to values from the outer query. It can be used to perform operations on a per-row basis.

**Example (Correlated Sub-query):**

sql

`SELECT product_name FROM products WHERE price > (SELECT AVG(price) FROM products WHERE category = products.category);`

In this query, the sub-query compares products' prices to the average price of products in the same category.

Sub-queries are a versatile feature in SQL and are often used for complex filtering, data retrieval, and calculations within queries. They can help break down complex problems into more manageable components.

* * *

### Correlated Sub-queries

**Correlated sub-queries** are a type of sub-query in SQL where the inner query references one or more columns from the outer query. This correlation between the inner and outer queries allows you to perform operations that involve values from the outer query on a per-row basis. Correlated sub-queries are particularly useful for complex filtering and comparisons. Here's an in-depth explanation with examples:

**1\. Basic Correlated Sub-query:**

* A basic correlated sub-query references a column from the outer query within the sub-query.

**Example:**

sql

`SELECT product_name FROM products p WHERE price > (SELECT AVG(price) FROM products WHERE category = p.category);`

In this example, the sub-query calculates the average price of products within the same category as the product in the outer query. The result is a list of products with prices higher than the average price of their respective categories.

**2\. Using Multiple Correlated Columns:**

* Correlated sub-queries can reference multiple columns from the outer query, allowing for more complex comparisons.

**Example:**

sql

`SELECT employee_name FROM employees e WHERE salary > (SELECT AVG(salary) FROM employees WHERE department = e.department AND hire_date < e.hire_date);`

In this query, the sub-query calculates the average salary of employees in the same department as the employee in the outer query who was hired earlier. This identifies employees who earn more than the average of their colleagues who were hired before them.

**3\. Correlation in the `FROM` Clause:**

* You can use correlated sub-queries in the `FROM` clause to create temporary result sets.

**Example:**

sql

`SELECT department, COUNT(employee_id) AS num_employees FROM (SELECT DISTINCT department, employee_id FROM employees) subquery GROUP BY department;`

This query uses a sub-query in the `FROM` clause to first create a distinct list of department-employee pairs and then counts the number of employees in each department.

Correlated sub-queries are powerful tools for performing per-row operations, especially when comparing data within the context of each row's values from the outer query. They are a fundamental part of advanced SQL querying and are useful for various data analysis tasks.

* * *

### Use of GROUP BY, HAVING, and ORDER BY

The use of `GROUP BY`, `HAVING`, and `ORDER BY` clauses in SQL is essential for advanced data retrieval and analysis. These clauses allow you to group data, filter grouped data based on conditions, and sort query results. Let's explore each clause in detail:

**1\. GROUP BY:**

* The `GROUP BY` clause is used to group rows of data based on the values in one or more columns. It is typically used with aggregate functions to perform calculations within each group.

**Example:**

sql

`SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department;`

In this query, the `GROUP BY` clause groups employees by their department, and the `AVG` function calculates the average salary for each department.

**2\. HAVING:**

* The `HAVING` clause is used to filter the results of a `GROUP BY` query. It specifies conditions that apply to the grouped data, allowing you to filter groups based on aggregate function results.

**Example:**

sql

`SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department HAVING AVG(salary) > 50000;`

In this query, the `HAVING` clause filters the groups and includes only departments where the average salary is greater than $50,000.

**3\. ORDER BY:**

* The `ORDER BY` clause is used to sort the result set based on one or more columns. You can specify the sorting order as ascending (ASC) or descending (DESC).

**Example:**

sql

`SELECT product_name, price FROM products ORDER BY price DESC;`

This query sorts products by price in descending order, displaying the most expensive products first.

**4\. Combining GROUP BY, HAVING, and ORDER BY:**

* You can combine these clauses to perform complex data analysis. For example, you can group data, filter the groups with `HAVING`, and sort the results with `ORDER BY`.

**Example:**

sql

`SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department HAVING AVG(salary) > 50000 ORDER BY avg_salary DESC;`

In this query, employees are grouped by department, departments with average salaries below $50,000 are filtered out using `HAVING`, and the results are sorted by average salary in descending order.

The `GROUP BY`, `HAVING`, and `ORDER BY` clauses provide you with the tools needed to aggregate data, filter results, and control the presentation of query output. They are crucial for data analysis and reporting in SQL.

* * *

### Join and Its Types

**Joins** in SQL are used to combine rows from two or more tables based on a related column between them. Joins are fundamental for retrieving data from multiple tables and creating meaningful result sets. There are several types of joins, including inner join, left join, right join, and full outer join. Let's explore each type:

**1\. Inner Join (or Equi Join):**

* An **inner join** returns only the rows that have matching values in both tables based on the specified join condition.

**Example:**

sql

`SELECT orders.order_id, customers.customer_name FROM orders INNER JOIN customers ON orders.customer_id = customers.customer_id;`

In this query, an inner join is used to retrieve orders and their corresponding customer names based on matching customer IDs.

**2\. Left Join (or Left Outer Join):**

* A **left join** returns all rows from the left table (the first table specified) and the matching rows from the right table. If there are no matches, null values are returned for columns from the right table.

**Example:**

sql

`SELECT employees.employee_id, departments.department_name FROM employees LEFT JOIN departments ON employees.department_id = departments.department_id;`

In this query, a left join retrieves employee IDs and their corresponding department names. Employees without assigned departments will still be included in the result.

**3\. Right Join (or Right Outer Join):**

* A **right join** is similar to a left join but returns all rows from the right table and the matching rows from the left table. Rows from the left table with no matches in the right table result in null values.

**Example:**

sql

`SELECT departments.department_name, employees.employee_name FROM departments RIGHT JOIN employees ON departments.department_id = employees.department_id;`

In this query, a right join retrieves department names and the names of employees within each department. Departments with no assigned employees will still be included in the result.

**4\. Full Outer Join:**

* A **full outer join** returns all rows when there is a match in either the left or right table. It includes rows from both tables, and if there is no match, null values are returned.

**Example:**

sql

`SELECT customers.customer_name, orders.order_id FROM customers FULL OUTER JOIN orders ON customers.customer_id = orders.customer_id;`

In this query, a full outer join combines customer names with their corresponding order IDs. It includes customers with no orders and orders without assigned customers.

Joins are fundamental for combining data from multiple tables, allowing you to create comprehensive result sets for various types of queries and reports.

* * *

### Exist, Any, All

In SQL, the **EXIST**, **ANY**, and **ALL** clauses are used for comparing values within sub-queries. They help you perform comparisons and filtering based on the results of sub-queries. Let's explore each of these clauses:

**1\. EXISTS:**

* The **EXISTS** clause is used to check for the existence of rows returned by a sub-query. If the sub-query returns any rows, the outer query will return true; otherwise, it returns false.

**Example:**

sql

`SELECT product_name FROM products WHERE EXISTS (SELECT * FROM orders WHERE orders.product_id = products.product_id);`

In this query, it retrieves the names of products that have been ordered. The sub-query checks if there are any rows in the "orders" table for each product in the "products" table.

**2\. ANY:**

* The **ANY** clause is used to compare a value to the result set of a sub-query. If the value satisfies the comparison with any row from the sub-query, the condition is true.

**Example:**

sql

`SELECT product_name FROM products WHERE price > ANY (SELECT price FROM products WHERE category = 'Electronics');`

In this query, it retrieves products with prices higher than the price of any product in the 'Electronics' category.

**3\. ALL:**

* The **ALL** clause is used to compare a value to the result set of a sub-query. It only returns true if the condition is satisfied for all rows in the sub-query.

**Example:**

sql

`SELECT product_name FROM products WHERE price > ALL (SELECT price FROM products WHERE category = 'Books');`

This query retrieves products with prices higher than the price of all products in the 'Books' category.

These clauses provide powerful tools for comparing values against sets of data. They are especially useful when you need to filter data based on conditions that involve sub-queries and aggregate functions.

* * *

### Views and Their Types

In SQL, **views** are virtual tables created from the result of a SELECT query. Views allow you to encapsulate complex SQL queries, providing a simplified and reusable way to access and manipulate data in the database. There are different types of views:

**1\. Simple Views:**

* Simple views are basic views that are created using a single SELECT statement.

**Example:**

sql

`CREATE VIEW employee_info AS SELECT employee_id, first_name, last_name, hire_date FROM employees;`

In this example, a simple view named "employee\_info" is created to provide access to specific employee information.

**2\. Complex Views:**

* Complex views are created using multiple SELECT statements and may involve JOIN operations and sub-queries.

**Example:**

sql

`CREATE VIEW order_summary AS SELECT customers.customer_name, COUNT(orders.order_id) AS order_count FROM customers LEFT JOIN orders ON customers.customer_id = orders.customer_id GROUP BY customers.customer_name;`

Here, a complex view named "order\_summary" is created to provide a summary of the number of orders for each customer, including customers with no orders.

**3\. Materialized Views (not supported by all database systems):**

* Materialized views store the actual result set of the view as a physical table. They are especially useful for frequently accessed or computationally expensive views because they can improve query performance.

**Example:**

sql

`CREATE MATERIALIZED VIEW product_availability AS SELECT product_id, product_name, SUM(quantity_in_stock) AS total_stock FROM inventory GROUP BY product_id, product_name;`

In this example, a materialized view named "product\_availability" stores the total stock for each product, making it efficient for querying stock levels without frequent recalculation.

**4\. Updatable Views:**

* Updatable views allow you to insert, update, or delete data through the view, which is propagated to the underlying tables.

**Example:**

sql

`CREATE VIEW orders_with_status AS SELECT orders.order_id, order_date, order_status.status FROM orders LEFT JOIN order_status ON orders.status_id = order_status.status_id;`

This view, "orders\_with\_status," can be used to update order statuses, and those updates will be reflected in the underlying "orders" and "order\_status" tables.

Views are beneficial for simplifying complex queries, enhancing data security by restricting access to certain columns or rows, and promoting data consistency. They provide a way to create a logical layer over your database, making it easier to work with data.
