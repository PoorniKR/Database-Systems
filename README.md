# Database-Systems

# Database CRUD Operations in SQL

This project demonstrates basic SQL CRUD (Create, Read, Update, Delete) operations on a database. These are the fundamental operations for interacting with databases.

## Prerequisites

Ensure you have the following installed:

- **SQL Database** (MySQL, PostgreSQL, Oracle)

## SQL CRUD Operations

### 1. Create Table - Defining the Database Schema

Before performing any CRUD operations, a table must be created using the `CREATE TABLE` statement.

```sql
CREATE TABLE table_name (
    column1 datatype constraints,
    column2 datatype constraints,
    column3 datatype constraints,
    ...
);
```

**Example:**

```sql
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Department VARCHAR(100),
    HireDate DATE
);
```

### 2. Create - Inserting Data into a Table

The `INSERT INTO` statement is used to insert new records into a table.

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

**Example:**

```sql
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department, HireDate)
VALUES (1, 'John', 'Doe', 'Engineering', '2024-01-15');
```

### 3. Read - Querying Data from a Table

The `SELECT` statement is used to read or retrieve data from a table.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

**Example:**

```sql
SELECT * FROM Employees
WHERE Department = 'Engineering';
```

### 4. Update - Modifying Data in a Table

The `UPDATE` statement is used to modify existing records in a table.

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

**Example:**

```sql
UPDATE Employees
SET Department = 'Marketing'
WHERE EmployeeID = 1;
```

### 5. Delete - Removing Data from a Table

The `DELETE` statement is used to delete records from a table.

```sql
DELETE FROM table_name
WHERE condition;
```

**Example:**

```sql
DELETE FROM Employees
WHERE EmployeeID = 1;
```

## Notes

- **Ensure you have the correct conditions** in your `WHERE` clause when running `UPDATE` or `DELETE` statements to avoid accidental data loss.
- Use `SELECT *` only when you need all columns; otherwise, specify the required columns for efficiency.

