# Day 4: SQL Safety Commands & Basic CRUD Operations

## 1. Database Management & Safety Commands
When working with databases, it is crucial to avoid errors when creating or deleting existing objects. SQL provides safety keywords for this.

### A. Viewing Databases and Tables
- **`SHOW DATABASES;`**: Lists all the databases present on the MySQL server.
- **`SHOW TABLES;`**: Lists all the tables present inside the currently selected database.

### B. Safe Creation and Deletion
- **`CREATE DATABASE IF NOT EXISTS db_name;`**
  - **Purpose:** Creates a new database only if it does not already exist. Prevents "Duplicate Database" errors.
  - **Example:** `CREATE DATABASE IF NOT EXISTS University;`

- **`DROP DATABASE IF EXISTS db_name;`**
  - **Purpose:** Deletes a database only if it exists. Prevents "Unknown Database" errors.
  - **Example:** `DROP DATABASE IF EXISTS University;`

---

## 2. Table Related Queries (CRUD Basics)
Once a database is selected, we create tables to store data and then manipulate that data.

### A. Creating a Table (`CREATE TABLE`)
Defines the structure (columns and data types) of the table.
```sql
CREATE TABLE Employees (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50),
    salary INT
);
### B. Inserting Data (INSERT INTO)
Adds new rows (records) into the table.
-- Method 1: Specifying column names (Recommended)
INSERT INTO Employees (emp_id, emp_name, salary) VALUES (1, 'Jamal', 50000);

-- Method 2: Without column names
INSERT INTO Employees VALUES (2, 'Ali', 60000);

### C. Retrieving Data (SELECT)
-- Select all columns and all rows
SELECT * FROM Employees;
