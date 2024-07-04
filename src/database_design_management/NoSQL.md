# NoSQL Databases

## Overview

- **Examples:** MongoDB, Redis, Cassandra
- **Types:**
  - Document (e.g., MongoDB)
  - Key-Value (e.g., Redis)
  - Column-Family (e.g., Cassandra)
  - Graph (e.g., Neo4j)
- **Features:** Flexible schemas, scalability

**Pros:**

- **Scalability:** Easily scales horizontally.
- **Flexibility:** Schemaless design allows for rapid changes.
- **Performance:** Optimized for specific use cases (e.g., high read/write throughput).
- **Variety:** Different types for different needs (Document, Key-Value, Column-Family, Graph).

**Cons:**

- **Consistency:** Might sacrifice consistency for availability (CAP Theorem).
- **ACID Compliance:** Not all NoSQL databases fully support ACID transactions.
- **Complexity:** Learning curve can be steep due to different paradigms and lack of standardization.

## MongoDB Example

- **Insert Document:**
  ```javascript
  db.users.insertOne({ name: "Alice", age: 30 });
  ```
- **Find Document:**
  ```javascript
  db.users.find({ name: "Alice" });
  ```
- **Update Document:**
  ```javascript
  db.users.updateOne({ name: "Alice" }, { $set: { age: 31 } });
  ```
- **Delete Document:**
  ```javascript
  db.users.deleteOne({ name: "Alice" });
  ```
