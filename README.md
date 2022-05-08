# Pewlett-Hackard-Analysis
Using PostgreSQL to analyze data.

## Overview of the analysis

Human Resources records for a huge agency with quite a few employees growing old into retirement. As far as the data source, There are six CSV files that are been supplied as records to load into the database tables that were created in PostgreSQL. The records include worker statistics indexed in diverse tables and the database is constructed as proven with the ERD image shown below which is used as a base to illustrate diverse SQL dataflow techniques.

![ERD](/images/EmployeeDB.png)

## Resources

- PostgreSQL / pgAdmin4
  - [PG ADMIN DOCUMENTAION](https://www.postgresql.org/docs/)

## Results Deliverable 1

After joining multiple tables (employee, titles, salaries) and using filters to get the right employee demographics that were requested, The instructions walk you through the use of partitioning the data and how to find and remove unwanted duplicate rows. 

### Employee data mart with duplicates

![Data](/images/retirement_tittles.png)

### Employee data mart without duplicates

![Data](/images/unique_tittles.png)

![Data](/images/employee_tittle.png)

## Results Deliverable 2

In this challenge, I created a mentorship-eligibility table that holds the current employees who were born between January 1, 1965, and December 31, 1965.

![Data](/images/mentorship_eligibilty.png)

## Results Overall

- When you have related tables you often have one-to-many or many-to-many relationships. So when you join to TableB each record in TableA many have multiple records in TableB. This is normal and expected.

- Now at times you only need certain columns and those are all the same for all the records, then you would need to do some sort of group by or distinct to remove the duplicates.

-  When wanting to use different tables (employee, titles, salaries) in one datamart we join the tables together because it's a way to work with more than one table. SQL JOIN will allow you to combine data from two or more tables within one SQL.

- WHERE clause is used to pull data using a condition requested by the data user. For example: Filtering the data on the birth_date column to retrieve the employees who were born between 1952 and 1955. 

## Summary:

How many roles will need to be filled as the "silver tsunami" begins to make an impact?
  - 90,398 roles are in urgent need to be filled out as soon as the workforce starts retiring at any given time.
  
Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
  - No, We have 1,940 employees who are eligible to participate in a mentorship program.
