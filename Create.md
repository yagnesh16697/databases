1. Creating a simple table:

```sql
CREATE TABLE Customers (
  CustomerID INT PRIMARY KEY,
  FirstName VARCHAR(50),
  LastName VARCHAR(50),
  Age INT
);
```

2. Creating a table with foreign key constraint:

```sql
CREATE TABLE Orders (
  OrderID INT PRIMARY KEY,
  CustomerID INT,
  OrderDate DATE,
  FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);
```

3. Creating a table with unique key constraint:

```sql
CREATE TABLE Employees (
  EmployeeID INT PRIMARY KEY,
  FirstName VARCHAR(50),
  LastName VARCHAR(50),
  Email VARCHAR(100) UNIQUE
);
```

4. Creating a table with composite primary key:

```sql
CREATE TABLE Products (
  ProductID INT,
  CategoryID INT,
  ProductName VARCHAR(100),
  PRIMARY KEY (ProductID, CategoryID)
);
```

5. Creating a table with auto-incrementing surrogate key:

```sql
CREATE TABLE Students (
  StudentID INT PRIMARY KEY AUTO_INCREMENT,
  FirstName VARCHAR(50),
  LastName VARCHAR(50),
  Age INT
);
```
