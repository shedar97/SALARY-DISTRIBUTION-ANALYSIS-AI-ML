Thursday, October 10, 2024



SALARY DISTRIBUTION ANALYSIS
AI/ML SALARIES 



Objective : Analyze the distribution of salaries across different job roles experience levels , and , Locations  

SQL Queries use GROUP BY and ORDER to calculate average, minimum and maximum salaries by job role.



To create a Salary Distribution Analysis using Microsoft Excel and SQL in Microsoft SQL Server Express, we will break the process into two main tasks:
SQL Analysis: Use SQL to analyze the salary distribution, focusing on calculating the average, minimum, and maximum salaries by job role, experience level, and location.
Excel Visualization: Use Excel to create visual representations (charts, histograms) to better understand the salary distribution.
Part 1: SQL Queries for Salary Distribution Analysis
In SQL, you will perform an analysis to group data by job role, experience level, and location. You will use aggregate functions like AVG(), MIN(), and MAX() to calculate salary statistics.
Assumptions:
Table Name: salaries
Columns:
job_role (job title or role of the employee)
experience_level (e.g., "Junior", "Mid", "Senior")
location (the location of the employee)
salary (the salary of the employee)




-- Analyzing salary distribution by job role, experience level, and location
SELECT 
    job_role,
    experience_level,
    location,
    AVG(salary) AS average_salary,
    MIN(salary) AS min_salary,
    MAX(salary) AS max_salary
FROM salaries
GROUP BY 
    job_role, 
    experience_level, 
    location
ORDER BY 
    job_role, 
    experience_level, 
    location;

