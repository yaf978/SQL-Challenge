SELECT * FROM departments;
SELECT * FROM titles;
SELECT * FROM employees;
SELECT * FROM salaries;
SELECT * FROM dept_manager;
SELECT * FROM dept_emp;


--TODO 1: List the following details of each employee: employee number, last name, first name, sex, and salary.

SELECT
	a.emp_no,
	a.last_name,
	a.first_name,
	a.sex,
	b.salary
FROM employees AS a
JOIN salaries AS b
ON a.emp_no = b.emp_no;

-- TODO 2: List first name, last name, and hire date for employees who were hired in 1986.

SELECT 
	first_name,
	last_name,
	hire_date
FROM employees 
WHERE hire_date BETWEEN '1986-01-01' and '1986-12-31'
ORDER BY hire_date DESC ;


-- TODO 3: List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.

SELECT 
	departments.dept_no,
	departments.dept_name,
	dept_manager.emp_no,
	employees.last_name,
	employees.first_name
FROM departments
JOIN dept_manager
ON departments.dept_no = dept_manager.dept_no
JOIN employees
ON dept_manager.emp_no = employees.emp_no;

-- TODO 4: List the department of each employee with the following information: employee number, last name, first name, and department name.

SELECT 
	employees.emp_no,
	employees.last_name,
	employees.first_name,
	departments.dept_name
FROM employees
JOIN dept_emp
ON employees.emp_no = dept_emp.emp_no
JOIN  departments ON departments.dept_no = dept_emp.dept_no;

-- TODO 5:List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."

SELECT
	first_name,
	last_name,
	sex
FROM employees
WHERE first_name = 'Hercules'
AND last_name like 'B%';

-- TODO 6: List all employees in the Sales department, including their employee number, last name, first name, and department name.

SELECT
	dept_emp.emp_no,
	employees.last_name,
	employees.first_name,
	departments.dept_name
FROM employees
JOIN dept_emp
ON dept_emp.emp_no = employees.emp_no
JOIN departments
ON dept_emp.dept_no = departments.dept_no
WHERE departments.dept_name ='Sales';

-- TODO 7: List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.

SELECT
	dept_emp.emp_no,
	employees.last_name,
	employees.first_name,
	departments.dept_name
FROM employees
JOIN dept_emp
ON dept_emp.emp_no = employees.emp_no
JOIN departments
ON dept_emp.dept_no = departments.dept_no
WHERE departments.dept_name IN ('Sales','Development');
 
-- TODO 7: List the frequency count of employee last names (i.e., how many employees share each last name) in descending order.

SELECT DISTINCT last_name,
COUNT(last_name) as frequency_count
FROM employees
GROUP BY last_name
ORDER BY frequency_count DESC;

SQL_Challenge_NWU


