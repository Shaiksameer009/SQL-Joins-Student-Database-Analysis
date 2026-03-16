# SQL-Joins-Student-Database-Analysis
SQL and Pandas analysis of a normalized student database demonstrating INNER JOIN, LEFT JOIN, multi-table joins, and data normalization concepts.

This project demonstrates how to work with a normalized relational database using SQL and Python. The assignment focuses on understanding database joins, normalization, and data analysis using Pandas.

# Project Overview

Student data is stored across three normalized tables:

- students – contains student information
- enrollments – contains course enrollment details
- grades – contains student scores for courses

These tables are connected using the **student_id** column.

The project shows how to combine and analyze data using SQL joins and Pandas.

# Technologies Used

- Python
- SQLite
- Pandas
- Google Colab

# Database Tables

# Students Table
| student_id | name | email | city |
|---|---|---|---|

# Enrollments Table
| enrollment_id | student_id | course_name | enrollment_date |

# Grades Table
| grade_id | student_id | course_name | score |

---

# Tasks Completed

# Task 1 – Basic Joins

# INNER JOIN

Retrieve student names and their enrolled courses.

# LEFT JOIN

Retrieve all students including those who are not enrolled in any course.


# Task 2 – Multiple Table Joins

Combine data from **students, enrollments, and grades** tables to display:

- Student name
- Course name
- Score


# Task 3 – Understanding Joins and Normalization

This section explains:

- Why database normalization is important
- When to use INNER JOIN
- When to use LEFT JOIN
- Pandas equivalent of SQL joins using `merge()`


# Pandas Integration

The project also demonstrates how to replicate SQL joins using Pandas:

```python
result = pd.merge(students_df, enrollments_df, on='student_id', how='left')
result = pd.merge(result, grades_df, on=['student_id','course_name'], how='left')
