use northwind;
use hr;
-- 1.Write a SQL query to find the number of employees hired in each year.
SELECT YEAR(hire_date) AS hire_year,
COUNT(*) AS num_employees_hired
FROM employees
GROUP BY YEAR(hire_date)
ORDER BY hire_year;



-- 2.Write a SQL query to find the number of employees in each department.
select department_id, count(*) as num_of_emp
from employees
group by department_id
order by num_of_emp;



--  3.Write a SQL query to find the department with the highest total salary.
select department_id,count(department_id) as no_emp,
sum(salary) as max_total_salary
from employees
group by department_id
order by max_total_salary desc;


--  4. Write a query to list the number of jobs available in the employees table.
select job_id,count(job_id) as no_emp
from employees
group by job_id
order by no_emp desc;


-- 5.Write a query to get the total salaries payable to employees.
select sum(salary) as total_salary
from employees;

-- 6. Write a query to get the minimum salary from the employees table.
select employee_id,count(employee_id) as no_emp,
min(salary) as min_salary
from employees
group by employee_id
order by min_salary;


-- 7. Write a query to get the maximum salary of an employee working as a Programmer. 
select job_title,
job_id,count(job_id) as noemp,
max_salary
from jobs
where job_title="Programmer"
group by job_id ;


-- 8. Write a query to get the average salary and number of employees working the department 90. 
select department_id,count(*) as no_emp,
avg(salary) as avg_sal
from employees
where department_id = 90
group by department_id;

-- 9. Write a query to get the highest, lowest, sum, and average salary of all employees. 
select max(salary) as max_sal,
min(salary) as min_sal,
sum(salary) as sum_sal,
avg(salary) as avg_sal
from employees;


-- 10. Write a query to get the number of employees with the same job
select job_id,count(job_id) as no_employee
from employees
group by job_id
order by no_employee desc;


-- 11. Write a query to get the difference between the highest and lowest salaries. 
select max(salary)-min(salary) as diff_salaries
from employees;


-- 12. Write a query to find the manager ID and the salary of the lowest-paid employee for that manager. 
select manager_id,count(manager_id) as no_mgr,
min(salary) as min_salary
from employees
group by manager_id
order by min_salary desc;

-- 13. Write a query to get the department ID and the total salary payable in each department.
select department_id,count(department_id) as no_emp,
sum(salary) as total_salary
from employees
group by department_id
order by total_salary;


-- 14. Write a query to get the average salary for each job ID excluding programmer. 

select job_id,count(job_id) as no_emp,
avg(salary) as avg_salary
from employees
where job_id != 'Programmer'
group by job_id;




-- 15. Write a query to get the total salary, maximum, minimum, average salary of employees (job ID wise), for department ID 90 only. 
select job_id,count(job_id) as count_job_id,
sum(salary) as total_salary,
max(salary) as max_salary,
min(salary) as min_salary,
avg(salary) as avg_salary
from employees
where department_id = 90
group by job_id;


-- 16. Write a query to get the job ID and maximum salary of the employees where maximum salary is greater than or equal to $4000.
select job_id,count(job_id) as cnt_job,
max(salary) as max_salary
from employees
group by job_id
having max_salary >= 4000
order by max_salary desc;



-- 17. Write a query to get the average salary for all departments employing more than 10 employees. 
select department_id,count(department_id) as no_emp,
avg(salary) as avg_salary
from employees
group by department_id 
having no_emp > 10
order by no_emp desc;
