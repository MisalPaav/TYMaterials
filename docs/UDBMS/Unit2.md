# Unit 2

- [Unit 2: Test Case Design Strategies](#unit-2-test-case-design-strategies)
  - [Comparison of Relational Databases to New NoSQL Stores](#comparison-of-relational-databases-to-new-nosql-stores)
  - [MongoDB, Cassandra, HBASE, Neo4j Use and Deployment](#mongodb-cassandra-hbase-neo4j-use-and-deployment)
  - [Application, RDBMS Approach](#application-rdbms-approach)
  - [Challenges NoSQL Approach](#challenges-nosql-approach)
  - [Key-Value and Document Data Models](#key-value-and-document-data-models)
  - [Column-Family Stores](#column-family-stores)
  - [Aggregate-Oriented Databases](#aggregate-oriented-databases)
  - [Replication and Sharding](#replication-and-sharding)
  - [MapReduce on Databases](#mapreduce-on-databases)
  - [Distribution Models](#distribution-models)
  - [Single Server](#single-server)
  - [Sharding](#sharding)
  - [Master-Slave Replication](#master-slave-replication)
  - [Peer-to-Peer Replication](#peer-to-peer-replication)
  - [Combining Sharding and Replication](#combining-sharding-and-replication)

### Comparison of Relational Databases to New NoSQL Stores

Relational databases and NoSQL stores represent two distinct approaches to data management, each with its strengths and weaknesses.

**Relational Databases:**

1. **Data Structure:** Relational databases organize data into tables with predefined schemas, enforcing a structured, tabular format.
2. **ACID Properties:** They adhere to ACID properties, ensuring transactions are Atomic, Consistent, Isolated, and Durable, which is crucial for applications requiring data integrity.
3. **Schema:** Relational databases require a predefined schema, offering a clear blueprint for data structure and relationships.
4. **Joins:** Relationships between tables are established through joins, allowing complex queries across multiple tables.
5. **Use Cases:** Well-suited for applications with complex relationships, transactional requirements, and structured data, such as financial systems or enterprise applications.

**NoSQL Stores (MongoDB, Cassandra, HBASE, Neo4j):**

1. **Data Structure:** NoSQL stores offer flexibility in handling unstructured or semi-structured data, allowing for dynamic and evolving data models.
2. **CAP Theorem:** NoSQL databases often adhere to the CAP theorem (Consistency, Availability, Partition tolerance), providing high availability and partition tolerance at the expense of strict consistency.
3. **Schema-less Design:** NoSQL databases typically embrace a schema-less or schema-flexible design, allowing for agile development and adaptation to changing data requirements.
4. **Scalability:** NoSQL databases excel in horizontal scalability, making them suitable for applications with massive amounts of data and high scalability requirements.
5. **Use Cases:** NoSQL databases are well-suited for applications with large-scale data requirements, real-time analytics, content management, and scenarios where flexibility in data models is crucial.

### MongoDB, Cassandra, HBASE, Neo4j Use and Deployment

**MongoDB:**

- **Use:** Document-oriented NoSQL database.
- **Deployment:** Widely used for web applications, content management systems, and real-time applications.

**Cassandra:**

- **Use:** Column-family NoSQL database.
- **Deployment:** Ideal for time-series data, event logging, and applications requiring high write throughput and horizontal scalability.

**HBASE:**

- **Use:** Column-family NoSQL database.
- **Deployment:** Suited for applications demanding random read/write access, such as large-scale analytics and content serving systems.

**Neo4j:**

- **Use:** Graph database.
- **Deployment:** Used for applications involving complex relationships, such as social networks, fraud detection, and recommendation engines.

### Application, RDBMS Approach

**Application Approach:**

- **Relational Databases:** Applications using relational databases often follow a structured and normalized data model, leveraging SQL for querying and transactions.
- **NoSQL Approach:** NoSQL databases allow for more flexibility in adapting to changing application requirements. Schema changes can be made without significant disruptions, promoting agile development.

**RDBMS Approach:**

- **Relational Databases:** Follow the principles of relational algebra, where data is organized into tables with predefined relationships. Emphasis on ACID properties for transactional integrity.
- **NoSQL Approach:** Diverges from traditional RDBMS principles, often prioritizing scalability, performance, and flexibility over strict consistency.

### Challenges NoSQL Approach

1. **Consistency:** NoSQL databases often prioritize availability and partition tolerance over strict consistency, leading to eventual consistency challenges.
2. **Learning Curve:** Adapting to the diverse models of NoSQL databases can pose a learning curve for developers accustomed to traditional relational databases.
3. **Tooling and Maturity:** Some NoSQL databases may have less mature tooling compared to well-established RDBMS solutions, impacting ease of use and management.
4. **Data Integrity:** Without the rigid constraints of a predefined schema, maintaining data integrity can become a challenge as data models evolve.

### Key-Value and Document Data Models

**Key-Value Data Model:**

- **Characteristics:** Simplest NoSQL model, storing data as key-value pairs.
- **Use Cases:** Caching, session storage, and scenarios where quick retrieval based on a unique key is essential.
- **Examples:** Redis, DynamoDB.

**Document Data Model:**

- **Characteristics:** Stores data in semi-structured documents, often using formats like JSON or BSON.
- **Use Cases:** Content management, catalog systems, and applications requiring flexibility in data representation.
- **Examples:** MongoDB, CouchDB.

### Column-Family Stores

**Overview:** Column-family stores are a type of NoSQL database that organizes data into columns rather than rows, providing a flexible and scalable approach to data storage. The key characteristics include:

1. **Column-Oriented Storage:** Data is stored in columns rather than rows, allowing efficient retrieval and storage of large amounts of data with varying attributes.

2. **Schema Flexibility:** Unlike traditional relational databases, column-family stores do not enforce a fixed schema, making it easier to adapt to evolving data structures.

3. **Scalability:** Column-family stores are designed for horizontal scalability, enabling the distribution of data across multiple nodes to handle large volumes of data and high write and read throughput.

4. **Use Cases:** Well-suited for scenarios with large amounts of data and where read and write performance are critical, such as time-series data, sensor data, and analytics.

### Aggregate-Oriented Databases

**Overview:** Aggregate-oriented databases focus on grouping related data into aggregates, where an aggregate is a collection of objects treated as a single unit. Key characteristics include:

1. **Aggregation of Data:** Data is grouped into aggregates, promoting encapsulation and reducing the need for complex relationships between different entities.

2. **Consistency:** Aggregates are treated as transactional units, ensuring that changes within an aggregate are consistent and atomic.

3. **Performance:** Retrieving entire aggregates can be more efficient than navigating complex relationships in traditional relational databases.

4. **Use Cases:** Commonly used in scenarios where data naturally forms clusters or groups, such as in event sourcing architectures or systems dealing with complex domain models.

### Replication and Sharding

**Replication:**

1. **Overview:** Replication involves creating and maintaining multiple copies of the same data across different nodes or servers.
2. **Benefits:** Enhances data availability, fault tolerance, and load balancing by distributing read operations across replicas.
3. **Challenges:** Consistency must be carefully managed to ensure that changes made to one replica are accurately reflected in others.

**Sharding:**

1. **Overview:** Sharding, or horizontal partitioning, involves dividing a database into smaller, more manageable pieces called shards.
2. **Benefits:** Improves scalability by distributing data across multiple servers, allowing the database to handle larger workloads.
3. **Challenges:** Careful consideration is needed to ensure that data is evenly distributed among shards, and queries involving multiple shards may introduce complexity.

### MapReduce on Databases

**Overview:** MapReduce is a programming model and processing technique for distributed data processing. When applied to databases, it involves two main steps:

1. **Map Phase:** Data is distributed across multiple nodes, and a map function is applied to process and filter the data locally on each node.

2. **Reduce Phase:** The results from the map phase are aggregated and reduced to produce the final output.

**Benefits:**

- **Parallel Processing:** Enables parallel processing of large datasets, improving performance and scalability.
- **Distributed Computing:** Well-suited for distributed computing environments, allowing efficient processing of data across multiple nodes.

**Use Cases:** MapReduce is commonly used for large-scale data processing tasks, such as log analysis, data transformation, and batch processing in distributed systems.

### Distribution Models

**Overview:** Distribution models describe how data is distributed across nodes in a distributed database system. Common distribution models include:

1. **Horizontal Distribution:** Involves dividing the dataset into smaller subsets (shards) and distributing them across multiple nodes. Each node is responsible for a specific range of data.

2. **Vertical Distribution:** Data is distributed based on columns, where each node contains a subset of columns for the entire dataset. This can be beneficial when certain columns are accessed together frequently.

3. **Replication:** Involves creating and maintaining multiple copies (replicas) of the same data across different nodes. Replication enhances fault tolerance, availability, and load balancing.

4. **Hybrid Approaches:** Some systems combine horizontal and vertical distribution or incorporate elements of both replication and sharding to optimize performance and fault tolerance.

### Single Server

**Overview:** A single-server architecture involves running a database on a single machine, where all data and processing are handled by that one server. Key characteristics include:

1. **Simplicity:** Easy to set up and manage, making it suitable for small-scale applications or development environments.
2. **Limitations:** Limited scalability and potential performance bottlenecks as the volume of data and the number of users grow.
3. **Use Cases:** Appropriate for small websites, prototypes, or applications with low traffic and data requirements.

### Sharding

**Overview:** Sharding, or horizontal partitioning, involves splitting a large database into smaller, more manageable pieces called shards. Each shard is hosted on a separate server or node. Key characteristics include:

1. **Scalability:** Enables horizontal scaling by distributing data across multiple servers, improving performance and accommodating larger workloads.
2. **Distribution:** Data is divided based on a defined sharding key, and each shard is responsible for a specific subset of data.
3. **Complexity:** Introduces complexity in managing distributed data and handling queries that span multiple shards.
4. **Use Cases:** Ideal for large-scale applications with high data volumes, where the benefits of horizontal scaling outweigh the challenges of distribution.

### Master-Slave Replication

**Overview:** Master-Slave Replication involves replicating data from a primary server (master) to one or more secondary servers (slaves). Key characteristics include:

1. **Read Scaling:** Read operations can be distributed across multiple slave servers, enhancing overall read performance.
2. **Data Redundancy:** Provides data redundancy and fault tolerance, as slaves can take over if the master fails.
3. **Write Operations:** Write operations typically occur on the master, and the changes are replicated to the slave servers.
4. **Use Cases:** Effective for scenarios where read scalability and fault tolerance are crucial, and write operations can be managed by a single primary server.

### Peer-to-Peer Replication

**Overview:** Peer-to-Peer Replication involves multiple database servers that can both read from and write to each other. Key characteristics include:

1. **Symmetry:** All nodes in the peer-to-peer setup have equal status, allowing for both read and write operations on any node.
2. **Load Balancing:** Read and write operations can be distributed across multiple nodes, enabling better load balancing.
3. **Complexity:** Introduces challenges in maintaining consistency and conflict resolution in scenarios where conflicting writes may occur.
4. **Use Cases:** Suitable for applications where both read and write scalability are critical, and the system needs to distribute both types of operations across multiple nodes.

### Combining Sharding and Replication

**Overview:** Combining sharding and replication involves implementing both horizontal partitioning (sharding) and data redundancy (replication) to achieve a scalable and fault-tolerant architecture. Key characteristics include:

1. **Scalability:** Enables horizontal scaling through sharding while providing data redundancy and read scalability through replication.
2. **Fault Tolerance:** Improved fault tolerance as each shard can have multiple replicas, ensuring data availability even if one or more nodes fail.
3. **Complexity:** Introduces a level of complexity in managing both sharding and replication mechanisms.
4. **Use Cases:** Ideal for large-scale applications with high scalability requirements, where maintaining data integrity and availability are critical.
