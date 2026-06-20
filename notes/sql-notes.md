# SQL Notes

## Week 1: SQL Basics

---

### SELECT Statement
```sql
SELECT column1, column2 FROM table_name;
SELECT * FROM employees;  -- all columns
SELECT DISTINCT city FROM customers;  -- unique values
```

---

### WHERE (Filtering Rows)
```sql
SELECT * FROM employees WHERE salary > 50000;
SELECT * FROM employees WHERE department = 'Sales';
SELECT * FROM employees WHERE age BETWEEN 25 AND 35;
SELECT * FROM employees WHERE city IN ('Delhi', 'Mumbai', 'Pune');
SELECT * FROM employees WHERE name LIKE 'R%';       -- starts with R
SELECT * FROM employees WHERE email LIKE '%@gmail.com';
SELECT * FROM employees WHERE manager_id IS NULL;    -- check NULL
```

**Operators:** `=`, `!=` or `<>`, `>`, `<`, `>=`, `<=`, `AND`, `OR`, `NOT`

---

### ORDER BY (Sorting)
```sql
SELECT * FROM employees ORDER BY salary DESC;         -- highest first
SELECT * FROM employees ORDER BY department, name ASC; -- multi-column sort
```

---

### LIMIT / OFFSET
```sql
SELECT * FROM employees ORDER BY salary DESC LIMIT 5;         -- top 5
SELECT * FROM employees ORDER BY salary DESC LIMIT 5 OFFSET 5; -- next 5
```

---

### GROUP BY + Aggregate Functions
```sql
SELECT department, COUNT(*) AS emp_count
FROM employees
GROUP BY department;

SELECT department, AVG(salary) AS avg_salary, MAX(salary) AS max_salary
FROM employees
GROUP BY department;
```

**Aggregate functions:** `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`

---

### HAVING (Filter Groups)
```sql
-- HAVING = WHERE but for groups (after GROUP BY)
SELECT department, COUNT(*) AS emp_count
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;

-- WHERE filters rows BEFORE grouping
-- HAVING filters groups AFTER grouping
```

---

### SQL Execution Order
```
FROM → WHERE → GROUP BY → HAVING → SELECT → ORDER BY → LIMIT
```
Remember this! Interview favorite question.

---

### JOINs

#### INNER JOIN (only matching rows from both tables)
```sql
SELECT e.name, d.department_name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.id;
```

#### LEFT JOIN (all rows from left + matching from right)
```sql
SELECT e.name, d.department_name
FROM employees e
LEFT JOIN departments d ON e.dept_id = d.id;
-- employees without department will show NULL for department_name
```

#### RIGHT JOIN (all rows from right + matching from left)
```sql
SELECT e.name, d.department_name
FROM employees e
RIGHT JOIN departments d ON e.dept_id = d.id;
-- departments without employees will show NULL for name
```

#### FULL OUTER JOIN (all rows from both, NULLs where no match)
```sql
SELECT e.name, d.department_name
FROM employees e
FULL OUTER JOIN departments d ON e.dept_id = d.id;
```

#### SELF JOIN (table joined with itself)
```sql
-- Find employee and their manager name
SELECT e.name AS employee, m.name AS manager
FROM employees e
LEFT JOIN employees m ON e.manager_id = m.id;
```

---

### JOIN Visual Summary
```
INNER:      Only intersection (both match)
LEFT:       All left + matching right (NULLs for no match)
RIGHT:      All right + matching left (NULLs for no match)
FULL OUTER: Everything from both (NULLs where no match)
```

---

### Aliases
```sql
SELECT e.name, e.salary AS monthly_pay
FROM employees AS e;  -- AS is optional
```

---

### NULL Handling
```sql
-- NULL is not equal to anything, not even NULL
SELECT * FROM employees WHERE commission IS NULL;
SELECT * FROM employees WHERE commission IS NOT NULL;
SELECT COALESCE(commission, 0) FROM employees; -- replace NULL with 0
```

---

### Common Interview Patterns

**Second highest salary:**
```sql
SELECT MAX(salary) FROM employees
WHERE salary < (SELECT MAX(salary) FROM employees);
```

**Count per group + filter:**
```sql
SELECT department, COUNT(*) 
FROM employees 
GROUP BY department 
HAVING COUNT(*) = (
    SELECT MAX(cnt) FROM (
        SELECT COUNT(*) AS cnt FROM employees GROUP BY department
    ) t
);
```

**Duplicate rows:**
```sql
SELECT email, COUNT(*) 
FROM employees 
GROUP BY email 
HAVING COUNT(*) > 1;
```

---

### Tips for Practice
- Always read the problem statement twice
- Think: what columns do I need? → what table(s)? → any filtering? → any grouping?
- Write query step by step, don't try to write everything at once
- Test with small examples mentally before submitting
