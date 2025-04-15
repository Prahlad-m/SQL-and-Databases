# SQL-and-Databases

# 🗃️ Data Technician Workbook – Week 3: Databases & SQL

This is my Week 3 submission for the **Data Technician course**, focusing on the fundamentals of **databases and SQL**. This workbook includes theoretical knowledge, practical SQL exercises using a sample world database, and a written task about designing a retail database.

---

## 🧠 Day 1 – Database Concepts

### Task 1: Keys & Relationships

- **Primary Key**: Uniquely identifies each row in a table.
- **Secondary Key**: Also uniquely identifies rows but isn’t the primary identifier.
- **Foreign Key**: Connects one table to another using the primary key from the referenced table.

**Examples of Relationships:**
- One-to-One: Each person ↔ National Insurance Number
- One-to-Many: One mother ↔ Many children
- Many-to-Many: Students ↔ Classes

### Task 2: Relational vs Non-Relational Databases

- **Relational**: Structured, schema-based (e.g., SQL databases)
- **Non-relational**: Schema-less, flexible for data like images, video, real-time feeds (e.g., NoSQL)

---

## 🔄 Day 3 – SQL JOIN Types

Studied various JOIN types with explanations and real-world applications:

| Join Type     | Description |
|---------------|-------------|
| **INNER JOIN** | Returns matching rows between tables |
| **LEFT JOIN**  | All rows from left, matched rows from right |
| **RIGHT JOIN** | All rows from right, matched rows from left |
| **FULL JOIN**  | All rows from both tables |
| **CROSS JOIN** | Cartesian product of both tables |
| **SELF JOIN**  | Table joined to itself for comparison |

---

## 💻 Day 4 – SQL Practical Tasks

Worked on SQL queries using the `world_db` dataset.

### 🧾 Sample Tasks and Queries

- **Cities in USA**
  ```sql
  SELECT COUNT(name) FROM city WHERE CountryCode = 'USA';

- **Cities in USA**
  ```sql
  SELECT COUNT(name) FROM city WHERE CountryCode = 'USA';


