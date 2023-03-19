## SQL

### Create tables

```sql
CREATE TABLE employees (
  id INT PRIMARY KEY,
  first_name VARCHAR(50) NOT NULL,
  last_name VARCHAR(50) NOT NULL,
  job_title VARCHAR(50),
  salary INT,
  department_id INT,
  FOREIGN KEY (department_id)
    REFERENCES departments(id)
);

CREATE TABLE departments (
  id INT PRIMARY KEY,
  name VARCHAR(50) NOT NULL
);

```

1. Retrieve data from a table:

- Select all columns from the employees table.
- Select only the first_name and last_name columns from the employees table.

2. Filter data using the WHERE clause:

- Select all employees from the employees table who work in the Sales department.
- Select all employees from the employees table who have a salary greater than $50,000.

3. Sort data using the ORDER BY clause:

- Select all employees from the employees table sorted by their last name in ascending order.
- Select all employees from the employees table sorted by their salary in descending order.

4. Modify data using the UPDATE statement:

- Update the salary of the employee with an ID of 12345 to $60,000 in the employees table.
- Update the department of all employees with a job title of "Manager" to "Executive" in the employees table.

5. Remove data using the DELETE statement:

- Delete all employees from the employees table who have a salary less than $30,000.
- Delete the employee with an ID of 67890 from the employees table.

6. Add data using the INSERT statement:

- Add a new employee with a first name of "Jane" and a last name of "Doe" to the employees table with a salary of $40,000.
- Add a new department called "Marketing" to the departments table.
