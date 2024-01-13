# Unit 5

- [Unit 5](#unit-5)
    - [NoSQL Key/Value Databases using Riak](#nosql-keyvalue-databases-using-riak)
      - [Riak](#riak)
    - [Key-Value Databases](#key-value-databases)
      - [What Is a Key-Value Store?](#what-is-a-key-value-store)
    - [Key-Value Store Features](#key-value-store-features)
    - [Consistency, Transactions, Query Features](#consistency-transactions-query-features)
    - [Structure of Data](#structure-of-data)
    - [Scaling](#scaling)
    - [Suitable Use Cases](#suitable-use-cases)
    - [Considerations for User Profiles and Preferences](#considerations-for-user-profiles-and-preferences)
    - [Shopping Cart Data](#shopping-cart-data)
    - [When Not to Use](#when-not-to-use)
    - [Multi-operation Transactions](#multi-operation-transactions)
    - [Query by Data](#query-by-data)
    - [Operations by Sets](#operations-by-sets)

### NoSQL Key/Value Databases using Riak

#### Riak

**Overview:**

- Riak is an open-source distributed NoSQL key/value database designed for high availability, fault tolerance, and scalability.
- It is part of the Riak TS (Time Series) family, which is suitable for time-series data.

**Key-Value Storage:**

- Riak stores data as key/value pairs, where each key is unique, and the associated value can be a simple scalar, a complex data structure, or even binary data.

**Distributed and Fault-Tolerant:**

- Riak employs a decentralized architecture, distributing data across multiple nodes, ensuring fault tolerance and high availability.
- It uses a consistent hashing algorithm for distributing data among nodes.

**Concurrency and Availability:**

- Riak supports high concurrency and availability, making it suitable for applications with demanding read and write requirements.

### Key-Value Databases

#### What Is a Key-Value Store?

**Overview:**

- A key-value store is a NoSQL database that stores data as a collection of key-value pairs.
- Each key is unique and associated with a corresponding value, creating a simple yet powerful data model.

**Key Characteristics:**

1. **Simplicity:** Key-value stores have a straightforward data model, making them easy to understand and use.
2. **High Performance:** Direct access to data through keys results in fast read and write operations.
3. **Scalability:** Key-value databases are designed to scale horizontally, distributing data across multiple nodes.

### Key-Value Store Features

**Common Features of Key-Value Stores:**

1. **Schema-less:** Key-value stores are schema-less, allowing flexibility in the data model without a predefined schema.
2. **High Write Throughput:** Optimized for high write throughput, making them suitable for applications with frequent inserts and updates.
3. **Partitioning:** Data is partitioned across nodes, enabling horizontal scaling to handle large datasets.
4. **No Complex Queries:** Key-value stores typically do not support complex queries or secondary indexes and are best suited for simple read and write operations.

### Consistency, Transactions, Query Features

**Consistency:**

- Key-value stores vary in their consistency models. Some provide strong consistency, ensuring that all nodes see the same data simultaneously, while others prioritize eventual consistency.
- Riak offers tunable consistency levels, allowing users to choose between strong consistency, eventual consistency, or something in between based on application requirements.

**Transactions:**

- Traditional key-value stores, including Riak, may not provide support for multi-statement transactions with ACID properties.
- Riak focuses on providing high availability and fault tolerance, and transactional support is often handled at the application level.

**Query Features:**

- Key-value stores are designed for simple read and write operations based on keys.
- Riak allows querying by key, but querying capabilities are limited compared to databases with more expressive query languages.
- Secondary indexes or querying by attributes within values may be less efficient or may not be supported in some key-value stores.

### Structure of Data

**Key-Value Data Model:**

- In a key-value data model, data is organized as pairs of keys and corresponding values.
- Each key is unique, and the associated value can be a simple scalar, a complex data structure, or binary data.
- The simplicity of the model makes it suitable for storing and retrieving data efficiently.

### Scaling

**Scaling in Key-Value Stores:**

- Key-value stores are designed for horizontal scaling, allowing them to handle increased data volumes and traffic by distributing data across multiple nodes.
- Scaling is achieved through mechanisms such as sharding, where data is partitioned and distributed across nodes, and adding new nodes to the cluster.

### Suitable Use Cases

**Storing Session Information:**

- **Data Structure:** Key-value stores are well-suited for storing session information, where each user's session can be represented by a unique key, and the associated value contains session-related data.
- **Scalability:** The ability to scale horizontally allows key-value stores to handle a large number of concurrent user sessions efficiently.

**User Profiles, Preferences:**

- **Data Structure:** Key-value stores can efficiently store and retrieve user profiles and preferences. Each user profile can be represented by a unique key, and the associated value contains user-specific information and preferences.
- **Flexibility:** The flexibility of the key-value model accommodates changes and additions to user profile attributes without requiring a predefined schema.
- **Scalability:** Horizontal scaling supports the storage and retrieval of user profiles in large-scale applications with a growing user base.

### Considerations for User Profiles and Preferences

1. **Schema Flexibility:** Key-value stores offer schema-less flexibility, allowing for dynamic changes and additions to user profile attributes without requiring a predefined schema.

2. **Efficient Retrieval:** Retrieving user profiles and preferences based on keys is efficient in key-value stores, making them suitable for scenarios where fast access to user-specific data is essential.

3. **Horizontal Scaling:** Key-value stores can horizontally scale to handle increased numbers of user profiles and preferences, ensuring scalability as the user base grows.

4. **High Write Throughput:** Key-value stores are optimized for high write throughput, making them suitable for applications where user profiles are frequently updated or modified.

5. **Partitioning:** The ability to partition and distribute data across multiple nodes ensures efficient storage and retrieval of user profiles in a distributed environment.

### Shopping Cart Data

**Structure in a Key-Value Store:**

- Shopping cart data in a key-value store can be represented with a unique key for each user's cart and the associated value containing the items in the cart.
- Each item can be further represented as a key-value pair within the cart, allowing for efficient retrieval and updates.

**Example in Riak:**

```{
  "user123_cart": {
    "item1": { "name": "Product A", "quantity": 2, "price": 29.99 },
    "item2": { "name": "Product B", "quantity": 1, "price": 49.99 }
    // ...
  }
}
```

### When Not to Use

**Complex Transactions Spanning Different Operations:**

- Key-value stores, including Riak, may not be the best choice for scenarios requiring complex transactions that span multiple operations and need strict ACID properties.
- If the shopping cart operations involve intricate dependencies or transactions across multiple documents or collections, a traditional relational database might be more suitable.

**Relationships Among Data:**

- If the shopping cart data has complex relationships with other entities (e.g., products, users, orders) and requires extensive joins or relational queries, a key-value store might not be the optimal choice.
- Graph databases or relational databases with well-defined relationships may be more appropriate in such cases.

### Multi-operation Transactions

**Considerations for Multi-operation Transactions:**

- Key-value stores, like Riak, may not provide built-in support for multi-operation transactions with ACID properties.
- If maintaining strict consistency and transactional integrity is critical for shopping cart operations, a database with native support for multi-operation transactions (e.g., relational databases) may be preferable.

### Query by Data

**Querying Shopping Cart Data:**

- Key-value stores are optimized for efficient retrieval based on keys.
- Riak allows querying by key, making it suitable for retrieving and updating shopping cart data based on the user's unique identifier.

### Operations by Sets

**Considerations for Operations by Sets:**

- Key-value stores may not inherently support operations across sets of data.
- If shopping cart operations involve set-based operations (e.g., applying discounts to multiple items, updating quantities across multiple carts), a database with more advanced querying capabilities or support for set-based operations may be necessary.

**Example of Operations by Sets in SQL:**

```
UPDATE shopping_cart
SET quantity = quantity * 0.9
WHERE user_id = 'user123' AND product_id IN ('item1', 'item2');
```
