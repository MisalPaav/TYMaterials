# UDBMS CAE 2 Question Bank Solution

<div style="position: relative; width: 100%; height: auto; max-width: 100%; padding-top: 56.25%;">
  <iframe src="https://drive.google.com/file/d/1nObjD6KG8HIMSpZxs3VuvbCghniJ-6Za/preview" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" frameborder="0" scrolling="no"></iframe>
</div>

## Solutions

### 1\. Discuss master-slave, peer to peer replication models

**Master-Slave Replication:** In a master-slave replication model, there is a single master node and one or more slave nodes. The master node is responsible for handling all write operations (inserts, updates, deletes), while the slave nodes replicate data from the master. Read operations can be distributed among both the master and slave nodes.

- **Advantages:**
  - Provides a single point for writes, ensuring consistency.
  - Can distribute read operations among multiple nodes, improving read performance.
  - Simple to set up and manage.
- **Disadvantages:**
  - Single point of failure: If the master node fails, the system becomes unavailable for writes until a new master is elected.
  - Read scalability is limited to the capacity of the master node.

**Peer-to-Peer Replication:** In a peer-to-peer replication model, all nodes are peers, meaning they can both read and write data. Each node maintains its own copy of the data, and changes made to one node are propagated to all other nodes in the network.

- **Advantages:**
  - No single point of failure: If one node goes down, the system remains available as other nodes can still handle requests.
  - Provides better write scalability since write operations can be distributed across multiple nodes.
  - Can improve read performance by distributing read operations among multiple nodes.
- **Disadvantages:**
  - More complex to set up and manage compared to master-slave replication.
  - Requires a mechanism to handle conflicts when updates are made to the same data on different nodes simultaneously.

### 2\. Discuss scale out in Mongo DB in detail. How does scale out occur in Mongo DB?

Scale-out in MongoDB refers to the ability to horizontally scale the database by adding more servers or nodes to the existing infrastructure. This is achieved through sharding, which involves partitioning data across multiple servers based on a shard key.

**How Scale-Out Occurs in MongoDB:**

1. **Sharding:**

    - MongoDB divides data into chunks based on a shard key, which is a field or fields chosen to distribute data across shards.
    - Each shard is a separate MongoDB instance or replica set.
    - The shard key determines which shard will store the data for a particular document.
2. **Adding Shards:**

    - When the data size exceeds the capacity of a single server, additional shards can be added to the cluster.
    - MongoDB automatically redistributes data across the new shards according to the shard key.
3. **Balancing Data:**

    - MongoDB's balancer process continually monitors the distribution of data across shards and moves chunks between shards as needed to maintain a balanced cluster.
4. **Config Servers:**

    - MongoDB uses config servers to store metadata about the cluster, including the mapping between shard keys and chunks.
    - Config servers are deployed as a replica set for redundancy.
5. **Query Routing:**

    - MongoDB routers (mongos) receive client requests and route them to the appropriate shard based on the shard key.
    - Routers also aggregate results from multiple shards for queries that span multiple chunks.

### 3\. Elaborate the application needs where Cassandra should not be used

Cassandra is a highly scalable and distributed NoSQL database designed for handling large amounts of data across multiple commodity servers with no single point of failure. However, there are certain scenarios where Cassandra may not be the best choice:

- **Small-Scale Applications:** Cassandra's distributed nature and overhead may not be justified for small-scale applications with low data volumes and simple data access patterns.

- **Transactional Workloads:** Cassandra sacrifices consistency for availability and partition tolerance (CAP theorem). Therefore, it may not be suitable for applications requiring strong consistency guarantees, such as financial transactions.

- **Complex Joins and Aggregations:** Cassandra is optimized for fast writes and scalable reads but does not support complex joins and aggregations like traditional relational databases. Applications heavily reliant on complex queries may not perform well with Cassandra.

- **Frequent Updates or Deletes:** Cassandra's data model is optimized for high write throughput but may experience performance issues with frequent updates or deletions due to the nature of its distributed architecture and compaction process.

- **Limited Analytical Capabilities:** While Cassandra supports basic analytics through features like secondary indexes and materialized views, it is not designed for complex analytical queries typical in data warehousing or business intelligence applications.

### 4\. Assume there is a collection named users that looks like the one below. How can you get all houses in the “Rabia” neighborhood?

```javascript
[
 {
    "_id" : ObjectId("5d011c94ee66e13d34c7c388"),
    "userName" : "kevin",
    "email" : "kevin@toptal.com",
    "password" : "affdsg342",
    "houses" : [
        {
            "name" : "Big Villa",
            "neighborhood" : "Zew Ine"
        },
        {
            "name" : "Small Villa",
            "neighborhood" : "Rabia"
        }
    ]
 },
{
    "_id" : ObjectId("5d011c94ee66e13d34c7c387"),
    "userName" : "sherif",
    "email" : "sharief@toptal.com",
    "password" : "67834783ujk",
    "houses" : [
        {
            "name" : "New Mansion",
            "neighborhood" : "Nasr City"
        },
        {
            "name" : "Old Villa",
            "neighborhood" : "Rabia"
        }
    ]
 },
]
```

#### Ans

To retrieve all houses in the "Rabia" neighborhood from the provided collection, you can use the following MongoDB query:

`db.collection.find({"houses.neighborhood": "Rabia"}, {"houses.$": 1})`

This query searches for documents where the "houses" array contains an object with the "neighborhood" field equal to "Rabia". The projection parameter `{"houses.$": 1}` ensures that only the matched element from the "houses" array is returned in the result.

### 5\. Assume there is a document with nested arrays that looks like the one below. How can you insert a “room” that has the name “Room 44” and size of “50” for a particular G H Raisoni College of Engineering & Management, Wagholi, Pune Department of Computer Engineering Class: T. Y B. Tech (A, B, C) Subject: UCOL307: Unstructured Database Management System “house” that belongs to this user?

```javascript
{
  "_id": "682263",
  "userName": "sherif",
  "email": "sharief@aucegypt.edu",
  "password": "67834783ujk",
  "houses": [
    {
      "_id": "2178123",
      "name": "New Mansion",
      "rooms": [
        {
          "name": "4th bedroom",
          "size": "12"
        },
        {
          "name": "kitchen",
          "size": "100"
        }
      ]
    }
  ]
}
```

#### Ans

To insert a new room for a specific house belonging to a user in the provided document, you can use the following MongoDB update query:

```javascript
db.collection.update(
  {
    "userName": "sherif",
    "houses._id": "2178123"
  },
  {
    $push: {
      "houses.$.rooms": {
        "name": "Room 44",
        "size": "50"
      }
    }
  }
)
```

This query updates the document where the "userName" is "sherif" and contains a house with "_id" equal to "2178123". It uses the `$push` operator to append a new room object to the "rooms" array of the matched house.

### 6\. Features of Cassandra

Cassandra, a distributed NoSQL database, offers several features:

- **Distributed Architecture:** Cassandra is designed to run on a cluster of commodity hardware, distributing data across multiple nodes for high availability and scalability.

- **Linear Scalability:** Adding more nodes to a Cassandra cluster increases its capacity linearly, allowing it to handle growing amounts of data and traffic.

- **High Availability:** Cassandra ensures data availability even in the face of node failures through its distributed architecture and data replication strategies.

- **No Single Point of Failure:** Data is replicated across multiple nodes, ensuring that the system remains available even if some nodes fail.

- **Tunable Consistency:** Cassandra allows users to configure consistency levels per operation, providing flexibility to balance consistency requirements with performance.

- **Schema-Free:** Cassandra does not require a fixed schema, allowing for flexible data models and schema evolution over time.

- **Partition Tolerance:** Cassandra partitions data across nodes using consistent hashing, ensuring that data remains available and accessible even if some nodes are unreachable.

- **Tunable CAP Theorem:** Cassandra allows users to trade off consistency for availability and partition tolerance based on their application requirements.

### 7\. Use Cases of MongoDB

MongoDB is a versatile NoSQL database used in various applications:

- **Content Management Systems:** MongoDB's flexible schema and support for large volumes of unstructured data make it well-suited for content management systems handling diverse content types.

- **Real-Time Analytics:** MongoDB's ability to handle high write loads and its flexible data model make it suitable for real-time analytics applications, such as user behavior analysis and monitoring.

- **Mobile and Social Applications:** MongoDB's scalability and ease of integration with mobile and web frameworks make it a popular choice for mobile and social applications requiring fast and flexible data access.

- **Catalog and Product Management:** MongoDB's document-oriented data model is ideal for catalog and product management systems, allowing for easy representation of complex product hierarchies and attributes.

- **Internet of Things (IoT):** MongoDB's ability to handle large volumes of time-series data and its support for geospatial queries make it suitable for IoT applications, such as sensor data collection and analysis.

### 8\. Consistency Settings of Cassandra

Cassandra offers several consistency levels to balance consistency, availability, and partition tolerance:

- **Consistency Level ONE (CL=1):** Requires a single replica to respond to a read or write operation, offering the lowest consistency but highest availability.

- **Consistency Level QUORUM (CL=QUORUM):** Requires a majority of replicas to respond, ensuring strong consistency across multiple replicas while maintaining availability and partition tolerance.

- **Consistency Level ALL (CL=ALL):** Requires all replicas to respond, offering the strongest consistency guarantee but potentially impacting availability, especially in large clusters.

- **Consistency Level LOCAL_ONE (CL=LOCAL_ONE):** Requires only one replica in the local data center to respond, providing low-latency reads and writes with eventual consistency.

- **Consistency Level LOCAL_QUORUM (CL=LOCAL_QUORUM):** Requires a quorum of replicas in the local data center to respond, offering strong consistency within the data center while still providing high availability and partition tolerance.

### 9\. Using MapReduce to Calculate Revenue Generated by a Book in January

MapReduce can be used to calculate the revenue generated by a book in January by following these steps:

1. **Map Function:**

    - The map function takes input data (e.g., sales transactions) and emits key-value pairs where the key is the book ID and the value is the revenue generated by the sale.
    - It filters out transactions that do not occur in January.

2. **Reduce Function:**

    - The reduce function takes the output of the map function and aggregates the revenue for each book ID.
    - It sums up the revenue values for each book ID.

3. **Execution:**

    - MapReduce is executed on the dataset containing sales transactions.
    - The output is the total revenue generated by each book in January.

Example pseudocode for MapReduce in MongoDB:

```javascript
// Map Function
var mapFunction = function() {
    var month = this.date.getMonth(); // Extract month from date
    if (month === 0) { // January
        emit(this.bookId, this.price);
    }
};

// Reduce Function
var reduceFunction = function(key, values) {
    return Array.sum(values);
};

// Execute MapReduce
db.sales.mapReduce(
    mapFunction,
    reduceFunction,
    { out: "january_revenue" }
);
```

This code calculates the revenue generated by each book in January and stores the results in the "january_revenue" collection.

### 10\. Replication for Increased Read Performance in NoSQL Databases

Replication in NoSQL databases, such as MongoDB and Cassandra, can improve read performance by distributing read requests across multiple replicas of the data:

- **Load Balancing:** Replicas can be used to distribute read requests, reducing the load on individual nodes and improving overall read performance.

- **Geographic Distribution:** Replicas can be placed in different geographical regions to reduce latency for users accessing the data from different locations.

- **Fault Tolerance:** Replicas provide redundancy, ensuring that read requests can still be served even if some nodes fail, thereby increasing availability and reliability.

- **Read Scalability:** By adding more replicas, the database can handle a higher volume of read requests in parallel, scaling out read performance horizontally.

- **Consistency Guarantees:** Depending on the consistency level chosen, replicas can provide either strong consistency or eventual consistency, allowing users to balance performance and consistency requirements.

### 11\. Comparison of RDBMS and MongoDB Schema

**RDBMS (Relational Database Management System) Schema:**

- RDBMS uses a predefined schema that defines the structure of the database, including tables, columns, data types, constraints, and relationships.
- Tables must have a fixed schema where each column has a predefined data type and constraints (e.g., primary keys, foreign keys, not null).
- Altering the schema often requires modifying the entire database structure, potentially causing downtime and complex migration processes.
- RDBMS enforces strict adherence to the schema, ensuring data integrity and consistency.

**MongoDB Schema:**

- MongoDB uses a flexible schema known as a schema-less or schema-on-read approach.
- Data in MongoDB is stored as flexible, JSON-like documents within collections, allowing each document within a collection to have a different structure.
- Documents within a collection can have varying sets of fields, data types, and structures, enabling easy adaptation to evolving application requirements.
- MongoDB does not enforce a schema at the database level, allowing for dynamic updates and changes to the data model without downtime.
- This flexibility allows developers to store and query data in a more natural and intuitive way, accommodating diverse data types and evolving application needs.

**Justification of MongoDB's Flexible Schema:**

- MongoDB's schema flexibility enables developers to iterate quickly and adapt to changing requirements without the need for complex schema migrations.
- New fields can be added to documents on-the-fly without affecting existing data, facilitating agile development and experimentation.
- MongoDB's dynamic schema supports polymorphic data structures, allowing documents within the same collection to have different fields and structures based on their specific needs.
- The absence of a fixed schema reduces development overhead and administrative complexity, particularly in applications with rapidly changing data models or large-scale data migration requirements.

### 12\. MapReduce Architecture and Application to Amazon's Total Sales Calculation

**MapReduce Architecture:**

MapReduce is a programming model and processing framework for distributed computing on large datasets. It consists of two main phases:

1. **Map Phase:**

    - Input data is divided into smaller chunks, and a map function is applied to each chunk in parallel.
    - The map function processes each input record and emits key-value pairs as intermediate outputs.
2. **Reduce Phase:**

    - Intermediate key-value pairs with the same key are grouped together, and a reduce function is applied to each group.
    - The reduce function aggregates values associated with the same key, producing the final output.

**Application to Amazon's Total Sales Calculation:**

1. **Map Phase:**

    - Input data consists of sales transactions, each containing the date and sale amount.
    - The map function extracts the year from each transaction's date and emits key-value pairs with the year as the key and the sale amount as the value.
2. **Reduce Phase:**

    - Intermediate key-value pairs are grouped by year.
    - The reduce function calculates the total sales amount for each year by summing up the sale amounts associated with the same year.

**Diagram:**

```sql
+-----------------+      +------------+      +----------------+
| Input Data      | ---> | Map        | ---> | Intermediate   |
| (Sales Data)    |      | Function   |      | Key-Value Pairs|
+-----------------+      +------------+      +----------------+
                                |
                                v
                         +------------+
                         | Reduce     |
                         | Function   |
                         +------------+
                                |
                                v
                       +----------------+
                       | Final Results  |
                       +----------------+
```

### 13\. Application Needs Where MongoDB Should Not Be Used

MongoDB may not be suitable for certain application scenarios, including:

- **ACID Transactions:** MongoDB sacrifices some level of ACID compliance for scalability and performance. Applications requiring strict ACID transactions (e.g., financial transactions) may be better suited for traditional RDBMSs.

- **Complex Joins and Aggregations:** While MongoDB supports basic querying and aggregation operations, it lacks the sophisticated join capabilities of relational databases. Applications heavily reliant on complex joins and aggregations may face performance limitations.

- **Structured Data with Fixed Schema:** MongoDB's flexible schema is well-suited for semi-structured and unstructured data. However, applications with highly structured data and rigid schema requirements may benefit from the relational model provided by RDBMSs.

- **Limited Analytical Capabilities:** MongoDB is optimized for operational workloads rather than complex analytical queries. Applications requiring advanced analytics, data warehousing, or business intelligence may require specialized tools or technologies.

- **Legacy Systems and Integration:** Migrating legacy systems built on relational databases to MongoDB may require significant effort and may not always be feasible or practical, especially if the existing systems rely heavily on SQL-based features.

### 14\. Use Cases of Cassandra

Cassandra is well-suited for the following use cases:

- **Highly Scalable Web Applications:** Cassandra's distributed architecture and linear scalability make it ideal for web applications requiring high availability and scalability, such as social media platforms, content management systems, and e-commerce websites.

- **Time-Series Data and IoT:** Cassandra's ability to handle large volumes of time-series data and its linear scalability make it suitable for IoT applications, sensor data collection, telemetry data, and real-time analytics.

- **Distributed Data Management:** Cassandra's decentralized architecture and built-in replication support make it well-suited for distributed data management across multiple data centers, geographical regions, or cloud environments.

- **Real-Time Analytics:** Cassandra's ability to handle high write throughput and support for fast read operations make it suitable for real-time analytics use cases, such as monitoring, fraud detection, and recommendation systems.

- **Highly Available Databases:** Cassandra's fault-tolerant design and tunable consistency levels make it ideal for building highly available databases that can withstand node failures, network partitions, and data center outages.

### 15\. Cassandra's Suitability for IoT and E-Commerce

**IoT (Internet of Things):**

- Cassandra's ability to handle massive volumes of time-series data and its linear scalability make it well-suited for IoT applications.
- It can efficiently store sensor data, telemetry data, and device logs, providing fast read and write access to real-time data streams.
- Cassandra's decentralized architecture ensures high availability and fault tolerance, crucial for IoT deployments spanning multiple geographical regions.

**E-Commerce:**

- Cassandra's distributed architecture and linear scalability make it ideal for e-commerce applications requiring high availability, scalability, and low latency.
- It can handle large volumes of product data, user profiles, and transactional data, providing fast read and write access to product catalogs, user sessions, and order processing.
- Cassandra's tunable consistency levels allow e-commerce platforms to balance consistency and performance, ensuring that users receive accurate product information and timely order updates.

### 16\. Queries for Cassandra

#### 1\. Creating Keyspace for Student Data

```sql
CREATE KEYSPACE IF NOT EXISTS student_keyspace
WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 3};
```

- This query creates a keyspace named `student_keyspace` if it does not already exist.
- The keyspace is configured with a replication strategy of `SimpleStrategy` and a replication factor of `3`, meaning that data will be replicated across 3 nodes.

#### 2\. Inserting Data in Keyspace

```sql
INSERT INTO student_keyspace.students (student_id, name, age, department)
VALUES ('1001', 'John Doe', 20, 'Computer Science');
```

- This query inserts a new student record into the `students` table within the `student_keyspace`.
- It specifies values for the `student_id`, `name`, `age`, and `department` fields.

### 17\. findOne Method and Pretty Method in MongoDB

**findOne Method:**

- `findOne`

Method in MongoDB is used to retrieve a single document from a collection that matches a specified query criteria. It returns the first document that satisfies the query condition within the collection. If no document matches the query, it returns null.

**Syntax:**

- `db.collection.findOne(filter, projection)`

  - `filter`: Specifies the query criteria to filter documents.
  - `projection` (optional): Specifies which fields to include or exclude in the returned document.

**Pretty Method:**

- The `pretty()` method in MongoDB is used to format the output of the result set in a more readable and indented JSON format.
- It's often used in conjunction with commands like `find()` or `aggregate()` to make the output more human-readable.

**Syntax:**

- `db.collection.find().pretty()`

- This method adds indentation and line breaks to the returned documents, making them easier to read, especially when dealing with large or complex documents.

### 18\. Data Types Used in MongoDB

MongoDB supports various data types for storing and representing data within documents. Some of the commonly used data types include:

1. **String**: Used to store textual data.
2. **Integer**: Used to store numeric whole numbers.
3. **Double**: Used to store floating-point numbers.
4. **Boolean**: Used to store boolean values (`true` or `false`).
5. **Date**: Used to store date and time values.
6. **Array**: Used to store arrays or lists of values.
7. **Object**: Used to embed documents within other documents.
8. **ObjectId**: A unique identifier for documents, automatically generated by MongoDB.
9. **Null**: Used to represent null or empty values.
10. **Binary Data**: Used to store binary data such as images or files.
11. **Regular Expression**: Used to store regular expression patterns.

MongoDB also supports various data types for geospatial data, such as `GeoJSON` objects for representing points, lines, and polygons on a map.

### 19\. Use of Timeout in Cassandra

In Cassandra, timeouts are used to control the duration for various operations to complete. Timeouts are crucial for preventing operations from hanging indefinitely and potentially causing resource contention or performance degradation. Some common uses of timeouts in Cassandra include:

- **Read and Write Operations:** Timeout settings can be configured for read and write operations to specify the maximum time allowed for the operation to complete. If the operation exceeds the specified timeout period, it will be aborted, and an error will be returned to the client.

- **Node and Cluster Communication:** Timeout settings also control the duration for communication between nodes and clusters. This ensures that nodes respond within a reasonable time frame, preventing network congestion or node unresponsiveness from affecting the overall system's performance.

- **Consistency Levels:** Timeout settings play a crucial role in consistency levels, determining how long the system waits for responses from replicas before returning a result to the client. Higher consistency levels typically require longer timeouts to ensure data consistency across replicas.

- **Failure Detection:** Timeout settings are used for failure detection mechanisms within Cassandra. If a node fails to respond within the specified timeout period, it may be marked as unresponsive or unreachable, triggering failover mechanisms to maintain system availability.

Properly configuring timeout settings is essential for maintaining system stability, preventing performance bottlenecks, and ensuring timely responses to client requests in Cassandra.

### 20\. Why NoSQL Databases are Not Suitable for Applications Needing Complex Queries and Transactions

NoSQL databases prioritize scalability, flexibility, and performance over strict consistency and complex query support. As a result, they may not be suitable for applications needing complex queries and transactions due to the following reasons:

- **Limited Query Capabilities:** NoSQL databases often lack advanced querying features compared to traditional relational databases. They typically support basic CRUD (Create, Read, Update, Delete) operations and simple query patterns but may struggle with complex join operations, aggregations, and ad-hoc queries.

- **Denormalized Data Model:** NoSQL databases favor denormalized data models to improve performance and scalability. While this approach enhances read and write performance, it may lead to data duplication and redundancy, making complex queries and transactions more challenging to execute efficiently.

- **Eventual Consistency:** Many NoSQL databases, especially those following the BASE (Basically Available, Soft state, Eventually consistent) model, prioritize availability and partition tolerance over strict consistency. As a result, they may exhibit eventual consistency, where data updates may take time to propagate across replicas. This can lead to inconsistency issues in applications requiring immediate and guaranteed consistency.

- **Limited Transaction Support:** NoSQL databases often offer limited support for ACID (Atomicity, Consistency, Isolation, Durability) transactions compared to relational databases. They may provide only eventual consistency or support transactions at the document or partition level, which may not be sufficient for applications with complex transactional requirements.

- **Data Model Complexity:** NoSQL databases are optimized for handling semi-structured and unstructured data, making them suitable for use cases like web applications, content management systems, and real-time analytics. However, they may struggle with applications requiring complex data models, intricate relationships, and transactional integrity.

While NoSQL databases offer advantages in scalability, performance, and flexibility, they may not be the best fit for applications needing complex queries and transactions that traditional relational databases excel at handling. It's essential to carefully evaluate the requirements of your application and choose the appropriate database technology based on factors like data model complexity, query flexibility, consistency requirements, and transactional support.
