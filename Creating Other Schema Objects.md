## Database Objects
| **Object** | **Description**                                              |
| ---------- | ------------------------------------------------------------ |
| Table      | Basic unit of storage                                        |
| View       | Logically represents subsets of data from one or more tables |
| Sequence   | Generates numeric values                                     |
| Index      | Improves the performance of some queries                     |
| Synonym    | Gives alternative names to objects                                                             |

## Detailed Description
**View**
- Present and hide data from tables

**Sequence**
- generate unique numbers for applications that require unique or primary key values

**Index**
- improve query performance
- enforce uniqueness on a column or a collection of columns

## View
- A view is a location table based on a table or another view
- Logical subsets or combinations of data
- Contains no data of its own
- Stored as a `SELECT` statement in the data dictionary

## Advantages of Views
**To restrict data access**
Views restrict access to the data because the view can display selected columns from the table.

**To make complex queries easy**
Views can be used to make simple queries to retrieve the results of complicated queries. For example, views can be used to query information from multiple tables without the user knowing how to write a join statement.

**To provide data independence**
Views provide data independence for ad hoc users and application programs. One view can be used to retrieve data from several tables.

**To prevent different views of same data**
Views provide groups of users access to data according to their particular criteria

## Simple Views and Complex Views

| **Features**                  | **Simple Views** | **Complex Views** |
| ----------------------------- | ---------------- | ----------------- |
| Number of Tables              | One              | One or more       |
| Contains Functions            | No               | Yes               |
| Contains Group of Data        | No               | Yes               |
| DML Operations through a View | Yes              | Not always                  |

## View Syntax
```sql
CREATE [OR REPLACE) [FORCE|NOFORCE) VIEW view
	[ (alias[, alias]... ) I
AS subquery
[WITH CHECK OPTION [CONSTRAINT constraint]
[WITH READ ONLY (CONSTRAINT constraint]
```

| **SYNTAX**        | **Description**                                                                                                                                   |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| `OR REPLACE`        | Re-creates view if it already exists                                                                                                              |
| `FORCE`             | Creates the view regardless of whether or not the base tables exist                                                                               |
| `NOFORCE`           | Creates the view only if the base tables exist (default)                                                                                          |
| `view`              | Name of the view                                                                                                                                  |
| `alias`             | Specifies names for the expressions selected by the view’s query. The number of aliases must match the number of expressions selected by the view |
| `subquery`          | Complete `SELECT` statement                                                                                                                       |
| `WITH CHECK OPTION` | Specifies that only those rows that are accessible to the view can be inserted or updated                                                         |
| `constraint`        | Name assigned to the `CHECK OPTION` constraint                                                                                                    |
| `WITH READ ONLY`    | Ensures that no DML operations can be performed on this view                                                                                                                                                  |

## View Example
```sql
CREATE VIEW empvu80
	AS SELECT employee_id, last_name, salary
	FROM employees
	WHERE department_id = 80
```

## View Guidelines
- The subquery that defines a view can contain complex `SELECT` syntax including joins, gorups, and subqueries
- If you do not specify a constraint name for a view created with the `WITH CHEKC OPTION`, the system assigns a default name in the format `SYS_Cn`
- You can use the `OR REPLACE` option to change the definition of view without dropping and re-creating it or regranting object priveleges
