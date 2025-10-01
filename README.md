## Zakariya Shafi 596

# Project Overview

This project demonstrates basic OLAP (Online Analytical Processing) operations using Python.
It covers the three main OLAP approaches:

ROLAP (Relational OLAP – using SQL queries)

MOLAP (Multidimensional OLAP – using in-memory Pandas pivot tables)

HOLAP (Hybrid OLAP – combining SQL queries with Pandas aggregations)

In addition, the project implements slice, dice, drill-down, and roll-up operations with visualizations.

#Technologies Used

Python (for data manipulation and analysis)

Pandas (for in-memory data operations)

NumPy (for numerical calculations)

SQLite3 (for relational database storage)

Seaborn & Matplotlib (for data visualization)

Project Structure

The project is implemented in a single Python script that follows these steps:

Create and connect to a database (SQLite3)

Generate sample data (employees and departments tables)

Load data into SQLite database

Perform OLAP operations (ROLAP, MOLAP, HOLAP)

Demonstrate slice, dice, drill-down, and roll-up

Visualize results with charts and heatmaps

Key OLAP Operations Explained
ROLAP (Relational OLAP)

Uses SQL queries directly on the relational database.

Example in the project:

SELECT d.dept_name AS department, AVG(e.salary) AS avg_salary
FROM employees e
JOIN departments d ON e.dept_id = d.dept_id
GROUP BY d.dept_name;


Visualization: Bar chart showing average salary by department.

MOLAP (Multidimensional OLAP)

Uses Pandas pivot tables for in-memory cube-like aggregation.

Example: Create a cube of salary by department vs age.

Visualization: Heatmap showing aggregated salary across departments and age groups.

HOLAP (Hybrid OLAP)

Combines ROLAP (SQL queries) with MOLAP (pandas grouping).

Example:

SQL extracts detailed employee-department-salary data.

Pandas groups the data for summary by department.

Visualization: Bar chart of average salary by department.

OLAP Operations Demonstrated

Slice – Select a single dimension subset

Example: All employees from IT Department.

Dice – Select data based on multiple conditions

Example: Employees from HR with salary > 60,000.

Drill Down – Move from aggregated data to detailed level

Example: Salary by individual employees within departments.

Roll Up – Aggregate data to a higher level

Example: Total salary aggregated at the department level.

Visualizations

The project generates multiple plots:

ROLAP: Average salary by department (bar plot).

MOLAP: Salary cube heatmap (department × age).

HOLAP: Average salary by department (bar plot).

Drill Down: Salary by employee and department (grouped bar plot).

Roll Up: Total salary by department (bar plot).
