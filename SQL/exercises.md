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

7. Joining tables using the JOIN command:

   - Select all employees and their department names from the employees and departments tables.
   - Select all employees and their manager's name (if a manager exists) from the employees table. Hint: You will need to join the employees table to itself using a self-join.

8. Using subqueries to filter data:

   - Select all departments with more than 3 employees from the departments table.
   - Select all employees who work in a department with a budget greater than $500,000. Assume each department has a budget column in the departments table.

9. Using functions to manipulate data:

   - Calculate the average salary of all employees in the employees table.
   - Calculate the maximum salary of all employees who work in the Sales department.

10. Using grouping to aggregate data:

    - Count the number of employees in each department in the employees table.
    - Calculate the total salary for each job title in the employees table.

11. Using transactions to modify data:

    - Create a transaction that updates the salary of all employees in the Sales department to $60,000.
    - Create a transaction that deletes all employees who have a salary less than $30,000.
