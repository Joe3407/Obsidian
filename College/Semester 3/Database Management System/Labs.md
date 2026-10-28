## 📘Lab 1

- **Null:** 
	- It's never tested with `=NULL`, but it's tested with `IS NULL` 
	- Null mulitply with anything gives null
- **Alias:**
	- Using `AS` is optional
	- Witout Double Quotes, it can't contain special characters, and the name will be Lower case by default 
	- Use Double Quotes for special characters, and customized case 
	- Double Quotes is only used for alias 
- **Distinct:** Removes duplicate rows, and is written after select, e.g. `SELET DISTINCT last_name` 
- **Between:** Inclusive range, lower limit first, e.g. `Between 250 AND 300`
- **In:** Matches any values in a list, e.g. `IN (100, 101, 102)` 
- **Like:** 
	- `%` $\to$ zero or many chars, e.g. `LIKE 'o%'` which means any data containing o as first char
	- `_` $\to$ exactly one char, e.g. `LIKE _o%` which means any data containing o as its second char 
- **Order by:** Always last clause, its `ASC` by default can be desending by `DESC`, e.g. `ORDER BY hire_date DESC` 

---
## 📘Lab 2

- **Single-Row Functions:**
	- **Lower:** Converts the data to lower case letters, e.g. `WHERE LOWER(last_name) = 'feil'`, same for `UPPER`, and `INITCAP` which makes each word start with Capital letter
	- **NVL:** Converts a null to an actual value, e.g. `NVL(job_id,0)`, where the value is the same data type as `job_id`, in PostgreSQL it's `COALESCE` 
	- **SYSDATE:** It's a function that returns the current date and time, e.g. `SELECT (SYSDATE-hire_date)/7`, which returns the number of weeks they worked since they started, in PostgreSQL there is no `SYSDATE`, instead `CURRENT_DATE` 
- **Group Functions:**
	- **Min & Max:** e.g. `SELECT MIN(hire_date), MAX(hire_date)`
	- **Sum:** e.g. `SELECT SUM(salary)` 
	- **Count:**
		- `SELECT COUNT(*)` counts number of rows containing duplicate and null values 
		- `SELECT COUNT(job_id)` counts number of rows with Non-Null values 
		- `SELECT COUNT(DISTINCT job_id)` counts number of distinct Non-Null values 
	- **AVG:** It discards null values by default, but can use NVL to make it count them from the sum and the value is 0, e.g. `SELECT AVG(NVL(salary,0))`
- **Group By:** When we want to calculate the sum of salary for each department, e.g. `GROUP BY department_id` 
- **Having:** It's used to put conditions on Group By data 

---
## 📘Lab 3

- **Sub-Queries:**
	- **Single Row:**
		- Operator is `=`, `<>`, `>`, `<`, `>=`, `<=` 
		- If we want the salaries of all employees which have greater than employeeA but all we know is the id of employeeA
		- So we can do a sub-query where we get the salary of employeeA using his id, then comparing the result with the first query 
	- **Multiple Row:**
		- Operator is `IN` 
		- Used when the return value of the sub-query is multiple rows 
- **Join:**
	- **Inner Join:**
		- If we have two tables having a common attribute, so we join them both 
		- e.g. `WHERE e.department_id=d.id` 
	- **Outer Join:**
		- If we have employees without a department, or a department that doesn't contain employees
		- e.g. `WHERE e.department_id(+) = d.id`, this means that put the employees with null that doesn't work for this department, meaning if an emplyee works for HR but not PR, so then put a new row having employee as null and the department as PR 
	- **Note:** 
		- If we have $n$ tables that we want to join, then there is $n-1$ conditions needed to join them 
		- **Cartesian Product:** It's when we don't join the tables, so every attribute from the first table gets a row with every attribute of second table 
- **Data Manipulating Language (DML):**
	- **Insert:** `INSERT INTO department_id` `VALUES (...)`, or `INSERT INTO department_id` `(id, name, code)` `VALUES (...)` 
	- **Update:** `UPDATE departments` `SET department_id = value` `WHERE condition` 
	- **Delete:** `DELETE FROM departments` `WHERE condtion` 

---

