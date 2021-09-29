

/*
*The SQL CREATE DATABASE Statement
*The CREATE DATABASE statement is used to create a new SQL database.
*/
CREATE DATABASE DB_Name;

/*
*The SQL SHOW DATABASE Statement
*SHOW DATABASES is used to view existing databases
*/

SHOW DATABASES;

/*
*The SQL DROP DATABASE Statement
*The DROP DATABASE statement is used to drop an existing SQL database.
*/
DROP DATABASE DB_Name;

/*
*The SQL BACKUP DATABASE Statement
*The BACKUP DATABASE statement is used in SQL Server to create a full back up of an existing SQL database.
*/

BACKUP DATABASE DB_Name
TO DISK = 'FilePath';
 
/*
*The SQL BACKUP WITH DIFFERENTIAL Statement
*A differential back up only backs up the parts of the database that have changed since the last full database backup.
*/

BACKUP DATABASE DB_Name
TO DISK = 'FilePath'
WITH DIFFERENTIAL;

/*
*The SQL CREATE TABLE Statement
*The CREATE TABLE statement is used to create a new table in a database.
*/

CREATE TABLE TableName(
    ColumnName datatype,
    ColumnNane datatype,
    ColumnName datatype
);

/*
*Create Table Using Another Table
*A copy of an existing table can also be created using CREATE TABLE.
*The new table gets the same column definitions. All columns or specific columns can be selected.
*If you create a new table using an existing table, the new table will be filled with the existing values from the old table.
*/

CREATE TABLE TableName_1 AS
SELECT *
FROM TableName_1
WHERE Condition;

/*
*The SQL DROP TABLE Statement
*The DROP TABLE statement is used to drop an existing table in a database.
*/

DROP TABLE TableName;

/*
*SQL TRUNCATE TABLE
*The TRUNCATE TABLE statement is used to delete the data inside a table, but not the table itself.
*/

TRUNCATE TABLE TableName;

/*
*SQL ALTER TABLE Statement
*The ALTER TABLE statement is used to add, delete, or modify columns in an existing table.
*The ALTER TABLE statement is also used to add and drop various constraints on an existing table.
*/

--ADD COLUMN

ALTER TABLE TableName ADD ColumnName datatype;

--MODIFY COLUMN

ALTER TABLE TableName MODIFY COLUMN ColumnName datatype;

--DROP COLUMN

ALTER TABLE TableName DROP COLUMN ColumnName;

              /*SQL Constraints*/

/*
*SQL NOT NULL Constraint
*By default, a column can hold NULL values.
*The NOT NULL constraint enforces a column to NOT accept NULL values.
*This enforces a field to always contain a value, which means that you cannot insert a new record, or update a record without adding a value to this field.
*/

--SQL NOT NULL on CREATE TABLE
CREATE TABLE TableName(
    ColumnName datatype NOT NULL,
    ColumnName datatype NOT NULL
);

--SQL NOT NULL on ALTER TABLE
ALTER TABLE TableName 
MODIFY COLUMN ColumnName datatype NOT NULL;

/*
*SQL UNIQUE Constraint
*The UNIQUE constraint ensures that all values in a column are different.
*/

--SQL UNIQUE Constraint on CREATE TABLE

CREATE TABLE TableName (
    ColumnName datatype UNIQUE,
    ColumnName datatype UNIQUE,
);
 

CREATE TABLE TableName (
    ColumnName datatype,
    UNIQUE(ColumnName)
);

--To name a UNIQUE constraint, and to define a UNIQUE constraint on multiple columns, use the following SQL syntax:

CREATE TABLE TableName (
    ColumnName_1 datatype,
    ColumnName_2 datatype,
    ColumnName_3 datatype,
    CONSTRAINT UC_TableName UNIQUE(ColumnName_1, ColumnName_2, ColumnName_3)
);

/*SQL UNIQUE Constraint on ALTER TABLE*/
--To create a UNIQUE constraint on the column when the table is already created, use the following SQL:

ALTER TABLE TableName ADD UNIQUE(ColumnNane);

--To name a UNIQUE constraint, and to define a UNIQUE constraint on multiple columns, use the following SQL syntax:

ALTER TABLE TableName ADD CONSTRAINT UC_TableName UNIQUE(ColumnNane_1, ColumnNane_2, ColumnNane_3);

--DROP a UNIQUE Constraint

ALTER TABLE TableName DROP INDEX UC_TableName;

/*
*SQL PRIMARY KEY Constraint
*The PRIMARY KEY constraint uniquely identifies each record in a table.
*Primary keys must contain UNIQUE values, and cannot contain NULL values.
*A table can have only ONE primary key; and in the table, this primary key can consist of single or multiple columns (fields).
*/

CREATE TABLE TableName (
    ColumnNane datatype PRIMARY KEY,
    ColumnNane datatype
);

CREATE TABLE TableName (
    ColumnNane_1 datatype,
    ColumnNane_2 datatype,
    PRIMARY KEY(ColumnNane_1)
);

--To allow naming of a PRIMARY KEY constraint, and for defining a PRIMARY KEY constraint on multiple columns, use the following SQL syntax:

CREATE Table TableName (
    ColumnNane_1 datatype,
    ColumnNane_2 datatype, 
    ColumnNane_3 datatype,
    CONSTRAINT PK_TableName PRIMARY KEY(ColumnNane_1, ColumnNane_2)
);

/*SQL PRIMARY KEY on ALTER TABLE*/

--To create a PRIMARY KEY constraint on the column when the table is already created, use the following SQL:

ALTER TABLE TableName ADD PRIMARY KEY(ColumnNane);

--To allow naming of a PRIMARY KEY constraint, and for defining a PRIMARY KEY constraint on multiple columns, use the following SQL syntax:

ALTER TABLE TableName ADD CONSTRAINT PK_TableName PRIMARY KEY(ColumnNane_1, ColumnNane_2);

--DROP a PRIMARY KEY Constraint

ALTER TABLE TableName DROP PRIMARY KEY;

/*
*SQL FOREIGN KEY Constraint
*The FOREIGN KEY constraint is used to prevent actions that would destroy links between tables.
*A FOREIGN KEY is a field (or collection of fields) in one table, that refers to the PRIMARY KEY in another table.
*The table with the foreign key is called the child table, and the table with the primary key is called the referenced or parent table.
*The FOREIGN KEY constraint prevents invalid data from being inserted into the foreign key column, because it has to be one of the values contained in the parent table.
*/

--SQL FOREIGN KEY on CREATE TABLE
CREATE TABLE TableName_2 (
    ColumnNane_1 datatype FOREIGN KEY REFERENCES TableName_1(ColumnNane),
    ColumnNane_2
);

CREATE TABLE TableName_2 (
    ColumnNane_1 datatype,
    ColumnNane_2 datatype,
    ColumnNane_3 datatype,
    FOREIGN KEY (ColumnNane_2) REFERENCES TableName_1(ColumnNane)
);
--To allow naming of a FOREIGN KEY constraint, and for defining a FOREIGN KEY constraint on multiple columns, use the following SQL syntax:

CREATE TABLE TableName_2 (
    ColumnNane_1 datatype,
    ColumnNane_2 datatype,
    ColumnNane_3 datatype,
    CONSTRAINT FK_TableName_2 FOREIGN KEY (ColumnNane_1, ColumnNane_2) REFERENCES TableName_1(ColumnNane_1, ColumnNane_2)
);
--SQL FOREIGN KEY on ALTER TABLE

ALTER TABLE TableName_2 ADD FOREIGN KEY (ColumnNane_2) REFERENCES TableName_1(ColumnNane_1);

ALTER TABLE TableName_2 ADD CONSTRAINT FK_TableName_2 FOREIGN KEY (ColumnNane_1, ColumnNane_2) REFERENCES TableName_1(ColumnNane_1, ColumnNane_2);

--DROP a FOREIGN KEY Constraint

ALTER TABLE TableName DROP FOREIGN KEY FK_TableName_2;

/*
*SQL CHECK Constraint
*The CHECK constraint is used to limit the value range that can be placed in a column.
*If you define a CHECK constraint on a column it will allow only certain values for this column.
*If you define a CHECK constraint on a table it can limit the values in certain columns based on values in other columns in the row.
*/

--SQL CHECK on CREATE TABLE

CREATE TABLE TableName (
    ColumnNane_1 datatype CHECK(ColumnNane_1 > 10),
    ColumnNane_2 datatype CHECK(ColumnNane_2 <> "MAX_13"),
    ColumnNane_3 datatype CHECK(ColumnNane_3 <= 100)
);

CREATE TABLE TableName (
    ColumnNane_1 datatype,
    ColumnNane_2 datatype,
    ColumnNane_3 datatype,
    CHECK(ColumnNane_3 >= 25)
);

--To allow naming of a CHECK constraint, and for defining a CHECK constraint on multiple columns, use the following SQL syntax:

CREATE TABLE TableName (
    ColumnNane_1 datatype,
    ColumnNane_2 datatype,
    ColumnNane_3 datatype,
    CONSTRAINT CHK_TableName CHECK(ColumnNane_3 > 100 AND ColumnNane_2 < 500);
);

--SQL CHECK on ALTER TABLE

ALTER TABLE TableName ADD CHECK(ColumnNane >= 1000);

ALTER TABLE TableName ADD CONSTRAINT CHK_TableName CHECK(ColumnName_1 <> "MUK" AND ColumnName_2 >= 18;

--DROP a CHECK Constraint

ALTER TABLE TableName DROP CHECK CHK_TableName;

/*
*SQL DEFAULT Constraint
*The DEFAULT constraint is used to set a default value for a column.
*The default value will be added to all new records, if no other value is specified.
*/

--SQL DEFAULT on CREATE TABLE

CREATE TABLE TableName (
    ColumnName_1 datatype DEFAULT VALUE/*VALUE: INT, STR, DATE*/,
    ColumnName_2 datatype DEFAULT VALUE,
    ColumnName_3 datatype DEFAULT VALUE
);

--The DEFAULT constraint can also be used to insert system values, by using functions like GETDATE():


CREATE TABLE TableName (
    ColumnName_1 datatype,
    ColumnName_3 datatype DEFAULT GETDATE()
);
--SQL DEFAULT on ALTER TABLE

ALTER TABLE TableName ALTER COLUMN ColumnName SET DEFAULT VALUE;

--DROP a DEFAULT Constraint

ALTER TABLE TableName ALTER COLUMN ColumnName DROP DEFAULT;

/*
*SQL CREATE INDEX Statement
*The CREATE INDEX statement is used to create indexes in tables.
*Indexes are used to retrieve data from the database more quickly than otherwise. The users cannot see the indexes, they are just used to speed up searches/queries.
*Note: Updating a table with indexes takes more time than updating a table without (because the indexes also need an update). So, only create indexes on columns that will be frequently searched against.
*/

--Creates an index on a table. Duplicate values are allowed:

CREATE INDEX IndexName ON TableName (ColumnNane_1, ColumnNane_2, ColumnNane_3);

--Creates a unique index on a table. Duplicate values are not allowed:

CREATE UNIQUE INDEX IndexName ON TableName (ColumnNane_1, ColumnNane_2, ColumnNane_3);

--The DROP INDEX statement is used to delete an index in a table.

ALTER TABLE TableName DROP INDEX IndexName;

/*
*AUTO INCREMENT Field
*Auto-increment allows a unique number to be generated automatically when a new record is inserted into a table.
*Often this is the primary key field that we would like to be created automatically every time a new record is inserted.
*/

--SQL AUTO_INCREMENT on CREATE TABLE

CREATE TABLE TableName (
    ColumnNane_1 datatype AUTO_INCREMENT,
    ColumnNane_2 datatype
);

--To let the AUTO_INCREMENT sequence start with another value, use the following SQL statement:

ALTER TABLE TableName AUTO_INCREMENT = 55;

/*
*SQL CREATE VIEW Statement
*In SQL, a view is a virtual table based on the result-set of an SQL statement.
*A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database.
*You can add SQL statements and functions to a view and present the data as if the data were coming from one single table.
*A view is created with the CREATE VIEW statement.
*Note: A view always shows up-to-date data! The database engine recreates the view, every time a user queries it.
*/

--SQL CREATE VIEW Examples

CREATE VIEW [View Name] AS
SELECT ColumnNane_1, ColumnNane_2, ColumnNane_3 /*SELECT * */
FROM TableName
WHERE CONDITION;

/*
*Creat Tables
*/
--Employee Table
CREATE TABLE Employee (
    emp_id INT PRIMARY KEY,
    first_name VARCHAR(20),
    last_name VARCHAR(20),
    birth_date DATE,
    sex VARCHAR(1),
    salary INT,
    super_id INT,
    branch_id INT
);

--Creat Branch Table
CREATE TABLE Branch (
    branch_id INT PRIMARY KEY,
    branch_name VARCHAR(20),
    mgr_id INT,
    mgr_start_date DATE,
    FOREIGN KEY(mgr_id) REFERENCES Employee(emp_id) ON DELETE SET NULL
);

--Add Foreign Key For The Employee Table 
ALTER TABLE Employee ADD FOREIGN KEY(super_id) REFERENCES Employee(emp_id) ON DELETE SET NULL;
ALTER TABLE Employee ADD FOREIGN KEY(branch_id) REFERENCES Branch(branch_id) ON DELETE SET NULL;

--Create Client Table
CREATE TABLE Client (
    client_id INT PRIMARY KEY,
    client_name VARCHAR(20),
    branch_id INT,
    FOREIGN KEY(branch_id) REFERENCES Branch(branch_id) ON DELETE SET NULL
);

--Create Works_With Table
CREATE TABLE Works_With (
    emp_id INT,
    client_id INT,
    total_sales INT,
    CONSTRAINT PK_WorksWith PRIMARY KEY(emp_id, client_id),
    FOREIGN KEY(emp_id) REFERENCES Employee(emp_id) ON DELETE CASCADE,
    FOREIGN KEY(client_id) REFERENCES Client(client_id) ON DELETE CASCADE
);

--Create Branch Supplier Table
CREATE TABLE Branch_Supplier (
    branch_id INT,
    supplier_name VARCHAR(20),
    supply_type VARCHAR(20),
    CONSTRAINT PK_BranchSupplier PRIMARY KEY(branch_id, supplier_name),
    FOREIGN KEY(branch_id) REFERENCES Branch(branch_id) ON DELETE CASCADE
);

/*
* NOW INSERT DATA IN ALL TABLES
*/
-- Insert Data in Employee And Branch Tables
INSERT INTO Employee VALUES(100, 'David', 'Wallace', '1967-11-17', 'M', 250000, NULL, NULL);
INSERT INTO Branch VALUES(1, 'Corporate', 100, '2006-02-09');

UPDATE Employee
SET branch_id = 1
WHERE emp_id = 100;

INSERT INTO Employee VALUES(101, 'Jan', 'Levinson', '1961-05-11', 'F', 110000, 100, 1);

INSERT INTO Employee VALUES(102, 'Michael', 'Scott', '1964-03-15', 'M', 75000, 100, NULL);
INSERT INTO Branch VALUES(2, 'Scranton', 102, '1992-04-06');

UPDATE Employee
SET branch_id = 2
WHERE emp_id = 102;

INSERT INTO Employee VALUES(103, 'Angela', 'Martin', '1971-06-25', 'F', 63000, 102, 2), (104, 'Kelly', 'Kapoor', '1980-02-05', 'F', 55000, 102, 2), (105, 'Stanley', 'Hudson', '1958-02-19', 'M', 69000, 102, 2);

INSERT INTO Employee VALUES(106, 'Josh', 'Porter', '1969-09-05', 'M', 78000, 100, NULL);
INSERT INTO Branch VALUES(3, 'Stamford', 106, '1998-02-13');

UPDATE Employee
SET branch_id = 3
WHERE emp_id = 106;

INSERT INTO Employee VALUES(107, 'Andy', 'Bernard', '1973-07-22', 'M', 65000, 106, 3), (108, 'Jim', 'Halpert', '1978-10-01',  'M', 71000, 106, 3);
INSERT INTO branch VALUES(4, "Buffalo", NULL, NULL);

--Insert Data In Client Table
INSERT INTO Client VALUES(400, 'Dunmore Highschool', 2);
INSERT INTO Client VALUES(401, 'Lackawana Country', 2);
INSERT INTO Client VALUES(402, 'FedExl', 3);
INSERT INTO Client VALUES(403, 'John Daly Law, LLC', 3);
INSERT INTO Client VALUES(404, 'Scranton Whitepages', 2);
INSERT INTO Client VALUES(405, 'Times Newspaper', 3);
INSERT INTO Client VALUES(406, 'FedEx', 2);


--Insert Date For Works_With
INSERT INTO Works_With V(105, 400, 55000);
INSERT INTO Works_With (102, 401, 267000);
INSERT INTO Works_With (108, 402, 22500);
INSERT INTO Works_With (107, 403, 5000);
INSERT INTO Works_With (108, 403, 12000);
INSERT INTO Works_With (105, 404, 33000);
INSERT INTO Works_With (107, 405, 26000);
INSERT INTO Works_With (102, 406, 15000);
INSERT INTO Works_With (105, 406, 130000);

--Insert Date In Branch Supplier

INSERT INTO Branch_Supplier VALUES(2, 'Hammer Mill', 'Paper');
INSERT INTO Branch_Supplier VALUES(2, 'Uni-ball', 'Writing Utensils');
INSERT INTO Branch_Supplier VALUES(3, 'Patriot Paper', 'Paper');
INSERT INTO Branch_Supplier VALUES(2, 'J.T. Forms & Labels', 'Custom Forms');
INSERT INTO Branch_Supplier VALUES(3, 'Uni-ball', 'Writing Utensils');
INSERT INTO Branch_Supplier VALUES(3, 'Hammer Mill', 'Paper');
INSERT INTO Branch_Supplier VALUES(3, 'Stamford Labels', 'Custom Forms');

/*
*Now Omre Querys
*/


--We can query the view above as follows:

SELECT * FROM [View Name];


--SQL Updating a View
--A view can be updated with the CREATE OR REPLACE VIEW statement.

CREATE OR REPLACE VIEW [View Name] AS
SELECT * 
FROM TableName
WHERE CONDITION;

--SQL Dropping a View
--A view is deleted with the DROP VIEW statement.

DROP VIEW [View Name];

/*
*The SQL SELECT Statement
*The SELECT statement is used to select data from a database.
*The data returned is stored in a result table, called the result-set.
*/
--ALL COLUMN
SELECT * FROM Employee;
--3 COLUMN
SELECT first_name, last_name, salary
FROM Employee;

/*
*The SQL SELECT DISTINCT Statement
*The SELECT DISTINCT statement is used to return only distinct (different) values.
*Inside a table, a column often contains many duplicate values; and sometimes you 
only want to list the different (distinct) values.
*/
SELECT DISTINCT sex
FROM Employee;

SELECT DISTINCT sex, branch_id
FROM Employee;

SELECT DISTINCT sex, super_id, branch_id
FROM Employee;


/*
*The SQL WHERE Clause
*The WHERE clause is used to filter records.
*It is used to extract only those records that fulfill a specified condition.
*WHERE COLUMN_NAME (=, <>, >, >=, <, <=) VALUE;
*/

SELECT *
FROM Employee
WHERE sex = 'M';

SELECT salary
FROM Employee
WHERE salary > 200000;

/*
*The SQL AND, OR and NOT Operators
*The WHERE clause can be combined with AND, OR, and NOT operators.
*The AND and OR operators are used to filter records based on more than one condition:
*The AND operator displays a record if all the conditions separated by AND are TRUE.
*The OR operator displays a record if any of the conditions separated by OR is TRUE.
*The NOT operator displays a record if the condition(s) is NOT TRUE.
*/

SELECT * 
FROM Employee
WHERE sex = 'F' AND branch_id = 1;

SELECT * 
FROM Employee
WHERE sex = 'F' OR branch_id = 1;

SELECT * 
FROM Employee
WHERE sex = 'F' AND NOT branch_id = 1;

SELECT * 
FROM Employee
WHERE sex = 'F' AND (branch_id = 1 OR NOT super_id = 106);

/*
*The SQL ORDER BY Keyword
*The ORDER BY keyword is used to sort the result-set in ascending or descending order.
*The ORDER BY keyword sorts the records in ascending order by default. To sort the 
 records in descending order, use the DESC keyword.
*/

SELECT *
FROM Employee
ORDER BY salary;

SELECT *
FROM Employee
ORDER BY salary ASC;

SELECT *
FROM Employee
ORDER BY salary DESC;

SELECT *
FROM Employee
ORDER BY salary/*ASC*/, birth_date DESC;

/*
*What is a NULL Value?
*A field with a NULL value is a field with no value.
*If a field in a table is optional, it is possible to insert a new record or update 
a record without adding a value to this field. Then, the field will be saved with a NULL value.
*Note: A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!
*How to Test for NULL Values?
It is not possible to test for NULL values with comparison operators, 
such as =, <, or <>.
*We will have to use the IS NULL and IS NOT NULL operators instead.
*/

SELECT *
FROM Employee
WHERE super_id IS NULL;

SELECT *
FROM Employee
WHERE super_id IS NOT NULL;

/*
*The SQL DELETE Statement
The DELETE statement is used to delete existing records in a table.
*/

DELET FROM client
WHERE Client_id = 405;

DELETE FROM Employee
WHERE first_name = 'David';

/*
*The SQL LIMIT Clause
*The LIMIT clause is used to specify the number of records to return.
*The LIMIT clause is useful on large tables with thousands of records. 
Returning a large number of records can impact performance.
*/

SELECT * FROM Employee
LIMIT 5;

SELECT *
FROM Employee
ORDER BY salary DESC
LIMIT 1;

/*
*SQL Functions
*The MIN() function returns the smallest value of the selected column.
*The MAX() function returns the largest value of the selected column.
*The COUNT() function returns the number of rows that matches a specified criterion.
*The AVG() function returns the average value of a numeric column. 
*The SUM() function returns the total sum of a numeric column. 
*SELECT FUNCTION(COLUMN_NAME)
*/
SELECT MIN(salary) FROM Employee;
SELECT MAX(first_name) FROM Employee;
SELECT COUNT(salary) FROM Employee;
SELECT COUNT(*) FROM Employee;
SELECT SUM(salary) FROM Employee;
SELECT AVG(salary) FROM Employee;

/*
*The SQL LIKE Operator
*The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.
*The percent sign (%) represents zero, one, or multiple characters
*The underscore sign (_) represents one, single character
*/

SELECT * 
FROM Employee
WHERE first_name LIKE 'j__';

SELECT * 
FROM Employee
WHERE first_name LIKE 'M%l';

SELECT *
FROM Employee
WHERE first_name LIKE 'ke%';

/*
*The SQL IN Operator
*The IN operator allows you to specify multiple values in a WHERE clause.
*The IN operator is a shorthand for multiple OR conditions.
*/

SELECT *
FROM Employee
WHERE emp_id IN (100, 108, 399);

SELECT *
FROM Employee
WHERE emp_id NOT IN (100, 108, 399);

SELECT *
FROM Branch
WHERE mgr_id IN (
    SELECT emp_id FROM Employee
);

/*
*The SQL BETWEEN Operator
*The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.
*The BETWEEN operator is inclusive: begin and end values are included. 
*WHERE column_name BETWEEN value1 AND value2;
*/

SELECT *
FROM Employee
WHERE emp_id BETWEEN 100 AND 103;

SELECT * 
FROM Employee
WHERE first_name BETWEEN 'Jan' AND 'Josh';

SELECT *
FROM Employee
WHERE birth_date BETWEEN '1967-11-17' AND '1973-01-01';

/*
*SQL Aliases
*SQL aliases are used to give a table, or a column in a table, a temporary name.
*Aliases are often used to make column names more readable.
*An alias only exists for the duration of that query.
*An alias is created with the AS keyword.
*Aliases can be useful when:
1-There are more than one table involved in a query
2-Functions are used in the query
3-Column names are big or not very readable
4-Two or more columns are combined together
*/

SELECT first_name AS FN
FROM Employee;

SELECT first_name AS [F N]
FROM Employee;

SELECT CONCAT(first_name, ' ', last_name, ' :',  sex) AS NAMES
FROM Employee;

SELECT EMP.first_name, EMP.last_name
FROM Employee AS EMP;

/*
*SQL JOIN
*A JOIN clause is used to combine rows from two or more tables, based on a related column between them.
*Different Types of SQL JOINs
*Here are the different types of the JOINs in SQL:
1-(INNER) JOIN: Returns records that have matching values in both tables
2-LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
3-RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
4-FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table
*/

--INNER JOIN OR JOIN
SELECT Employee.first_name, Employee.last_name, Branch.branch_id
FROM Employee
INNER JOIN Branch ON Employee.emp_id = Branch.mgr_id;

SELECT Employee.first_name, Employee.last_name, Branch.branch_id
FROM Employee
JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--SQL LEFT JOIN Keyword
--Note: The LEFT JOIN keyword returns all records from the left table (TABLE 1), even if there are no matches in the right table (TABLE 2).

SELECT Employee.emp_id, Employee.first_name, Branch.branch_id
FROM Employee
LEFT JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--SQL RIGHT JOIN Keyword
--Note: The RIGHT JOIN keyword returns all records from the right table (TABLE 2), even if there are no matches in the left table (TABLE 1).

SELECT Employee.emp_id, Employee.first_name, Branch.branch_id
FROM Employee
RIGHT JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--SQL FULL OUTER JOIN Keyword
--Note: The FULL OUTER JOIN keyword returns all matching records from both tables whether the other table matches or not. So, if there are rows in "TABLE 1" that do not have matches in "TABLE 2", or if there are rows in "TABLE 2" that do not have matches in "TABLE 1", those rows will be listed as well.
--NO WORK IN MYSQL
SELECT Employee.emp_id, Employee.first_name, Branch.branch_id, Branch.branch_name
FROM Employee
FULL JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--SQL Self Join
--A self join is a regular join, but the table is joined with itself.

SELECT T1.first_name AS NAME_T1, T2.first_name AS NAME_T2, T2.branch_id
FROM Employee AS T1, Employee AS T2
WHERE T1.emp_id <> T2.emp_id AND T1.branch_id = T2.branch_id;

SELECT T1.first_name AS NAME_T1, T2.first_name AS NAME_T2, T2.super_id
FROM Employee AS T1, Employee AS T2 /*YOU CAN WRIET: Employee T1, Employee T2*/
WHERE T1.emp_id <> T2.emp_id AND T1.super_id = T2.super_id;

/*
*The SQL UNION Operator
*The UNION operator is used to combine the result-set of two or more SELECT statements.
1.Every SELECT statement within UNION must have the same number of columns
2.The columns must also have similar data types
3.The columns in every SELECT statement must also be in the same order
*UNION ALL Syntax:
-The UNION operator selects only distinct values by default. To allow duplicate values, use UNION ALL:
*/

SELECT first_name AS Name_Company
FROM Employee
UNION
SELECT branch_name
FROM Branch;

SELECT client_name FROM Client
UNION
SELECT supplier_name FROM Branch_Supplier;

SELECT client_name FROM client
UNION ALL
SELECT supplier_name FROM Branch_Supplier;

SELECT client_name AS Name, branch_id, 'Client' AS Type
FROM client
UNION
SELECT supplier_name, branch_id, 'Branch Supplier' /*'Branch Supplier' AS Type*/
FROM Branch_Supplier
ORDER BY Type; 

/*
*The SQL GROUP BY Statement
*The GROUP BY statement groups rows that have the same values into summary rows, 
like "find the number of customers in each country".
*The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG())
to group the result-set by one or more columns.
*/

SELECT branch_id
FROM Employee
GROUP BY branch_id;

SELECT branch_id, COUNT(emp_id)
FROM Employee
GROUP BY branch_id;

SELECT emp_id, SUM(total_sales)
FROM works_with
GROUP BY emp_id
ORDER BY SUM(total_sales) DESC;

SELECT client_id, SUM(total_sales) AS '$$$$'
FROM works_with
GROUP BY client_id
ORDER BY SUM(total_sales) DESC;

/*
*The SQL HAVING Clause
*The HAVING clause was added to SQL because the WHERE keyword cannot be used with 
aggregate functions.
*/

SELECT branch_id, COUNT(emp_id)
FROM Employee
GROUP BY branch_id
HAVING COUNT(emp_id) > 2;

SELECT emp_id, SUM(total_sales)
FROM works_with
GROUP BY emp_id
HAVING SUM(total_sales) < 130000
ORDER BY SUM(total_sales) DESC;

SELECT client_id, SUM(total_sales) AS '$$$$'
FROM works_with
GROUP BY client_id
HAVING SUM(total_sales) > 150000
ORDER BY SUM(total_sales) DESC;

/*
*The SQL EXISTS Operator
*The EXISTS operator is used to test for the existence of any record in a subquery.
*The EXISTS operator returns TRUE if the subquery returns one or more records.
*/

SELECT first_name, emp_id
FROM Employee
WHERE EXISTS (
    SELECT *
    FROM Branch
    WHERE Branch.mgr_id = Employee.emp_id
);

SELECT branch_id, client_name
FROM client
WHERE EXISTS(
    SELECT Branch.branch_id FROM Branch
    WHERE Branch.branch_id = 2 AND Branch.branch_id = Client.branch_id
);

SELECT client_name
FROM client
WHERE EXISTS(
    SELECT *
    FROM works_with
    WHERE works_with.client_id = Client.client_id AND  total_sales > 100000 
);

SELECT first_name
FROM Employee
WHERE EXISTS(
    SELECT *
    FROM works_with
    WHERE works_with.emp_id = Employee.emp_id AND works_with.total_sales >= 200000
);

/*
*The SQL SELECT INTO Statement
*The SELECT INTO statement copies data from one table into a new table.
*/

--COPY ALL COLUMNS IN THIS DATABASE

SELECT * INTO New_Table
FROM client;

--COPY ALL COLUMNS IN OTHER DATABASE

SELECT *
INTO New_Table IN 'OtherDB.mdb'
FROM works_with;

--COPY SOME COLUMNS IN THIS DATABASE

SELECT first_name, last_name, salary
INTO New_Table
FROM Employee;

--COPY SOME COLUMNS IN OTHER DATABASE

SELECT branch_name, branch_id
INTO New_Table IN 'OtherDB.mdb'
FROM Branch;

/*
*The SQL INSERT INTO SELECT Statement
*The INSERT INTO SELECT statement copies data from one table and inserts it into another table.
*The INSERT INTO SELECT statement requires that the data types in source and target tables matches.
*Note: The existing records in the target table are unaffected.
*/
--Copy all columns from one table to another table:

INSERT INTO table2
SELECT * FROM table1
WHERE condition; --OPTIONAL PHRASE

--Copy only some columns from one table into another table:

INSERT INTO table2 (column1, column2, column3, ...)
SELECT column1, column2, column3, ...
FROM table1
WHERE condition; --OPTIONAL PHRASE

/*
*The SQL CASE Statement
*The CASE statement goes through conditions and returns a value when the first 
condition is met (like an if-then-else statement). So, once a condition is true, 
it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause.
*If there is no ELSE part and no conditions are true, it returns NULL.
*/

SELECT emp_id, client_id, 
CASE
    WHEN total_sales > 100000 THEN 'A'
    WHEN total_sales < 100000 THEN 'B'
    ELSE 'AB'
END 
FROM works_with;

SELECT client_name, client_id, 
CASE
    WHEN branch_id = 1 THEN 'Branch 1'
    WHEN branch_id = 2 THEN 'Branch 2'
    ELSE 'Branch 3'
END AS Branch
FROM client;

SELECT *
FROM Employee
ORDER BY (
    CASE
        WHEN salary IS NULL THEN branch_id
        ELSE salary
    END
);

/*
*SQL NULL Functions
*The MySQL IFNULL() function lets you return an alternative value if an expression is NULL:
*or we can use the COALESCE() function, like this:
*/

SELECT branch_name, branch_id * IFNULL(mgr_id, 1)
FROM Branch;

SELECT branch_name, branch_id * COALESCE(mgr_id, 1)
FROM Branch;

SELECT branch_id, COALESCE(mgr_id, 1) * (branch_id + IFNULL(mgr_id, 0))
FROM Branch;

/*
MORE QUERY 
*/

-- Find a list of all clients & branch suppliers' names
SELECT client.client_name AS Non_Employee_Entities, client.branch_id AS Branch_ID
FROM client
UNION
SELECT branch_supplier.supplier_name, branch_supplier.branch_id
FROM branch_supplier;

SELECT 'Employee' AS Type, Employee.emp_id, Employee.first_name
FROM employee
UNION
SELECT 'Branch', branch_id, branch_name
FROM Branch;

SELECT 'Client' AS Type, Client.client_id AS ID, Client.client_name AS Name 
FROM client
UNION
SELECT 'Supplier' AS Type, Branch_Supplier.branch_id, Branch_Supplier.supplier_name
FROM Branch_Supplier;

/*
*Join
*/
--Join
SELECT Employee.emp_id, Employee.first_name, Branch.branch_name
FROM Employee
JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--Inner Join
SELECT Branch.branch_name AS Branch, Employee.first_name AS Mgr_Name
FROM Employee
INNER JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--Left Join
SELECT Employee.emp_id, Employee.first_name, Branch.branch_name
FROM Employee
LEFT JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--Right Join
SELECT Employee.emp_id, Employee.first_name, Branch.branch_name
FROM Employee
RIGHT JOIN Branch ON Employee.emp_id = Branch.mgr_id;

--Self Join
SELECT T1.emp_id, T1.first_name AS T1, T2.first_name AS T2, T2. super_id AS super
FROM Employee T1, Employee T2
WHERE T1.emp_id <> T2.emp_id AND T1.super_id = T2.super_id;

SELECT DISTINCT T1.first_name AS T1, T2.first_name AS T2, T2.branch_id
FROM Employee T1, Employee T2
WHERE T1.emp_id <> T2.emp_id AND T1.branch_id = T2.branch_id;

SELECT COUNT(emp_id), super_id
FROM Employee
GROUP BY super_id;

-- Find names of all employees who have sold over 50,000
SELECT *
FROM Employee
WHERE emp_id IN (
    SELECT emp_id
    FROM Works_With
    WHERE total_sales >= 50000
);

-- Find all clients who are handles by the branch that Michael Scott manages
SELECT emp_id
FROM Employee
WHERE first_name = 'Michael';

SELECT branch_id
FROM Branch
WHERE mgr_id = 102;

SELECT client_name
FROM client
WHERE Branch_ID = (
    SELECT branch_id
    FROM Branch
    WHERE mgr_id = (
        SELECT emp_id
        FROM Employee
        WHERE first_name = 'Michael'
));

-- Find the names of employees who work with clients handled by the scranton branch
SELECT employee.first_name, employee.last_name
FROM employee
WHERE employee.emp_id IN (
    SELECT works_with.emp_id
    FROM works_with
    )
AND employee.branch_id = 2;

-- Find the names of all clients who have spent more than 100,000 dollars
SELECT client.client_name
FROM client
WHERE client.client_id IN (
    SELECT client_id
    FROM (
        SELECT SUM(works_with.total_sales) AS totals, client_id
        FROM works_with
        GROUP BY client_id) AS total_client_sales
        WHERE totals > 100000
);

SELECT CLclient_name
FROM client
WHERE client_id IN (
    SELECT client_id
    FROM (
    SELECT client_id, SUM(Works_With.total_sales)
    GROUP BY Works_With.client_id
    HAVING SUM(Works_With.total_sales) > 50000)
);

SELECT client_id ,SUM(total_sales)
FROM Works_With
GROUP BY client_id
HAVING SUM(total_sales) > 50000;

-- Find names of all employees who have sold over 50,000
SELECT first_name, last_name
FROM Employee
WHERE emp_id IN (
    SELECT emp_id
    FROM(
        SELECT emp_id, SUM(total_sales)
        FROM Works_With
        GROUP BY emp_id
        HAVING SUM(total_sales) > 50000
    ) AS total_sales_for_employee
);

SELECT emp_id, SUM(total_sales)
FROM Works_With
GROUP BY emp_id
HAVING SUM(total_sales) > 50000;

-- Find all clients who are handles by the branch that Michael Scott manages
-- Assume you DONT'T know Michael's ID
SELECT CLclient_name
FROM client
WHERE ;

SELECT emp_id
FROM Employee
WHERE first_name = 'Michael';

SELECT branch_id
FROM Branch
WHERE mgr_id = 102;

SELECT client_name
FROM client
WHERE branch_id IN (
    SELECT branch_id
    FROM Branch
    WHERE mgr_id = (
        SELECT emp_id
        FROM Employee
        WHERE first_name = 'Michael')
) ;
--
SELECT client_id, SUM(total_sales)
FROM Works_With
GROUP BY client_id
ORDER BY SUM(total_sales) DESC
LIMIT 1;

SELECT client_name
FROM client
WHERE client_id = (
    SELECT client_id
    FROM (
        SELECT client_id, SUM(total_sales)
        FROM Works_With
        GROUP BY client_id
        ORDER BY SUM(total_sales) DESC
        LIMIT 1
    ) AS T
);

SELECT T1.client_name AS T1, T2.client_name AS T2, T2.branch_id AS Branch
FROM client AS T1, client AS T2
WHERE T1.client_id <> T2.client_id AND T1.branch_id = T2.branch_id;

SELECT T1.first_name AS Name_1, T2.first_name AS Name_2, T1.super_id AS ID
FROM Employee T1, Employee T2
WHERE T1.emp_id <> T2.emp_id AND T1.super_id = T2.super_id;

SELECT Client.client_name, Works_With.total_sales
FROM client
INNER JOIN Works_With ON Client.client_id = Works_With.client_id;

SELECT client_name, SUM(total_sales)
FROM(
    SELECT Client.client_name, Works_With.total_sales
    FROM client
    INNER JOIN Works_With ON Client.client_id = Works_With.client_id
) AS Client_Works_With
GROUP BY client_name;

SELECT client_id, SUM(total_sales)
FROM Works_With
GROUP BY client_id
ORDER BY SUM(total_sales) DESC;

SELECT client_name, branch_id
FROM client
WHERE client_id IN(
    SELECT client_id
    FROM (
        SELECT client_id, SUM(total_sales)
        FROM Works_With
        GROUP BY client_id
        ORDER BY SUM(total_sales) DESC
        LIMIT 1
    ) AS maxx
);

SELECT client.client_name, SUM(Works_With.total_sales)
FROM client
INNER JOIN Works_With ON client.client_id = Works_With.client_id
GROUP BY Works_With.client_id
ORDER BY SUM(Works_With.total_sales) DESC
LIMIT 1;

SELECT emp_id, SUM(total_sales)
FROM Works_With
GROUP BY emp_id
ORDER BY sum(total_sales) DESC
LIMIT 1;
SELECT first_name, last_name, emp_id
FROM Employee
WHERE emp_id = (
    SELECT emp_id
    FROM (
        SELECT emp_id, SUM(total_sales)
        FROM Works_With
        GROUP BY emp_id
        ORDER BY sum(total_sales) DESC
        LIMIT 1
    ) AS Works_With_ID
);

SELECT Employee.first_name, Employee.last_name, Works_With.emp_id, SUM(Works_With.total_sales)
FROM Employee
INNER JOIN Works_With ON Employee.emp_id = Works_With.emp_id
GROUP BY Works_With.emp_id
ORDER BY SUM(Works_With.total_sales) DESC
LIMIT 1;

SELECT first_name, last_name, branch_id
FROM Employee;

SELECT emp_id, COUNT(client_id)
FROM Works_With
GROUP BY emp_id
ORDER BY COUNT(client_id) DESC
LIMIT 1;

SELECT first_name, last_name, branch_id
FROM Employee
WHERE emp_id = (
    SELECT emp_id
    FROM (
        SELECT emp_id, COUNT(client_id)
        FROM Works_With
        GROUP BY emp_id
        ORDER BY COUNT(client_id) DESC
        LIMIT 1
    ) AS ID
);

SELECT Employee.first_name, Employee.last_name, Employee.branch_id, COUNT(Works_With.client_id)
FROM Employee
INNER JOIN Works_With ON Employee.emp_id = Works_With.emp_id
GROUP BY Employee.emp_id
ORDER BY COUNT(Works_With.client_id) DESC;
