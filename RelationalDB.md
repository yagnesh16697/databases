# Relational Databases

- Data (Records) is stored in tables, organized into rows and columns.
- Tables can be related to other tables using 1:1, 1:N, or N:N relations.

### Normal Forms:

Normal Forms are used to reduce redundancy and improve data integrity (1NF 2NF 3NF 4NF 5NF BCNF....).

**Constraints** can be placed on columns and combinations of columns to ensure data quality, such as:

- Unique: values must be unique within a column
- NOT NULL: values must not be null
- Primary Key: unique identifier for each row in a table
- Foreign Key: column that references the primary key of another table.

### Transactions

1. **Atomicity**: Each transaction is a single unit of execution.
2. **Consistency**: Databse goes from one valid state to another.
3. **Durability**: Past commit data is recoverable even after failure of system.
4. **Isolation**: Concurrent execution == Sequential execution.
