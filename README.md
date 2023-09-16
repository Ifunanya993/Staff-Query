# STAFF QUERY

## INTRODUCTION
Structured Query Language (SQL) is a data analysis tool use to store, organise and analyze data.
Query is a question or inquiry about a set of data. We use Structured Query Language (SQL) to
retrieve meaningful and relevant information from databases.
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

We also have function key which is linked to primary key


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

### TO CREATE DATABASE 'STAFF'

USE CODE

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

-----------------------------

## Task Two

using the ANSWER from TASK ONE, solve the following problem:

* Rename the tables Employee_info and Employee_Salary
  
* Change the ID columns to Employee_ID
  
* Create a new column in the Employee_Salary named Department
  
* For Employees with following IDs, update their Department with the one specified
   - 1, 3, 7 - IT
   - 2, 5, 9 - Advertising
   - 4, 6, 8, 10 - Communicating
     
* Change the data type of the IDs in both columns to Text data type

* Run a query that returns the Months, Day and year each employee came into the company

* Run a query that adds 10 years to the year the employees came into the company as their
  year_Of_Exit.


## ANSWER

### TO RENAME THE TABLES STAFF_INFO TO EMPLOYEE_INFO

 USE CODE:

 ALTER TABLE Staff_info

 RENAME EMPLOYEE_INFO; and execute , the table name will change.

### TO RENAME THE TABLE STAFF_SALARY TO EMPLOYEE_SALARY

 USE CODE:

 ALTER TABLE Staff_salary

 RENAME EMPLOYEE_INFO; and execute, it will change


### TO CHANGE ID COLUMN TO EMPLOYEE_ID 

 USE CODE: 

 ALTER TABLE Employee_info

 CHANGE COLUMN ID EMPLOYEE_ID (INT);


### TO CREATE A COLUMN NAMED DEPARTMENT

USE CODE:

ALTER TABLE Employee_salary

ADD COLUMN DEPARTMENT VARCHAR (50); and execute.


### UPDATE ID EMPLOYEE WITH DEPARTMENTS

USE CODE:

UPDATE Employee_salary

SET Department = 

CASE

WHEN Employee_ID = 1 THEN IT

WHEN Employee_ID = 3 THEN IT

WHEN Employee_ID = 7 THEN IT

WHEN Employee_ID = 2 THEN Advertising

WHEN Employee_ID = 5 THEN Advertising

WHEN Employee_ID = 9 THEN Advertising

WHEN Employee_ID = 4 THEN Communication

WHEN Employee_ID = 6 THEN Communication

WHEN Employee_ID = 8 THEN Communication

WHEN E mployee_ID = 10 THEN Communication

END; and execute. the IDs and Department in employee_salary table will be updated.


### TO CHANGE THE IDs DATA TYPE IN THE COLUMN TO TEXT

USE CODE:

ALTER TABLE Employee_info

MODIFY COLUMN Employee_ID VARCHA (50);


ALTER TABLE Employee_salary

MODIFY COLUMN Employee_ID VARCHA (50);


### TO RUN A QUERY THAT RETURN MONTH, DAY AND YEAR EMPLOYEE CAME INTO THE COMPANY

##### FOR MONTH OF ENTRY

USE CODE:

ALTER TABLE Employee_info

ADD COLUMN month_of_entry Varchar (50);

and execute, it will create a column for month_of_entry.


UPDATE enployee_info

SET MONTH_OF_ENTRY = MONTHNAME(DATE_OF_ENTRY);

and execute, it will return only the month of entry.


#### FOR DAY

USE CODE:

ALTER TABLE Employee_info

ADD COLUMN day_of_entry varchar (50);

and execute, it will create a column for day of entry.


UPDATE employee_info

SET DAY_OF_ENTRY = DAYNAME(DATE_OF_ENTRY);

and execute, it will return only the day of entry.


#### FOR YEAR

USE CODE:

ALTER TABLE Employee_info

ADD COLUMN Year_of_entry varchar (50);

and execute, it will create a column for year of entry.


UPDATE Employee_info

SET year_of_entry = year(DATE_OF_ENTRY);

and execute, it will return only the year of entry.



### TO RUN A QUERY THAT RETURN YEAR_OF_EXIT IN 10 YEARS INTERVAL

USE CODE:

ALTER TABLE Employee_info

ADD COLUMN YEAR_OF_EXIT DATE;

and execute, it will create a column for year_of_entry.



UPDATE Employee_info

SET YEAR_OF_EXIT = DATE_ADD(DATE_OF_ENTRY,INTERVAL 10 YEAR);

and execute, it will return a year of exit in 10 years.  

------------------------

## INCONCLUSION
SQL is one of the most useful tools use to work on a multi database as it can take up to 5000
rows. it can sort and filter out any specific information in a database.

