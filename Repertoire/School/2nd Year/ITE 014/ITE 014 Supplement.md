## Creating Other Schema Objects
| **Keyword** | **Definition**                                                             |
| ----------- | -------------------------------------------------------------------------- |
| View        | Logical table based on a table or another view                             |
| Sequence    | Database object that generates integer values                              |
| Index       | Database object that can be created to improve performance of some queries |
| Synonym     | Database object that provide an alternative name for a table, view, sequence, procedure, or other objects                                                                           |

### View Syntax
```sql
% Syntax
CREATE [OR REPLACE] [FORCE|NOFORCE] VIEW view [(alias[, alias]...)] AS subquery [WITH CHECK OPTION [CONSTRAINT constraint]] [WITH READ ONLY [CONSTRAINT constraint]];

% Example
CREATE VIEW empvu80 AS SELECT employee_id, last_name FROM employees WHERE department_id = 80;
```

### Sequence Syntax
```sql
% Syntax
CREATE SEQUENCE sequence [INCREMENT BY n] [{MAXVALUE n | NOMAXVALUE}] [{MINVALUE n | NOMINVALUE}] [{CYCLE | NOCYCLE}] [{CACHE n | NOCACHE}];

% Example
CREATE SEQUENCE dept_deptid_seq START WITH 120 INCREMENT BY 10 NOCACHE NOCYCLE;`
```

### Index Syntax
```sql
CREATE [UNIQUE] INDEX index ON table (column[, column]...) [REVERSE];

CREATE INDEX upper_last_name_idx ON employees (UPPER(last_name));
```

### Synonym Syntax
```sql
% Syntax
CREATE [PUBLIC] SYNONYM synonym FOR object;

% Example
CREATE SYNONYM emp FOR hr.employees;
```

## Managing Objects with Data Dictionary Views