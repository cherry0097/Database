# Database Management System (DBMS) 📚

## 1. Three-Tier Architecture 🏗️
```
Client [GUI, Web interface] --> Application Server or Web Server [Application programs, Web pages] --> Database Server [Database Management System]
```

## 2. View of Data 🔍
### Data Abstraction:
- **Physical Level** (Lowest Level) ⚙️
  - Deals with how data is stored.
  - Uses complex data structures.
- **Logical Level** 📊
  - Deals with what data is stored and its relationships.
  - Uses simple data structures.
- **View Level** (Highest Level) 👀
  - Defines how users access data.

## 3. Schemas 🏗️
- **What is a Schema?**
  - It is the overall design of a database.
  - It is not frequently changed.

### Three Levels of Schemas:
- **Sub-Schemas**
- **Logical Schema**
- **Physical Schema**

## 4. Types of Users 👥
- **Naive Users** - End users interacting via applications.
- **Application Programmers** - Developers creating database applications.
- **Sophisticated Users** - Analysts using advanced queries.
- **Specialized Users** - Database Administrators managing the system.

## 5. Data Models 🏛️
- **Relational Model** 📊
- **Entity-Relationship (E-R) Model** 🏗️
- **Object-based Data Model** 🛠️
- **Semi-structured Data Model** 🗄️

## 6. Database System Architecture 🏗️
### Diagram Representation:
```mermaid
graph TD;
  A[Naive Users (Tellers, Agents, Web Users)] -->|Use| B(Application Interfaces);
  C[Application Programmers] -->|Write| D(Application Programs);
  E[Sophisticated Users (Analysts)] -->|Use| F(Query Tools);
  G[Database Administrators] -->|Use| H(Administration Tools);
  B --> I[Application Program Object Code];
  D --> J[Compiler and Linker];
  F --> K[DML Queries];
  H --> L[DDL Interpreter];
  I --> M[Query Evaluation Engine];
  K --> N[DML Compiler and Organizer];
  L --> N;
  M --> O[Buffer Manager];
  M --> P[File Manager];
  N --> Q[Authorization & Integrity Manager];
  N --> M;
  Q --> R[Transaction Manager];
  P --> S[Disk Storage: Data, Indices, Statistical Data, Data Dictionary];
  O --> S;
  R --> S;
```

## 7. Data Definition Language (DDL) Commands 📜
```sql
-- Create a new table
CREATE TABLE table_name(col1 datatype, col2 datatype, ... coln datatype);

-- Add another column to the table
ALTER TABLE table_name ADD column_name datatype;

-- Remove all rows from the table but keep its structure
TRUNCATE TABLE table_name;

-- Remove the table completely
DROP TABLE table_name;

-- Rename a table
RENAME TABLE old_table_name TO new_table_name;
```

## 8. Data Manipulation Language (DML) Commands ✍️
```sql
-- Insert data into a table
INSERT INTO table_name(col1, col2, ..., coln) VALUES (val1, val2, ..., valn);

-- Update records in a table
UPDATE table_name SET col1=val1, col2=val2, ... coln=valn WHERE condition;

-- Delete specific records from a table
DELETE FROM table_name WHERE condition;

-- Retrieve specific records from a table
SELECT col1, col2, ..., coln FROM table_name WHERE condition;
```

## 9. Data Control Language (DCL) Commands 🔐
```sql
-- Grant privileges
GRANT privilege_name1, privilege_name2 ON object_name1, object_name2 TO user1, user2;
-- Example: Grant SELECT privilege to a user named Ratul
GRANT SELECT ON Student TO Ratul;

-- Revoke privileges
REVOKE privilege_name1, privilege_name2 ON object_name1, object_name2 FROM user1, user2;
```

## 10. Transaction Control Language (TCL) Commands 🔄
```sql
-- Save changes permanently
COMMIT;

-- Create a savepoint
SAVEPOINT savepoint_name;

-- Rollback to a specific savepoint
ROLLBACK TO savepoint_name;

-- Set transaction properties
SET TRANSACTION [READ WRITE || READ ONLY];
```

## 11. Aggregate Functions 🧮
```sql
-- Count total values in a column
SELECT COUNT(col1) FROM table_name;

-- Count unique values in a column
SELECT COUNT(DISTINCT col1) FROM table_name;

-- Sum of values in a column
SELECT SUM(col1) FROM table_name;

-- Average value in a column
SELECT AVG(col1) FROM table_name;

-- Minimum value in a column
SELECT MIN(col1) FROM table_name;

-- Maximum value in a column
SELECT MAX(col1) FROM table_name;
```

## 12. SQL Clauses 📌
### GROUP BY:
```sql
SELECT COUNT(colx), coly FROM table_name GROUP BY colz HAVING COUNT(cola) >= vala;
```

### ORDER BY:
```sql
SELECT col1, col2, ..., coln FROM table_name ORDER BY col1, col2, ..., coln ASC|DESC;
```

### LIKE:
```sql
-- Using % wildcard (matches any sequence of characters)
SELECT * FROM table_name WHERE col1 LIKE 'A%';

-- Using _ wildcard (matches a single character)
SELECT * FROM table_name WHERE col1 LIKE 'A_';
```

---
✨ **This document provides an overview of fundamental DBMS concepts and SQL commands in a well-structured and visually appealing manner.** ✨