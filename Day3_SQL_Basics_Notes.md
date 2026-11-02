# Day 3: SQL Data Types & Command Categories

## 1. Numeric Data Types: Signed vs. Unsigned
In SQL, numeric types (like INT, TINYINT, BIGINT) can be configured to handle negative numbers or not.

### A. SIGNED (Default)
- **Definition:** Can store both **positive (+)** and **negative (-)** numbers.
- **Range Example (TINYINT):** -128 to 127.
- **Real-world Use Case:** Temperature readings, Bank account balances (can be overdrawn), Profit/Loss.

### B. UNSIGNED
- **Definition:** Can store **only positive (+)** numbers and zero. No negative values allowed.
- **Advantage:** It doubles the maximum positive capacity of the data type.
- **Range Example (UNSIGNED TINYINT):** 0 to 255.
- **Real-world Use Case:** Age, Population, ID numbers, Phone numbers (things that can never be negative).
- **Syntax Example:** 
  ```sql
  CREATE TABLE Users (
      user_id INT UNSIGNED PRIMARY KEY,
      age TINYINT UNSIGNED
  );
