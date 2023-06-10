## Command

-   **Summary**
    
    `TODO: Create summary`
    

## Using a Subquery to Solve a Problem

## Subquery Syntax

```jsx
SELECT select_list
FROM table
WHERE expr_operator

	(SELECT select_list
	FROM table);
```

```sql
SELECT last_name salary
FROM employees
WHERE salary >
	(SELECT salary
	FROM employees
	WHERE last_name = 'Abel');
```

## Types of Subqueries

**Note:** There are also multiple-column subqueries, which are queries that return more than one column from the inner SELECT statement.

### Single-Row Subquery

Queries that return only one row from the inner SELECT statement

### Multiple-Row Subquery

Queries that return more than one row from the inner SELECT statement

## Executing Single-Row Subqueries

```sql
SELECT last_name, job_id, salary
FROM employees
WHERE job_id = 
	(SELECT job_id
	FROM employees
	WHERE employee_id = 141)
AND salary >
	(SELECT salary
	FROM employees
	WHERE employee_id = 143);
```

## Using Group Functions in a Subquery

```sql
SELECT last_name, job_id, salary
FROM employees
WHERE salary =
	(SELECT MIN(salary)
	FROM employees);
```

```sql
SELECT department_id, MIN(salary)
FROM employees
GROUP BY department_id
HAVING MIN(salary) >
	(SELECT MIN(salary)
	FROM employees
	WHERE department_id = 50);
```

## Incorrect Subquery Syntax

```sql
SELECT employee_id, last_name
FROM employees
WHERE salary =
	(SELECT MIN(salary)
	FROM employees
	GROUP BY department_id)

```

```sql
ERROR at line 4:
ORA-01427: single-row subquery returns more than one row
```

***Note:*** The `WHERE` clause only accepts one value thus, group rows are invalid

## Return No Rows

```sql
SELECT last_name, job-id
FROM employees
WHERE job_id =
	(SELECT job_id
	FROM employees
	WHERE last_name = 'Haas'
```

Subquery returns no values since there is no employee named Haas.

There is no `job_id = NULL` thus, returns no rows.

## Multiple-Row Subqueries

| Operator | Definition                                           |
| -------- | ---------------------------------------------------- |
| IN       | Equal to any member in the list                      |
| ANY      | Compare value to each value returned by the subquery |
| ALL      | Compare value to every value returned by the subquery                                                     |

### IN Operator

```sql
SELECT last_name, salary, department_id
FROM employees
WHERE salary IN
	(SELECT MIN(salary)
	FROM employees
	GROUP BY department_id);
```

```sql
SELECT last_name, salary, department_id
FROM employees
WHERE salary IN (2500,4200,4400,6000,7000,8300,8600,17000);
```

### ANY Operator

```sql
SELECT employee_id, last_name, job_id, salary
FROM employees
WHERE salary < ANY
	(SELECT salary
	FROM employees
	WHERE job_id = 'IT_PROG')
AND job_id <> 'IT_PROG';
```

<<<<<<< HEAD
`< ANY`: less than the maximum

`> ANY:` more than the maximum
=======
************`< ANY`:** less than the maximum

`> ******ANY`:** more than the maximum
>>>>>>> origin/main

************`= ANY`:** equivalent to IN

### ALL Operator

```sql
SELECT employee_id, last_name, job_id, salary
FROM employees
WHERE salary < ALL
	(SELECT salary
	FROM employees
	WHERE job_id = 'IT_PROG')
AND job_id <> 'IT_PROG';
```

`> ALL` more than the maximum

`< ALL` less than the minimum

`NOT` can be used with `IN`, `ANY`, and `ALL` operators

<<<<<<< HEAD
=======
## ANY and ALL Comparison

******ANY******

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3016f0ca-ed24-46c9-b89f-e6bd311eed80/Untitled.png)

********ALL********

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d90d1b06-3b00-4e6a-b979-037f06769111/Untitled.png)

>>>>>>> origin/main
### NULL Values

Does not return any rows due to the existence of a single NULL value

```sql
SELECT emp.last_name
FROM employees emp
WHERE emp.employee_id NOT IN
	(SELECT mgr.manager_id
	FROM employees mgr);
```

<<<<<<< HEAD
**Display Employees who have subordinates**
=======
******************************************************************************Display Employees who have subordinates******************************************************************************
>>>>>>> origin/main

```sql
SELECT emp.last_name
FROM employees emp
WHERE emp.employee_id IN
	(SELECT mgr.manager_id
	FROM employees mgr);
```

<<<<<<< HEAD
**Display all employees who do not have any subordinates**
=======
******************Display all employees who do not have any subordinates******************
>>>>>>> origin/main

```sql
SELECT last_name FROM employees
WHERE employee_id NOT IN
	(SELECT manager_id
	FROM employees
WHERE manager_id IS NOT NULL);
```

## GROUP BY and HAVING

```sql
SELECT department_id, MIN(salary)
FROM employees
GROUP BY department_id
HAVING MIN(salary) < ANY
	(SELECT salary
	FROM employees
	WHERE department_id IN (10,20))
ORDER BY department_id;
```

Return the salaries of employees in departments 10 and 20.

MIN is used to group the outer query by department_id

## Multiple-Column Subqueries

```sql
SELECT employee_id, manager_id, department_id
FROM employees
WHERE (manager_id, department_id) IN
	(SELECT manager_id, department_id
	FROM employees
	WHERE employee_id IN (149,174))
AND employee_id NOT IN (149,174)
```

List the employees whose manager and departments are the same as the manager and department of employees 149 or 174.

```sql
SELECT employee_id, manager_id, department_id
FROM employees
WHERE manager_id IN
	(SELECT manager_id
	FROM employees
	WHERE employee_id IN (149,174))
AND department_id IN
	(SELECT department_id
	FROM employees
	WHERE employee_id IN (149,174))
AND employee_id NOT IN (149,174);
```

-   Non-pair wise multiple-column subquery
-   Uses more than one column
-   Compares one at a time

## EXISTS and NOT EXISTS

<<<<<<< HEAD
**NOT EXISTS**
=======
********************NOT EXISTS********************
>>>>>>> origin/main

```sql
SELECT last_name AS "Not a Manager"
FROM employees emp
WHERE NOT EXISTS
	(SELECT *
	FROM employees mgr
	WHERE mgr.manager_id = emp.employee_id)e
```

<<<<<<< HEAD
**NOT IN**
=======
************NOT IN************
>>>>>>> origin/main

```sql
SELECT last_name AS "Not a Manager"
FROM employees emp
WHERE emp.employee_id NOT IN
	(SELECT mgr.manager_id
	FROM employees mgr)
```

## Correlated Subqueries

<<<<<<< HEAD
| **Operator** | **Definition**                        |
| ------------ | ------------------------------------- |
| `GET`        | Candidate row from outer query        |
| `EXECUTE`    | Inner query using candidate row value |
| `USE`        | Values from innery query to qualify or disqualify candidate row                                      |
=======
Operator

Definition

GET

candidate row from outer query

EXECUTE

inner query using candidate row value

USE

values from inner query to qualify or disqualify candidate row
>>>>>>> origin/main

```sql
SELECT o.first_name,
	o.last_name,
	o.salary
FROM employees o
WHERE o. salary >
	(SELECT AVG(i.salary)
	FROM employees i
	WHERE i.department_id = o.department_id);
```

<<<<<<< HEAD
=======
![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/79edaf12-43bc-49cd-b8b3-3682cb773225/Untitled.png)

>>>>>>> origin/main
### WITH Clause

```sql
WITH subquery-name AS (subquery),
	subquery-name AS (subquery)
	SELECT column-list
	FROM (table | subquery-name | view)
	WHERE condition is true;
```

```sql
WITH managers AS
	(SELECT DISTINCT manager_id
	FROM employees
	WHERE manager_id IS NOT NULL)
SELECT last_name AS "Not a manager"
FROM employees
WHERE employee_id NOT IN
 (SELECT *
 FROM managers);
```