# Unit 5: DBMS and BIRT

- [Unit 5: DBMS and BIRT](#unit-5-dbms-and-birt)
    - [Introduction to Databases](#introduction-to-databases)
    - [Schema Creation](#schema-creation)
    - [Keys](#keys)
    - [Relation Creation](#relation-creation)
    - [Data Insertion](#data-insertion)
    - [SELECT: Data Retrieval](#select-data-retrieval)
    - [Drop and Truncate Relation](#drop-and-truncate-relation)
    - [Data Upload via CSV file](#data-upload-via-csv-file)
    - [Where Clause](#where-clause)
    - [Order by Clause](#order-by-clause)
    - [Aggregate Functions](#aggregate-functions)
    - [Group by Clause](#group-by-clause)
    - [And Or In Not In](#and-or-in-not-in)
    - [Between](#between)
    - [Like Not Like](#like-not-like)
    - [Distinct](#distinct)
    - [Nested Queries](#nested-queries)
    - [Having Clause](#having-clause)
    - [Union and Intersection](#union-and-intersection)
    - [Joins (Inner, Left, Right, Full Outer)](#joins-inner-left-right-full-outer)
    - [Business Performance Management Systems](#business-performance-management-systems)

### Introduction to Databases

A **database** is a structured collection of data organized for efficient retrieval and management. Databases are essential in modern computing and serve as the foundation for storing, retrieving, and manipulating data. Key concepts in database management include data models, database systems, and database management systems (DBMS).

- **Data Models:** Data models define the structure and organization of data in a database. Common data models include the relational model, hierarchical model, and network model.

- **Database Systems:** Database systems are software applications that facilitate data storage, retrieval, and management. They include the database engine, query language, and data manipulation tools.

- **DBMS:** A Database Management System (DBMS) is software that provides an interface for users and applications to interact with the database. It handles tasks such as data storage, retrieval, security, and data integrity.

### Schema Creation

In the context of databases, a **schema** is a blueprint that defines the structure of the database, including tables, columns, relationships, and constraints. Creating a schema involves designing the database's architecture, determining data types, setting constraints, and defining relationships between tables. The schema acts as a guide for data entry, retrieval, and management within the database.

### Keys

In a relational database, a **key** is a field or combination of fields that uniquely identifies a record in a table. Different types of keys include:

- **Primary Key:** A primary key is a unique identifier for each record in a table. It enforces data integrity and is used to establish relationships between tables.

- **Foreign Key:** A foreign key is a field in one table that references the primary key in another table. It creates relationships between tables, ensuring data consistency.

- **Super Key:** A super key is a set of one or more fields that can be used to uniquely identify records in a table.

- **Candidate Key:** A candidate key is a minimal super key, meaning no subset of the candidate key can uniquely identify records.

Understanding keys is crucial for database design and maintaining data integrity.

### Relation Creation

In the context of a relational database, a **relation** refers to a table with rows and columns. Each row represents a record, while each column represents an attribute or field. Creating relations involves defining the table structure, specifying column data types, and setting constraints, including primary keys and foreign keys.

### Data Insertion

**Data insertion** is the process of adding records or rows to a database table. The data to be inserted must adhere to the table's schema, including data types, constraints, and key relationships. Inserting data is a fundamental operation for populating a database with information.

### SELECT: Data Retrieval

The **SELECT** statement is a fundamental SQL command used to retrieve data from a database. It allows you to specify which columns to retrieve, which table(s) to query, and optional filtering conditions. The result of a SELECT query is a result set containing rows and columns of data that meet the specified criteria.

### Drop and Truncate Relation

- **DROP:** The **DROP** statement in SQL is used to delete a table, including all of its data and schema. It is a non-recoverable operation and permanently removes the table from the database.

- **TRUNCATE:** The **TRUNCATE** statement is used to remove all rows from a table but retains the table structure. It is faster than DELETE for removing all data but does not return the table to its initial state.

### Data Upload via CSV file

Uploading data from a CSV (Comma-Separated Values) file to a database is a common task. It involves using SQL or a database management tool to import data from an external CSV file into a specified table. This is useful for bulk data insertion and updating.

### Where Clause

The **WHERE** clause in SQL is used to filter records in a SELECT statement. It specifies a condition that data must meet to be included in the result set. For example, you can use the WHERE clause to retrieve records with specific values in a particular column.

### Order by Clause

The **ORDER BY** clause in SQL allows you to specify the order in which records are returned in the result set. You can sort records in ascending (ASC) or descending (DESC) order based on one or more columns. It is commonly used to present data in a meaningful sequence.

### Aggregate Functions

**Aggregate functions** in SQL perform calculations on sets of values and return a single value as the result. Common aggregate functions include:

- **SUM:** Calculates the sum of values in a column.
- **AVG:** Calculates the average of values in a column.
- **COUNT:** Counts the number of records in a column.
- **MIN:** Retrieves the minimum value from a column.
- **MAX:** Retrieves the maximum value from a column.

Aggregate functions are useful for summarizing and analyzing data.

### Group by Clause

The **GROUP BY** clause in SQL is used in conjunction with aggregate functions to group rows based on the values in one or more columns. It allows you to perform aggregate calculations on groups of data, enabling the analysis of data at a higher level of granularity.

### And Or In Not In

**AND**, **OR**, **IN**, and **NOT IN** are logical operators in SQL used to combine conditions in the WHERE clause. They help you create complex criteria for filtering and retrieving data. For example, you can use AND to require that multiple conditions be met, OR to select rows that meet at least one condition, IN to match a value against a list of values, and NOT IN to exclude values from a list.

### Between

The **BETWEEN** operator in SQL is used to specify a range of values for a column. It simplifies the process of specifying a range and is often used in conjunction with the AND operator. For example, you can use BETWEEN to retrieve records with values within a specific date range.

### Like Not Like

The **LIKE** and **NOT LIKE** operators are used for pattern matching in SQL. They are typically used with wildcard characters to search for records that match a pattern. For instance, you can use % as a wildcard to match any number of characters or _ to match a single character.

### Distinct

The **DISTINCT** keyword in SQL is used to retrieve unique values from a column. It eliminates duplicate values and returns a distinct set of records. DISTINCT is useful when you want to identify unique values within a column.

### Nested Queries

**Nested queries** (subqueries) in SQL involve embedding one query within another query. Subqueries are used to retrieve data that will be used in the main query as a condition or filter. For example, you can use a subquery to find the highest salary in a department and then use that value in the main query.

### Having Clause

The **HAVING** clause in SQL is similar to the WHERE clause but is used with aggregate functions. It filters the results of a GROUP BY query based on the results of aggregate functions. HAVING is used to impose conditions on the aggregated data.

### Union and Intersection

- **UNION:** The **UNION** operator in SQL is used to combine the result sets of two or more SELECT queries into a single result set. It eliminates duplicate rows and returns a unique set of records.

- **INTERSECTION:** SQL does not have a built-in INTERSECTION operator. You can achieve the same result using the INTERSECT keyword in some database systems or by using subqueries.

### Joins (Inner, Left, Right, Full Outer)

**Joins** in SQL are used to retrieve data from multiple tables based on a related column between them. There are several types of joins:

- **Inner Join:** Retrieves rows that have matching values in both tables.
- **Left Join:** Retrieves all rows from the left table and the matching rows from the right table. Non-matching rows in the left table will have NULL values for columns from the right table.
- **Right Join:** Similar to the left join but retrieves all rows from the right table and the matching rows from the left table.
- **Full Outer Join:** Retrieves all rows when there is a match in either the left or right table. Non-matching rows will have NULL values for columns from the non-matching table.

Joins are essential for combining data from different tables and performing complex queries.

### Business Performance Management Systems

**Business Performance Management (BPM) systems** are software applications and methodologies that help organizations monitor, measure, and manage their performance and strategic goals. BPM systems provide tools for collecting, analyzing, and visualizing data related to key performance indicators (KPIs) and strategic objectives.

BPM systems often include features for budgeting, forecasting, scorecarding, and dashboards. They are used by organizations to improve decision-making, align strategies with objectives, and drive better business performance.
