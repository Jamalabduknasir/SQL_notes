# Day 6: SQL Filtering - DISTINCT & WHERE

Filtering data is one of the most crucial skills in Data Science and SQL. These two commands help us clean and extract specific information from large datasets.

## 1. The DISTINCT Keyword
- **Definition:** Used to return only **unique (different)** values. It eliminates duplicate rows from the result set.
- **When to use:** When you want to see a list of unique categories, cities, or types without repetitions.
- **Syntax:**
  ```sql
  SELECT DISTINCT column1, column2 FROM table_name;
  
