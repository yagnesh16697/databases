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

21. Using correlated subqueries:

    - Select all employees from the employees table and add a column that displays their department's average salary. Use a correlated subquery to calculate the average salary for each employee's department.

22. Using self joins:

    - Select all employees from the employees table and add a column that displays the name of their manager. Use a self join on the employees table to retrieve this information.

23. Using window functions:

    - Select all employees from the employees table and add a column that displays their salary rank within their department. Use a window function to calculate the rank.

24. Using pivot tables:

    - Create a pivot table that shows the total salary for each department broken down by job title from the employees table.

25. Using recursive queries:

    - Select all employees who report directly or indirectly (i.e., through one or more levels of managers) to a particular manager from the employees table. Use a recursive query to traverse the employee hierarchy.

26. Using temporary tables:

    - Create a temporary table that stores the total salary for each department from the employees table. Then, use this temporary table to join with the departments table to retrieve additional department information.

27. Using subqueries to modify data:

    - Update the salary of all employees in the Sales department to be 10% higher than the average salary of all employees in that department. Use a subquery to calculate the average salary.

28. Using common table expressions:

    - Select all employees from the employees table and add a column that displays the name of their department's manager. Use a common table expression to retrieve this information.

29. Using stored procedures:

    - Create a stored procedure that retrieves all employees from the employees table and returns the result set sorted by salary in descending order.

30. Using triggers:

    - Create a trigger that automatically updates the salary column of the employees table whenever the job_title column of the same table is modified.

31. Using full-text search:

    - Select all employees from the employees table whose job title contains the phrase "software engineer". Use full-text search to perform this query.

32. Using JSON data:

    - Create a table that stores JSON data for each employee in the employees table. Then, use JSON functions to extract specific information from this data.

33. Using XML data:

    - Create a table that stores XML data for each employee in the employees table. Then, use XML functions to extract specific information from this data.

34. Using spatial data:

    - Create a table that stores spatial data (e.g., latitude and longitude coordinates) for each employee in the employees table. Then, use spatial functions to perform calculations on this data.

35. Using time-series data:

    - Create a table that stores time-series data (e.g., stock prices) for a particular security. Then, use time-series functions to calculate moving averages or other metrics.

36. Using partitioning:

    - Partition the employees table by department so that data for each department is stored in a separate physical file. Then, use partition functions to retrieve data efficiently.

37. Using indexing:

    - Add indexes to the employees table to improve query performance. Experiment with different types of indexes (e.g., clustered vs. non-clustered, covering, filtered) to see how they affect query execution time.

38. Using database views:

    - Create a view that joins the employees and departments tables and displays only the columns that are relevant for reporting purposes. Use this view to retrieve data for reports.

39. Using database backups and restores:

    - Create a backup of your SQL database and restore it to a different server. Verify that the restored database contains the same data as the original database.

40. Using replication:

    - Set up replication between two SQL servers so that changes made to the employees table on one server are automatically propagated to the other server. Test this setup by making changes on both servers and verifying that the changes are replicated correctly.
