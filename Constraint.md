1. Primary Key Constraint:

- Details: A primary key constraint ensures that a column or a combination of columns uniquely identifies each row in a table.
- Example:

```sql
 CREATE TABLE Employees (
  EmployeeID INT PRIMARY KEY,
  FirstName VARCHAR(50),
  LastName VARCHAR(50)
);
```

- In this example, the EmployeeID column is designated as the primary key, ensuring that each employee has a unique identifier.

2.  Foreign Key Constraint:

- Details: A foreign key constraint establishes a relationship between two tables by referencing the primary key of another table.
- Example:

```sql
  CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    OrderDate DATE,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
  );
```

- In this example, the CustomerID column in the "Orders" table is a foreign key that references the primary key of the "Customers" table, linking each order to a specific customer.

3. Unique Constraint:

- Details: A unique constraint ensures that the values in a column or a set of columns are unique within a table.
- Example:

```sql
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    Email VARCHAR(100) UNIQUE,
    ...
);
```

- In this example, the Email column has a unique constraint, ensuring that each employee has a distinct email address.

4. Check Constraint:

- Details: A check constraint defines a condition that must be satisfied for the data in a column.
- Example:

```sql
CREATE TABLE Students (
    StudentID INT PRIMARY KEY,
    Age INT,
    ...
    CHECK (Age >= 18)
);
```

- In this example, the check constraint ensures that the age of a student is always 18 or greater.

5. Default Constraint:

- Details: A default constraint assigns a default value to a column if no explicit value is provided during insertion.
- Example:

```sql
    CREATE TABLE Employees (
     EmployeeID INT PRIMARY KEY,
     FirstName VARCHAR(50),
     LastName VARCHAR(50),
     EmploymentStatus VARCHAR(20) DEFAULT 'Active'
    );
```

- In this example, if no employment status is specified during the insertion of an employee record, the default value of 'Active' will be assigned to the EmploymentStatus column.

5. Alter Constraint

```sql
-- Adding a unique constraint
ALTER TABLE Employees
ADD CONSTRAINT UC_Email UNIQUE (Email);

-- Adding a foreign key constraint
ALTER TABLE Orders
ADD CONSTRAINT FK_CustomerID
FOREIGN KEY (CustomerID)
REFERENCES Customers(CustomerID);

```

- These ALTER TABLE statements modify the structure of the tables by adding the specified constraints. It is important to note that constraints can be added to existing tables using the ALTER TABLE statement, providing flexibility in enforcing data integrity rules even after the table is created.
