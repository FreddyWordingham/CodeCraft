Absolutely, here's a primer on database normalisation:

### Database Normalisation Overview

Database normalisation is the process of organising a database to reduce redundancy and improve data integrity.
This is achieved by dividing large tables into smaller, related tables and defining relationships between them.
The main goals are to minimise duplicate data, ensure logical data storage, and make the database easier to maintain.

### Normal Forms

Normalisation involves applying a series of rules, called normal forms (NF), to the database schema.
Each normal form addresses a specific type of redundancy or anomaly.

#### 1. First Normal Form (1NF)

- **Definition:** A table is in 1NF if all columns contain atomic (indivisible) values, and each column contains values of a single type.
- **Requirements:**
  - Each column contains only one value.
  - Each column contains values of a single type.
  - Each row is unique.

**Example:**
| ID | Name | Phone Numbers |
|----|-----------|-------------------|
| 1 | Alice | 123-4567, 234-5678|
| 2 | Bob | 345-6789 |

_In 1NF:_
| ID | Name | Phone Number |
|----|-------|--------------|
| 1 | Alice | 123-4567 |
| 1 | Alice | 234-5678 |
| 2 | Bob | 345-6789 |

#### 2. Second Normal Form (2NF)

- **Definition:** A table is in 2NF if it is in 1NF and all non-key attributes are fully functionally dependent on the primary key.
- **Requirements:**
  - Must be in 1NF.
  - All non-key columns are fully dependent on the primary key (no partial dependency).

**Example:**
| OrderID | ProductID | ProductName | Quantity |
|---------|-----------|-------------|----------|
| 1 | 101 | Apple | 10 |
| 2 | 102 | Banana | 20 |

_In 2NF:_
| OrderID | ProductID | Quantity |
|---------|-----------|----------|
| 1 | 101 | 10 |
| 2 | 102 | 20 |

| ProductID | ProductName |
| --------- | ----------- |
| 101       | Apple       |
| 102       | Banana      |

#### 3. Third Normal Form (3NF)

- **Definition:** A table is in 3NF if it is in 2NF and all attributes are only dependent on the primary key.
- **Requirements:**
  - Must be in 2NF.
  - No transitive dependency (non-key column depends on another non-key column).

**Example:**
| EmployeeID | DepartmentID | DepartmentName |
|------------|--------------|----------------|
| 1 | 10 | HR |
| 2 | 20 | Sales |

_In 3NF:_
| EmployeeID | DepartmentID |
|------------|--------------|
| 1 | 10 |
| 2 | 20 |

| DepartmentID | DepartmentName |
| ------------ | -------------- |
| 10           | HR             |
| 20           | Sales          |

#### Higher Normal Forms

- **Boyce-Codd Normal Form (BCNF):** A stronger version of 3NF where every determinant must be a candidate key.
- **Fourth Normal Form (4NF):** No multi-valued dependencies.
- **Fifth Normal Form (5NF):** No join dependencies.

### Advantages of Normalisation

- **Reduces Data Redundancy:** Minimises duplicate data.
- **Improves Data Integrity:** Ensures that data dependencies make sense.
- **Enhances Query Performance:** Smaller tables with fewer columns can be queried more efficiently.
- **Easier Maintenance:** Updates, deletions, and insertions are simplified and less error-prone.

### Disadvantages of Normalisation

- **Complex Queries:** Sometimes require complex joins to retrieve related data.
- **Performance Overhead:** Joins can be computationally expensive, especially in large datasets.
- **Initial Design Complexity:** Requires careful planning and understanding of data relationships.
