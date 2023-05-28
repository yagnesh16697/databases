1. Primary Key (PK):

Details: A primary key uniquely identifies each row in a table.
Example: In a "Customers" table, the "CustomerID" column can be designated as the primary key, ensuring that each customer has a unique identifier.

2. Foreign Key (FK):

Details: A foreign key establishes a relationship between two tables by referencing the primary key of another table.
Example: In an "Orders" table, the "CustomerID" column can be a foreign key that references the primary key of the "Customers" table, connecting each order to a specific customer.

3. Unique Key (UK):

Details: A unique key ensures that the values in a column or a set of columns are unique within a table.
Example: In an "Employees" table, the "EmployeeID" column can have a unique key constraint, ensuring that each employee has a distinct identifier.

4. Candidate Key:

Details: A candidate key is a column or a set of columns that can potentially become a primary key.
Example: In a "Students" table, both the "StudentID" and "Email" columns can be candidate keys, as they can uniquely identify a student.

5. Composite Key:

Details: A composite key is a key that consists of multiple columns, working together to uniquely identify a row.
Example: In a "Books" table, a composite key could be formed by combining the "ISBN" and "Edition" columns, ensuring that no two books have the same ISBN and edition.

6. Surrogate Key:

Details: A surrogate key is an artificial primary key assigned to a table that lacks a natural key.
Example: In a "Products" table, an auto-incrementing "ProductID" column can serve as a surrogate key, providing a unique identifier for each product.

7. Alternate Key:

Details: An alternate key is a candidate key that is not selected as the primary key.
Example: In a "Countries" table, both the "CountryCode" and "CountryName" columns can be alternate keys, as they can uniquely identify a country.

8. Super Key:

Details: A super key is a set of one or more columns that can uniquely identify a row.
Example: In a "Students" table, a super key can be formed by combining the "StudentID," "FirstName," and "LastName" columns, as it can uniquely identify a student.
