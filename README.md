# STAFF QUERY

## INTRODUCTION
Structured Query Language (SQL) is a data analysis tool use to store, organise and analyze data.
Query is a question or inquiry about a setof data. We use Structured Query Language (SQL) to
retrieve meaninful and relevant information from databases.
When building a structure , we pull data from tables and fields .The fields are the columns in the 
database table, while the actual data makes up the rows.
Every programming language includuing SQL follows a guidelines known as syntax.

### SYNTAX 
It is a predetermined structure language that includes all required words, symbols and
punctuation, as well as their proper placement.

The syntax of every SQL query is the same.

### SELECT 
We use SELECT to choose the columns you want to return.
### FROM
We use FROM to choose the tables where the columns you want to locate.
### WHERE
We use WHERE to filter for certain information.

 A SQL query is like filling a template. It is helpful to start a query by writing the SELECT, FROM
 and WHERE keywords in the following format:

### SELECT
### FROM
### WHERE

In SQL, we have primary keys which consist of constraints:
AI (Auto_Increment

TEXT (VARCHAR)(50)

NUMBER (INTEGER)

DATE ( DEFAULT IF NO DATE IS GIVING)

UNIQUE ( NO DUPLICATE)


----------------------------

## Task One

* Create a database named 'Staff'

* Create the following tables with at least 4 constraints for each :

  - Staff_info ( ID PK, Name, Age, DOE, Contract_Duration)
  - Staff_Salary ( ID PK, Salary, Yearly_Increment)
    
* Insert 10 rows of information into both tables
  
* Return the Name and Age of the Staffs
  
* Return the ID and Salary of the Staffs.

## Answer

### TO CREATE DATABASE 'STAFF' USE CODE

CREATE DATABASE staff;

and execute.

### TO CREATE STAFF_INFO TABLE

USE staff;

CREAT TABLE staff_info (ID PRIMARY KEY AUTO_INCREMENT, NAME  VARCHAR (50) UNIQUE, AGE (INT), DOE DATE,
CONTRACT_DURATION VARCHAR (50)); 

and execute .

A Table staff_info will be created.

using the syntax to insert the values accordingly and execute .

### TO CREATE STAFF_SALARY

USE staff;

CREATE TABLE staff_salary ( ID PRIMARY KEY AUTO_INCREMENT, SALARY INT, YEARLY_INCREMENT INT); and
execute.

A Table Staff_salary will be created.

Using the syntax to insert the values accordingly.


### TO RETURN NAME AND AGE

USE staff;

SELECT NAME,AGE

FROM Staff_info; and execute

It will bring out the Age and Name column from the table.


### TO RETURN ID AND SALARY

USE staff;

SELECT ID , SALARY

FROM Staff_salary; and  execute 

It will bring out the ID and salary column from Staff_salary table.

## INCONCLUSION
SQL is one of the most usefull tools use to work on a multi database as it can take up to 5000
rows. it can sort and filter out any specific information in a database.

