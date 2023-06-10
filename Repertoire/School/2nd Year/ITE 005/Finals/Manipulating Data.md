# Data Manipulation Language
- A DML Statement is executed when you
	- Add new rows to a table
	- Modify existing rows in a table
	- Remove existing rows from a table
- A transaction consists of a collection of DML statements that form a logical unit of work
- 
## `INSERT` Statement
### `INSERT` Syntax
```sql
INSERT INTO table[(column [, column...])]
VALUES (value [, value])
```

### Example
```sql
INSERT INTO departments(department_id,
						department_name, manager_id, location_id)
VALUES (70, 'Public Relations', 100, 1700)
```

### `NULL` Values
**Implicit Method:** Omit the column from the column list
```sql
INSERT INTO deparments (department_id, department_name)
VALUES (30,'Purchasing')
```

**Explicit Method:** Specify the `NULL` keyword in the `VALUES` clause
```sql
INSERT INTO departments
VALUES (100,'Finance', NULL, NULL)
```

**Common Errors**
- Mandatory value missing for a `NOT NULL` column
- Duplicate values violate uniqueness constraint
- Foreign key constraint violated
- `CHECK` constraint violated
- Data type mismatch
- Value too wide to fit in a column

### Special Values
`SYSDATE` function records the current date and time
```sql
INSERT INTO employees (employee,id
					  first_name, last_name,
					  email, phone_number,
					  hire_date, job_id, salary,
					  commission_pct, manager_id
					  department_id)
VALUES (113,
	   'Louis', 'Popp',
	   'LPOPP', '515.124.4567',
	   SYSDATE, 'AC_ACCOUNT', 6900,
	   NULL, 205, 100)
```

`USER` function records the current username
```sql
SELECT employee_id, last_name, job_id, hire_date, commission_pct
FROM employees
WHERE employee_id = 113
```

### Specific Date Values
```sql
INSERT INTO employees
VALUES (114,
	   'Den', 'Raphealy',
	   'DRAPHAL', '515.127.4561',
	   TO_DATE('FEB 3, 1999', 'MON DD, YYYY'),
	   'AC_ACCOUNT', 11000, NULL, 100, 30)
```

Automatically identifies `HIRE_DATE` as ‘February 3, 1999’ (RR Format)
```sql
INSERT INTO employees
VALUES (114,
	   'Den', 'Raphaely',
	   'DRAPHAEL', '515.127.4561',
	   '03-FEB-99',
	   'AC_ACCOUNT', 11000, 100, 30)
```

### Creating a Script
- Use &substitution in an SQL statement to prompt for values
- & is a placeholder for the variable value

```sql
INSERT INTO departments (deparment_id,
						department_name, location_id)
VALUES (&department_id, &department_name, &location_id)
```

### Copying Rows from Another Table
Write statement using subquery
- Do not use `VALUES` clause
- Match the number of columns in the `INSERT` clause to those in the subquery
```SQL
INSERT INTO sales_reps(id, name, salary, commission_pct)
	SELECT employee_id, last_name, salary, commission_pct
	FROM employees
	WHERE job_id LIKE '%REP'
--4 rows created
```

## `UPDATE` Statement
### `UPDATE` Syntax
```sql
UPDATE employees
SET department_id = 70
WHERE employee_id = 113
--1 row updated
```

```sql
UPDATE copy_emp
SET department_id = 110
--22 rows updated
```

### Updating Two Columns with a Subquery
```sql
UPDATE employees
SET job_id = (SELECT job_id
			 FROM employees
			 WHERE employee_id = 205),
			 
```

### Updating Rows Based on Another Table

## `DELETE` Statement
### `DELETE` Syntax
```sql
DELETE (FROM)
```

### Example

## `TRUNCATE` Statement
### `TRUNCATE` Syntax
```sql
TRUNCATE TABLE table_name
```

### Example
```sql
TRUNCATE table copy_emp
```

**Use Case**
- The `TRUNCATE` statement is a Data Definition Language (DDL)

### Using Subquery to 

## Database Transactions
- DML Statements that constitute one consistent change to the data
- One DDL Statement
- One DCL statement
- Begin when the first DML SQL statement is executed
- End with one of the following
	- A `COMMIT` or `ROLLBACK` statement is issued

| **Type**                   | **Definition** |
| -------------------------- | -------------- |
| Data Manipulation Language |                |
|                            |                |
|                            |                |

### Controlling Transactions
**Explicit Transaction Control Statements**

### Rolling Back Changes to a Marker

### 