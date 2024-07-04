# Relational Databases (RDBMS)

## Overview

- **Examples:** MySQL, PostgreSQL, SQLite
- **Structure:** Tables with rows and columns
- **Query Language:** SQL (Structured Query Language)
- **Features:** ACID compliance (Atomicity, Consistency, Isolation, Durability)

**Pros:**

- **ACID Compliance:** Ensures reliable transactions.
- **Structured Data:** Well-defined schema with tables and relations.
- **SQL:** Powerful and widely-used query language.
- **Data Integrity:** Strong data validation and constraints.

**Cons:**

- **Scalability:** Can be challenging to scale horizontally.
- **Complexity:** Schema changes can be difficult.
- **Performance:** Might not perform well with very large datasets or complex queries.

## Basic SQL Commands

- **SELECT:** Retrieve data.
  ```sql
  SELECT * FROM users;
  ```
- **INSERT:** Add new data.
  ```sql
  INSERT INTO users (name, age) VALUES ('Alice', 30);
  ```
- **UPDATE:** Modify existing data.
  ```sql
  UPDATE users SET age = 31 WHERE name = 'Alice';
  ```
- **DELETE:** Remove data.
  ```sql
  DELETE FROM users WHERE name = 'Alice';
  ```
