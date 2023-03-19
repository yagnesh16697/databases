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

12. Using the HAVING clause:

    - Select all departments with an average salary greater than $70,000 from the employees table grouped by department.

13. Using the UNION operator:

    - Select all employees who work in the Sales department from the employees table and all employees who have a job title of "Manager" from the same table.
    - Combine the results of two queries that retrieve the names of all departments and all job titles from the departments and employees tables, respectively.

14. Using the IN operator:

    - Select all employees who work in departments with IDs 1, 3, or 5 from the employees table.
    - Select all employees who have job titles of either "Manager" or "Director" from the employees table.

15. Using the EXISTS operator:

    - Select all departments that have at least one employee from the departments table.
    - Select all employees who have a manager from the employees table.

16. Using the LIKE operator:

    - Select all employees whose last name starts with "M" from the employees table.
    - Select all employees whose first name contains the substring "an" from the employees table.

17. Using the CASE statement:

    - Select all employees from the employees table and add a column that displays "High" if their salary is greater than $80,000, "Medium" if their salary is between $50,000 and $80,000, and "Low" if their salary is less than $50,000.

18. Using the GROUP_CONCAT function:

    - Select all departments from the departments table and concatenate the first names of all employees who work in each department into a single string.

19. Using the LIMIT clause:

    - Select the top 5 highest paid employees from the employees table.
    - Select the 10 most recently hired employees from the employees table.

20. Using the DATE functions:

    - Select all employees from the employees table who were hired in January.
    - Select all employees from the employees table whose hire date was more than 5 years ago.
