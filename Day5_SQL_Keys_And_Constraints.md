# Day 5: SQL Keys & Constraints (Relational Database Basics)

## 1. Primary Key vs. Foreign Key
These keys are essential for creating relationships between different tables in a Relational Database.

### A. Primary Key (PK)
- **Definition:** A column (or set of columns) that **uniquely identifies** each record in a table.
- **Rules:** It cannot contain `NULL` values, and no two rows can have the same Primary Key.
- **Real-world Example:** `Roll_Number` in a Student table, or `CNIC` in a Citizens table.

### B. Foreign Key (FK)
- **Definition:** A column in one table that refers to the **Primary Key** of another table. It creates a link (relationship) between the two tables.
- **Purpose:** Ensures "Referential Integrity" (prevents invalid data from being inserted that doesn't exist in the linked table).
- **Real-world Example:** `Department_ID` in the `Students` table, which links to the `Department_ID` (Primary Key) in the `Departments` table.

---

## 2. SQL Constraints (Rules for Data)
Constraints are rules applied to table columns to restrict the type of data that can go into a table.

### 1. NOT NULL
- **Rule:** Ensures that a column cannot have a `NULL` (empty) value. A value must always be provided.
- **Example:** A user's `Name` or `Password` should never be empty.

### 2. UNIQUE
- **Rule:** Ensures that all values in a column are **different**. No duplicates are allowed.
- **Example:** `Email_Address` or `Phone_Number` (Two users cannot have the same email).

### 3. PRIMARY KEY
- **Rule:** A combination of `NOT NULL` and `UNIQUE`. It uniquely identifies each row in a table.
- **Note:** A table can have only ONE Primary Key.

### 4. FOREIGN KEY
- **Rule:** Prevents actions that would destroy links between tables. It ensures that the value in this column must exist in the referenced table's Primary Key.

### 5. DEFAULT
- **Rule:** Sets a **default value** for a column if no value is specified during an `INSERT` operation.
- **Example:** If a `Country` column has a `DEFAULT 'Pakistan'`, and a user doesn't provide a country, it will automatically save 'Pakistan'.

---

### 💡 Syntax Example:
```sql
CREATE TABLE Students (
    Roll_No INT PRIMARY KEY,          -- Primary Key Constraint
    Name VARCHAR(50) NOT NULL,        -- Not Null Constraint
    Email VARCHAR(100) UNIQUE,        -- Unique Constraint
    Dept_ID INT,                      -- This will be our Foreign Key
    Country VARCHAR(50) DEFAULT 'Pakistan', -- Default Constraint
    FOREIGN KEY (Dept_ID) REFERENCES Departments(Dept_ID) -- Foreign Key Constraint
);
