Joins

Inner Join -

What is an SQL Inner Join?
-> An INNER JOIN is used to combine rows from two tables based on a related column between them. It returns only the rows where there is a match in both tables.

Example Tables
Employees Table:

employee_id	employee_name	department_id
1	           Alice	      101
2	           Bob	        102
3	           Charlie	    101

Departments Table:

department_id	   department_name
101	             Sales
102	             Marketing
103	             IT

Query -

SELECT Employees.employee_id, Employees.employee_name, Departments.department_name
FROM Employees
INNER JOIN Departments ON Employees.department_id = Departments.department_id;

SQL Left Join (or Left Outer Join) -

A LEFT JOIN returns all rows from the left table and the matched rows from the right table. If there is no match, the result is NULL on the side of the right table.

Query -

SELECT Employees.employee_id, Employees.employee_name, Departments.department_name
FROM Employees
LEFT JOIN Departments ON Employees.department_id = Departments.department_id;


The LEFT JOIN ensures that all rows from the Employees table are included, even if there is no matching department_id in the Departments table.

SQL Right Join (or Right Outer Join) -

A RIGHT JOIN returns all rows from the right table and the matched rows from the left table. If there is no match, the result is NULL on the side of the left table.

Query -

SELECT Employees.employee_id, Employees.employee_name, Departments.department_name
FROM Employees
RIGHT JOIN Departments ON Employees.department_id = Departments.department_id;

The RIGHT JOIN ensures that all rows from the Departments table are included, even if there is no matching department_id in the Employees table.

Summary
LEFT JOIN: Returns all rows from the left table and matched rows from the right table. If no match, NULL on the right side.
RIGHT JOIN: Returns all rows from the right table and matched rows from the left table. If no match, NULL on the left side.

SQL Full Join (or Full Outer Join) -

A FULL JOIN returns all rows when there is a match in either left or right table. If there is no match, the result is NULL on the side where there is no match.

Query -

SELECT Employees.employee_id, Employees.employee_name, Departments.department_name
FROM Employees
FULL OUTER JOIN Departments ON Employees.department_id = Departments.department_id;

The FULL JOIN ensures that all rows from both tables are included, even if there is no matching department_id in the other table.

SQL Self Join -

A SELF JOIN is a regular join, but the table is joined with itself. This is useful for comparing rows within the same table.

Query -

SELECT e1.employee_id, e1.employee_name, e2.employee_name AS manager_name
FROM Employees e1
LEFT JOIN Employees e2 ON e1.manager_id = e2.employee_id;

The SELF JOIN allows you to compare rows within the same table, such as finding the manager of each employee.

SQL Union -

A UNION is used to combine the result sets of two or more SELECT statements. Each SELECT statement within the UNION must have the same number of columns in the result sets with similar data types.

Query -

SELECT customer_name AS name, city
FROM Customers
UNION
SELECT supplier_name AS name, city
FROM Suppliers;

Breakdown of the Query
SELECT customer_name AS name, city FROM Customers

This part retrieves the customer_name and city columns from the Customers table, with customer_name aliased as name.
UNION

This keyword combines the result sets of the two SELECT statements.
SELECT supplier_name AS name, city FROM Suppliers

This part retrieves the supplier_name and city columns from the Suppliers table, with supplier_name aliased as name.

The UNION combines the result sets of the two SELECT statements, providing a unified list of names and cities from both the Customers and Suppliers tables.


