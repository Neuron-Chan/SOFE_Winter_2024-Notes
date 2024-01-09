# Software Project Management (SOFE3490)

| Category                     | Mark   |
|------------------------------|--------|
| 5 Lab Assignments            | 15%    |
| Tutorials                    | 10%    |
| In-Class Activities/Quizzes  | 10%    |
| Midterm (Feb. 26th)          | 30%    |
| Final                        | 35%    |

Office Hours: Mondays 7-8 PM, SIRC 3386


**Quizzes:**
- Lockdown browser will be used in quizzes and must be done in class. 
- Expect a quiz bi-weekly. *(Lowest quiz mark dropped)*

**Midterm:**
- The exam will be on Feb. 26th during the class time. (**yes that means it's at 8pm**)
- No midterm deferral, marks will be added to the final exam

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 1 | Introduction to SPM</summary>
  
  # Intro:

  

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;"> Section 5 | In Lecture
  </summary>

  **Like** Clause; Address Like %Houston,TX% 
  - Searching sub-string within main string

  **WHERE** Bdate **LIKE** 195_ *(All people born in the 50s)*


  Review for Select (main clause for queries)

  **SELECT** |DISTINCT| *(Only unique rows)*, by default it's |ALL|
  **FROM** Tbl-name
  **WHERE** Condition
  **GROUP BY** Group based on a given condition (Group by all Name's that start with J)
  **HAVING** condition (filter groups)

---
SELECT * FROM

SELECT Fname, Lname FROM Employee E WHERE E.FName = "";


`FROM Employee E, Employee E2 WHERE E2.Fname = "Franklin" AND E2.Lname = "Wong" AND E.super_ssn = E2.ssn;`

`FROM Course C, Section S WHERE S.Instructor = "King" AND S.year = 07 AND C.course_number = S.course_number`

</details>


</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;"> Section 5 | Final Study Important Stuff
  </summary>

**DDL** : Data Definition Language *(Essentially Schema Modification, creating and editing tables and relationships)* <br></br>
**DML** : Data Manipulation Language *(Essentially Data Modifciation, within tables for ex)*

### Scenario: Online Shopping Database | Data Definitions

Imagine an online shopping database with two tables: `Products` and `Orders`. The `Products` table contains details about products, and the `Orders` table records customer orders for these products.

1. **`Products` Table**
    ```sql
    CREATE TABLE Products (
        ProductID int PRIMARY KEY,
        ProductName varchar(255),
        Price decimal
    );
    ```

2. **`Orders` Table with Different Foreign Key Constraints**
    - **`ON DELETE NO ACTION` and `ON UPDATE NO ACTION`:**
        ```sql
        CREATE TABLE Orders (
            OrderID int PRIMARY KEY,
            ProductID int,
            OrderDate date,
            FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
            ON DELETE NO ACTION
            ON UPDATE NO ACTION
        );
        ```
        - **Deletion Scenario**: If you try to delete a row in `Products` that is referenced in `Orders`, an error occurs.
        - **Update Scenario**: If you try to update the `ProductID` in `Products` that is referenced in `Orders`, an error occurs.

    - **`ON DELETE CASCADE` and `ON UPDATE CASCADE`:**
        ```sql
        CREATE TABLE Orders (
            OrderID int PRIMARY KEY,
            ProductID int,
            OrderDate date,
            FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
            ON DELETE CASCADE
            ON UPDATE CASCADE
        );
        ```
        - **Deletion Scenario**: Deleting a product in `Products` will also delete all orders in `Orders` containing that product.
        - **Update Scenario**: Updating a `ProductID` in `Products` will update the `ProductID` in all corresponding rows in `Orders`.

    - **`ON DELETE SET NULL` and `ON UPDATE SET NULL`:**
        ```sql
        CREATE TABLE Orders (
            OrderID int PRIMARY KEY,
            ProductID int,
            OrderDate date,
            FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
            ON DELETE SET NULL
            ON UPDATE SET NULL
        );
        ```
        - **Deletion Scenario**: Deleting a product in `Products` will set the `ProductID` in `Orders` to `NULL` for all related orders.
        - **Update Scenario**: Updating a `ProductID` in `Products` sets the `ProductID` in `Orders` to `NULL` for related orders.

    - **`ON DELETE SET DEFAULT` and `ON UPDATE SET DEFAULT`:**
        ```sql
        CREATE TABLE Orders (
            OrderID int PRIMARY KEY,
            ProductID int DEFAULT 1, -- Assuming 1 is a valid default ProductID
            OrderDate date,
            FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
            ON DELETE SET DEFAULT
            ON UPDATE SET DEFAULT
        );
        ```
        - **Deletion Scenario**: Deleting a product in `Products` will set the `ProductID` in `Orders` to a default value (e.g., `1`) for all related orders.
        - **Update Scenario**: Updating a `ProductID` in `Products` will change the `ProductID` in `Orders` to a default value for related orders.

### Key Points:

- **NO ACTION**: Ensures referential integrity by preventing the deletion or updating of referenced data.
- **CASCADE**: Propagates changes (delete/update) from the parent table to the child table.
- **SET NULL**: Nullifies the foreign key in the child table when the referenced row in the parent table is deleted or updated.
- **SET DEFAULT**: Sets the foreign key to a default value when the referenced row in the parent table is deleted or updated.

These examples show how different `ON DELETE` and `ON UPDATE` clauses can be used to maintain the integrity and logical consistency of data in relational databases.

---

### Key Constraints and Referential Integrity

- Giving Names to Constraints: You can assign a name to any defined constraint (optional) BUT must be a **unique name** if given

1. **Primary Key**:
   - Single Attribute: `Dnumber INT PRIMARY KEY;`
   - Multiple Attributes: `CONSTRAINT DEPTPK PRIMARY KEY(Dnumber, ...);`

2. **Unique Key**:
   - Single Attribute: `Dname VARCHAR(15) UNIQUE;`
   - Multiple Attributes: `CONSTRAINT DEPTSK UNIQUE (Dname, ...);`

### Attribute Constraints and Defaults
1. **NOT NULL**: Indicates an attribute cannot be NULL. Automatically applied to primary key attributes.
   - Example: `EmployeeID INT NOT NULL;`

2. **DEFAULT**: Sets a default value for an attribute if none is provided.
   - Example: `StartDate DATE DEFAULT '2023-01-01';`

### CHECK Constraints
1. **Simple CHECK**: Restricts values for a single attribute.
   - Example: `Age INT CHECK (Age > 0 AND Age < 100);` – Ensures Age is between 1 and 99.

2. **Complex CHECK**: Involves multiple attributes.
   - Example: `CHECK (StartDate <= EndDate);` – Ensures StartDate is not after EndDate.

3. **Domain CHECK**: Creates a domain with a constraint. *(Custom Data Type-kinda)*
   - Example: `CREATE DOMAIN PositiveInt AS INT CHECK (VALUE > 0);` – Defines a domain for positive integers.

4. **CHECK with Range**:
   - Example: `Dnumber INT NOT NULL CHECK (Dnumber > 0 AND Dnumber < 21);` – Dnumber must be between 1 and 20.

5. **General Constraint**:
   - Example: `Salary DECIMAL CHECK (Salary >= 30000);` – Ensures Salary is at least 30,000.

These examples cover the fundamental aspects of SQL constraints, focusing on the practical application of `CHECK` constraints to ensure data integrity and validity.

### Basic DDL for table creation using Checks and ON UPDATE and or ON DELETE data DDL constraints.

![DB 5 1](../static/DB_5_1.png)
![DB 5 2](../static/DB_5_2.png)
---

# Select Queries (only non-trivial info):

Logical comparison operators are: =, <, <=, >, >=, and <>

*The focus here is on handling duplicates, set operations, string pattern matching, and ordering in SQL queries.*

### 1. Eliminating Duplicates with `DISTINCT`

- **Key Point**: SQL does not automatically eliminate duplicate tuples. Use `DISTINCT` to remove duplicates.
  
  **Example**:
  ```sql
  SELECT DISTINCT EmployeeName FROM Employees;
  ```
  This query returns unique employee names, removing any duplicates.

### 2. Set Operations: `UNION`, `EXCEPT`, `INTERSECT`

- **Key Point**: These operations automatically eliminate duplicate tuples.
  
  **Example**:
  - **`UNION`**: Combines results from two queries without duplicates.
    ```sql
    SELECT EmployeeName FROM Sales
    UNION
    SELECT EmployeeName FROM Marketing;
    ```
    This query lists all unique employee names from both Sales and Marketing departments.

  - **`EXCEPT`**: Returns tuples from the first query that are not in the second query.
    ```sql
    SELECT EmployeeName FROM Employees
    EXCEPT
    SELECT EmployeeName FROM Managers;
    ```
    This query shows employees who are not managers.

  - **`INTERSECT`**: Returns only the common tuples from both queries.
    ```sql
    SELECT EmployeeName FROM FullTime
    INTERSECT
    SELECT EmployeeName FROM BenefitsEligible;
    ```
    This finds employees who are both full-time and eligible for benefits.

### 3. Multiset Operations: `UNION ALL`, `EXCEPT ALL`, `INTERSECT ALL`

- **Key Point**: These operations do not eliminate duplicates.
  
  **Example**:
  - **`UNION ALL`**: Combines all results, including duplicates.
    ```sql
    SELECT EmployeeID FROM Sales
    UNION ALL
    SELECT EmployeeID FROM Marketing;
    ```
    This query lists all employee IDs from both departments, including duplicates.

  - **`EXCEPT ALL`**: Returns tuples from the first query minus those in the second, keeping duplicates.
    ```sql
    SELECT Product FROM Orders
    EXCEPT ALL
    SELECT Product FROM CancelledOrders;
    ```
    This shows products ordered but not cancelled, including duplicate orders.

  - **`INTERSECT ALL`**: Returns all common tuples including duplicates.
    ```sql
    SELECT CustomerID FROM OnlineOrders
    INTERSECT ALL
    SELECT CustomerID FROM InStorePurchases;
    ```
    This lists customers who made both online and in-store purchases, including multiple purchases.

---

## The difference between a "Set" and a "Multiset" (also known as a "Bag") is fundamentally in how they handle duplicate elements:

### Set
1. **Uniqueness**: A set is a collection of distinct, unique elements. In a set, each element can appear only once. 
2. **SQL Context**: When applying set operations in SQL (like `UNION`, `INTERSECT`, and `EXCEPT`), duplicates are automatically eliminated in the resulting set. For example, if the same element appears in both sets being united, it will appear only once in the union set.

   **Example**:
   ```sql
   SELECT Column FROM Table1
   UNION
   SELECT Column FROM Table2;
   ```
   This SQL query combines unique values from both `Table1` and `Table2`.

### Multiset (Bag)
1. **Duplicates Allowed**: A multiset, unlike a set, can contain duplicate elements. The same element can appear multiple times in a multiset.
2. **SQL Context**: In SQL, multiset operations (like `UNION ALL`, `INTERSECT ALL`, and `EXCEPT ALL`) retain duplicates. These operations are more like aggregating the results of two queries, including their duplicates.

   **Example**:
   ```sql
   SELECT Column FROM Table1
   UNION ALL
   SELECT Column FROM Table2;
   ```
   This SQL query combines all values from both `Table1` and `Table2`, keeping duplicates.

### Key Differences
- **Uniqueness**: Sets do not allow duplicates, while multisets do.
- **SQL Operations**: Set operations in SQL (`UNION`, `INTERSECT`, `EXCEPT`) remove duplicates, whereas their `ALL` variants (`UNION ALL`, `INTERSECT ALL`, `EXCEPT ALL`) keep duplicates.

Understanding this distinction is particularly important in database operations and when working with data structures in programming, where the choice between a set and a multiset can affect performance and results.

---

### 4. String Pattern Matching with `LIKE`

- **Key Point**: `%` matches any sequence of characters, `_` matches a single character.
  
  **Example**:
  - `"Smith%"` matches any string starting with 'Smith'.
  - `"Sm_th"` matches 'Smith', 'Smoth', etc.
  - `'%Smith'` matches any string ending with 'Smith'.

  ```sql
  SELECT * FROM Employees WHERE Name LIKE 'Sm%th';
  ```
  This query finds employees whose names start with 'Sm' and end with 'th'.

### 5. Ordering Results with `ORDER BY`

- **Key Point**: `ORDER BY` sorts query results. `ASC` for ascending (default), `DESC` for descending.
  
  **Example**:
  ```sql
  SELECT EmployeeName, Department FROM Employees
  ORDER BY Department ASC, EmployeeName DESC;
  ```
  This orders employees by department in ascending order **and then** by name in descending order within each department.
*(Sequential)*

![DB 5 2](../static/DB_5_3.png)

---
### INSERT, DELETE, UPDATE with concise examples:

### 1. The `INSERT` Command
Used to add tuples (rows) to a table.

#### Types of `INSERT` Statements:
1. **INSERT With Column List**:
   - **Syntax**: `INSERT INTO table_name (column_list) VALUES (value_list);`
   - **Example**:
     ```sql
     INSERT INTO Employees (ID, Name, Age) VALUES (1, 'John Doe', 30);
     ```
     Here, values for ID, Name, and Age are inserted into the Employees table.

2. **INSERT Without Column List**:
   - Assumes values for all columns.
   - **Example**:
     ```sql
     INSERT INTO Employees VALUES (2, 'Jane Doe', 25);
     ```
     It inserts values assuming the order of columns in the table schema.

3. **INSERT with SELECT Statement**:
   - Useful for inserting data from other tables.
   - **Example**:
     ```sql
     INSERT INTO Managers (ID, Name) SELECT EmployeeID, Name FROM Employees WHERE Position = 'Manager';
     ```
     This inserts data into the Managers table from the Employees table where the position is 'Manager'.

#### Integrity Constraints in `INSERT`:
- Ensures the consistency of the data. For example, an `INSERT` operation can fail if it violates a primary key or foreign key constraint.

### 2. The `DELETE` Command
Used to remove tuples from a table.

- **Syntax**: `DELETE FROM table_name [WHERE search_condition];`
- **Example**:
  ```sql
  DELETE FROM Employees WHERE Age < 25;
  ```
  This deletes all employees younger than 25 years from the Employees table.
- **Without WHERE Clause**: Deletes all rows in the table.
  
### 3. The `UPDATE` Command
Used to modify attribute values of one or more tuples.

- **Syntax**: `UPDATE table_name SET column1 = value1 [, column2 = value2...] [WHERE search_condition];`
- **Example 1**: Increase salary by 10% for all employees.
  ```sql
  UPDATE Employees SET Salary = Salary * 1.10;
  ```
- **Example 2**: Update location and department number for a specific project.
  ```sql
  UPDATE Projects SET Location = 'Bellaire', DeptNumber = 5 WHERE ProjectID = 10;
  ```
- **With WHERE Clause**: Updates only those rows that satisfy the condition.

### Key Points:
- **INSERT**: Adds new data. Must match column list and data types.
- **DELETE**: Removes data. Can target specific rows or clear a table.
- **UPDATE**: Modifies existing data. Can update specific rows or all rows in a table.
- **Integrity Constraints**: Important for maintaining data consistency and are enforced during these operations.
- **Column Order and Data Types**: Must be respected especially in `INSERT` operations.

These examples illustrate the basic usage of `INSERT`, `DELETE`, and `UPDATE` commands in SQL, showing how they interact with table data and integrity constraints.

</details>
