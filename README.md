## 🎨 Database System Overview

## 🧱 1. Three-Tier Architecture

```mermaid
graph LR
  A[👨‍💻 Client <br> (GUI/Web Interface)] --> B[🌐 Application/Web Server <br> (App Programs/Web Pages)]
  B --> C[🗄️ Database Server <br> (DBMS)]

---

## 🧩 2. View of Data (Abstraction Levels)

| Level        | Description                                | Complexity        |
|--------------|--------------------------------------------|-------------------|
| 🔧 **Physical** | How data is stored, uses complex structures | 🔽 Lowest          |
| 📊 **Logical**  | What data is stored and relationships      | ⚖️ Medium          |
| 👀 **View**     | User-level access and representation       | 🔼 Highest         |

---

## 🧬 3. Schemas

📌 A schema is like a **variable declaration** for your database — the **overall design**. It's stable and rarely changed.

### Types of Schemas:

- 🔹 **Sub-Schemas** — User-specific views
- 🔸 **Logical Schema** — Logical structure of entire database
- ⚙️ **Physical Schema** — Actual physical storage structure

---

## 👥 4. Types of Users

| User Type             | Role/Description                        |
|-----------------------|-----------------------------------------|
| 🙋 **Naive Users**        | End users (e.g. bank tellers)             |
| 💻 **Application Programmers** | Build and maintain application software |
| 🧠 **Sophisticated Users**   | Analysts, write complex queries         |
| 🛠️ **Specialized Users**     | DBAs and engineers managing systems     |

---

## 🧾 5. Data Models

- 📘 **Relational Model**
- 📙 **Entity-Relationship (ER) Model**
- 📗 **Object-Based Model**
- 📕 **Semi-Structured Model** (e.g., XML, JSON)

---

## 🏗️ 6. Database System Architecture

### 👥 Users Interaction

```mermaid
flowchart TB
  Naive[🙋 Naive Users] -->|Use| UI[🖥️ Application Interface]
  Programmer[💻 App Programmers] -->|Write| Code[📦 Application Code]
  Analyst[🧠 Analysts] -->|Use| Tools[🔍 Query Tools]
  Admin[🛠️ Admins] -->|Use| AdminTools[🧰 Admin Tools]
```

### 🔧 System Components

```mermaid
graph TD
  AppCode[📦 Application Program Object Code] --> Engine[⚙️ Query Evaluation Engine]
  Engine --> Manager[🗃️ Storage Manager]
  Manager --> Compiler[🛠️ DML Compiler & Organizer]
```

### 🧠 Query Processor

- **Query Eval Engine**
- **DML Compiler**
- **Stats Collector**

### 📦 Storage Manager

- 🧮 Buffer Manager  
- 📂 File Manager  
- 🔄 Transaction Manager  
- 🔐 Auth & Integrity Manager

### 💾 Disk Storage

- 📑 Data  
- 🗂️ Indices  
- 📊 Statistical Data  
- 📘 Data Dictionary (Metadata)

---

## 🧱 7. Data Definition Language (DDL)

```sql
CREATE TABLE table_name(col1 datatype, col2 datatype, ...);
ALTER TABLE table_name ADD column_name datatype;
TRUNCATE TABLE table_name;
DROP TABLE table_name;
RENAME TABLE old_table TO new_table;
```

---

## ✍️ 8. Data Manipulation Language (DML)

```sql
INSERT INTO table_name(col1, col2) VALUES (val1, val2);
UPDATE table_name SET col1 = val1 WHERE condition;
DELETE FROM table_name WHERE condition;
SELECT col1, col2 FROM table_name WHERE condition;
```

---

## 🛡️ 9. Data Control Language (DCL)

```sql
GRANT SELECT ON Student TO Ratul;
REVOKE SELECT ON Student FROM Ratul;
```

---

## 🔄 10. Transaction Control Language (TCL)

```sql
COMMIT;
SAVEPOINT my_savepoint;
ROLLBACK TO my_savepoint;
SET TRANSACTION READ WRITE;
```

---

## 📊 Aggregate Functions

```sql
SELECT COUNT(col1) FROM table_name;
SELECT COUNT(DISTINCT col1) FROM table_name;
SELECT SUM(col1) FROM table_name;
SELECT AVG(col1) FROM table_name;
SELECT MIN(col1) FROM table_name;
SELECT MAX(col1) FROM table_name;
```

---

## 📚 GROUP BY and HAVING

```sql
SELECT COUNT(colx), coly
FROM table_name
GROUP BY colz
HAVING COUNT(cola) >= vala;
```

---

## 🔃 ORDER BY

```sql
SELECT col1, col2
FROM table_name
ORDER BY col1 DESC;
```

---

## 🔍 LIKE Clause

```sql
LIKE '_%'  -- _ = single char, % = any sequence
-- Example
SELECT * FROM users WHERE name LIKE '_ohn%';
```

---

> 📌 **Tip:** Use markdown preview in VS Code or GitHub for best visuals. For diagrams, you can use Mermaid.js or plantUML-enabled viewers.

---

Would you like me to export 