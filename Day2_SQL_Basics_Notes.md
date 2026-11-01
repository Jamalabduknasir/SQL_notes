# 📅 Day 2: SQL Basics & Database Commands

## 1. CREATE DATABASE
- **Definition:** A command used to create a new database (a container to store data).
- **Analogy:** Like building a new physical building or creating a new main folder on your computer.
- **Syntax:** 
  ```sql
  CREATE DATABASE database_name;
## 2. USE
**Definition:** A command used to select a specific database to work with. All subsequent queries will run inside this database.
**Analogy:** Like entering the building you just built to start working inside it.
**Syntax:**
USE database_name;
## 3. CREATE TABLE
**Definition:** A command used to create a new table inside the selected database. A table consists of rows and columns.
**Analogy:** Like creating a specific room or a register inside the building to store specific data.
**Syntax:**
  ```sql
CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
**Common Data Types:**
INT: For whole numbers (e.g., 1, 20, 2023).
VARCHAR(size): For text/strings (e.g., 'Jamal', 'Lahore').
PRIMARY KEY: A unique identifier for each record (no duplicates allowed).
## 4. DROP DATABASE
**Definition:** A command used to completely delete an existing database and all the data inside it.
**⚠️ Warning:** This action is permanent and cannot be undone. Use with extreme caution in real-world scenarios.
  ```sql
DROP DATABASE database_name;

