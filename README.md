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

- **Country with the highest Life Expectancy**
  ```sql
  SELECT Name, LifeExpectancy FROM country ORDER BY LifeExpectancy DESC LIMIT 5;

- **Cities Named Starting with "New"**
  ```sql
  SELECT * FROM city WHERE LEFT(name, 3) = 'New';

- **Cities Between 500k - 1M Population**
  ```sql
  SELECT * FROM city WHERE Population BETWEEN 500000 AND 1000000;

- **Capital of Spain**
  ```sql
  SELECT city.name AS Capital, country.name AS Country
  FROM city
  JOIN country ON city.ID = country.capital
  WHERE country.name = 'Spain';

- **Cities with High GDP per Capita**
  ```sql
  SELECT Name, Continent, GNP
  FROM country
  WHERE GNP > (SELECT AVG(GNP) FROM country)
  ORDER BY GNP DESC;

### 📝 Day 4 – Task 2: Retail Business Database Design

**Scenario**: A small corner shop wants a new database system to manage inventory, customer data, sales, and a loyalty program.

#### 📌 Step-by-Step Summary

1. **Understanding the Business Requirements**
   - The database needs to store product data, stock levels, pricing, customer information, purchase history, and loyalty status.
   - Users of the system will be the shop owner and staff.
   - Their goals include tracking sales, managing stock, and analysing customer behaviour.

2. **Designing the Database Schema**
   - Key tables may include:
     - `Products` – details like name, price, stock quantity, and category.
     - `Categories` – classification of product types.
     - `Customers` – personal and contact information, loyalty membership.
     - `Sales` – records of each transaction.
     - `SaleDetails` – line items in each sale, including quantity and products sold.
   - Relationships:
     - A customer can have many sales.
     - Each sale can include multiple products.
     - Each product belongs to a category.

3. **Implementing the Database**
   - Plan out the structure of each table and define relationships between them.
   - Make sure to apply primary and foreign keys to link related data.

4. **Populating the Database**
   - Start with sample data entries for products, categories, and customers.
   - Record sample transactions and sales details.

5. **Maintaining the Database**
   - Input sales data regularly and generate weekly reports to monitor performance.
   - Ensure data is backed up consistently.
   - Consider measures for data validation, accuracy, and security.

> ✅ This database system will help streamline store operations, ensure accurate inventory management, and improve customer engagement through loyalty tracking.
  


