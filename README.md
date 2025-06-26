CREATE TABLE employees (
    id INTEGER PRIMARY KEY AUTO_INCREMENT, 
    first_name TEXT NOT NULL,
    last_name TEXT NOT NULL,
    department TEXT,
    salary INTEGER
);

-- 2. Insert sample data
INSERT INTO employees (first_name, last_name, department, salary) VALUES
('Alice', 'Johnson', 'Engineering', 75000),
('Bob', 'Smith', 'Sales', 50000),
('Charlie', 'Lee', 'Engineering', 82000),
('Diana', 'Ross', 'HR', 60000),
('Ethan', 'Brown', 'Sales', 45000),
('Fiona', 'Davis', 'Engineering', 70000),
('George', 'Miller', 'HR', 55000);

-- 3. SELECT: Get all data
SELECT * FROM employees;

-- 4. SELECT: Specific columns
SELECT first_name, last_name, department FROM employees;

-- 5. WHERE: Filter employees from 'Engineering'
SELECT * 
FROM employees
WHERE department = 'Engineering';

-- 6. WHERE: Employees with salary over 60000
SELECT * 
FROM employees
WHERE salary > 60000;

-- 7. ORDER BY: Sort by salary descending
SELECT first_name, last_name, salary 
FROM employees
ORDER BY salary DESC;

-- 8. LIMIT: Top 3 highest-paid employees
SELECT first_name, last_name, salary 
FROM employees
ORDER BY salary DESC
LIMIT 3;

-- 9. Combined: Engineers with salary > 70000, sorted by salary, top 2 only
SELECT first_name, last_name, department, salary
FROM employees
WHERE department = 'Engineering' AND salary > 70000
ORDER BY salary DESC
LIMIT 2;
