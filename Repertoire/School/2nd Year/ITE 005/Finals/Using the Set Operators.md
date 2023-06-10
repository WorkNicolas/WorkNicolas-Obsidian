## Set Operators

| **Operator** | **Returns**                                                 |
| ------------ | ----------------------------------------------------------- |
| UNION        | All distinct rows selected by either query                  |
| UNION ALL    | All rows selected by either query, including all duplicates |
| INTERSECT    | All distinct rows selected by both queries                  |
| MINUS             | All distinct rows that are selected by the first SELECT statement and not selected in the second SELECT statement                                                           |

## Tables Used
-   employees
-   job_history

## UNION Operator
Display the current and previous job details of all employees. Display each employee only once.
```sql
SELECT employee_id, job_id
FROM employees
UNION
SELECT employee_id, job_id
FROM job_history
```

## UNION ALL Operator
Display the current and previous departments of all employees.

```sql
SELECT employee_id, job_id, department_id
FROM employees
UNION ALL
SELECT employee_id, job_id, department_id
FROM job_history
ORDER BY employee_id
```

## INTERSECT Operator
Display the employee IDs and job IDs of those employees who currently have job title that is the same as their job title when they were initially hired (i.e. they changed jobs but have now gone back to doing their original job)

```sql
SELECT employee_id, job_id
FROM employees
INTERSECT
SELECT employee_id, job_id
FROM job_history
```

## MINUS Operator
Display the employee IDs of those employees who have not changed their jobs even once

```sql
SELECT employee_id
FROM employees
MINUS
SELECT employee_id
FROM job_history
```

## Set Operator Guidelines
-   expressions in the `SELECT` lists must match number and data type
-   Parentheses can be used to alter the sequence of execution
-   Order by clause
    -   Can appear only at the very end of the statement
    -   Will accept the column name, aliases from the first `SELECT` statement, or the positional statement

## Matching the `SELECT` Statements
Using the `UNION` operator, display the department ID, location, and hire date for all employees.

```sql
SELECT department_id, TO_NUMBER(null),
	location, hire_date
FROM employees
UNION
SELECT department_id, location_id, TO_DATE(null)
FROM departments
```

## Controlling the Order of Rows
Produce an English sentence using two `UNION` operators

```sql
COLUMN a_dummy NOPRINT
SELECT 'sing' AS "My dream", 3 a_dummy
FROM dual
UNION 
SELECT 'I''d like to teach', 1 a_dummy
FROM dual
UNION
SELECT 'the world to', 2 a_dummy
FROM dual
ORDER BY a_dummy
```