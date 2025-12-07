# MySQL

MySQL is a very popular open-source relational database management system (RDBMS).

What is MySQL?

    MySQL is a relational database management system
    MySQL is open-source
    MySQL is free
    MySQL is ideal for both small and large applications
    MySQL is very fast, reliable, scalable, and easy to use
    MySQL is cross-platform
    MySQL is compliant with the ANSI SQL standard
    MySQL was first released in 1995
    MySQL is developed, distributed, and supported by Oracle Corporation.

Who Uses MySQL?

    Huge websites like Facebook, Twitter, Airbnb, Booking.com, Uber, GitHub, YouTube, etc.
    Content Management Systems like WordPress, Drupal, Joomla!, Contao, etc.
    A very large number of web developers around the world.


What is RDBMS?

RDBMS stands for Relational Database Management System.

RDBMS is a program used to maintain a relational database.

RDBMS is the basis for all modern database systems such as MySQL, Microsoft SQL Server, Oracle, and Microsoft Access.

What is a Database Table?

A table is a collection of related data entries, and it consists of columns and rows.

A column holds specific information about every record in the table.

A record (or row) is each individual entry that exists in a table.

What is SQL?

SQL is the standard language for dealing with Relational Databases.

SQL is used to insert, search, update, and delete database records.


Keep in Mind That...

    * SQL keywords are NOT case sensitive: select is the same as SELECT

    * Use semicolon at the end of each SQL statement.

Some of The Most Important SQL Commands

    SELECT - extracts data from a database
    UPDATE - updates data in a database
    DELETE - deletes data from a database
    INSERT INTO - inserts new data into a database
    CREATE DATABASE - creates a new database
    ALTER DATABASE - modifies a database
    CREATE TABLE - creates a new table
    ALTER TABLE - modifies a table
    DROP TABLE - deletes a table
    CREATE INDEX - creates an index (search key)
    DROP INDEX - deletes an index

MySQL SELECT Statement
----------------------
The following SQL statement selects the "CustomerName", "City", and "Country" columns from the "Customers" table.

SELECT CustomerName, City, Country FROM Customers;

The following SQL statement selects only the DISTINCT values from the "Country" column in the "Customers" table.

SELECT DISTINCT Country FROM Customers;

SELECT COUNT(DISTINCT Country) FROM Customers; 

MySQL WHERE Clause
------------------

The WHERE clause is used to filter records.
It is used to extract only those records that fulfill a specified condition.

The following SQL statement selects all the customers from "Mexico"

SELECT * FROM Customers
WHERE Country = 'Mexico'; 

Text Fields vs. Numeric Fields

SQL requires single quotes around text values (most database systems will also allow double quotes).
However, numeric fields should not be enclosed in quotes.

The following SQL statement selects a specific customer by ID

SELECT * FROM Customers
WHERE CustomerID = 1; 

<img width="1092" height="605" alt="image" src="https://github.com/user-attachments/assets/dbbd4cbe-42b7-4cf3-adeb-2fb11c7d0391" />

MySQL AND operator 
------------------
The following SQL statement selects all fields from "Customers" where country is "Germany" AND city is "Berlin"

select * from Customers 
where  Country="Germany" and  City="Berlin";

MySQL OR operator 
------------------
The following SQL statement selects all fields from "Customers" where city is "Berlin" OR "Stuttgart"

SELECT * FROM Customers
WHERE City = 'Berlin' OR City = 'Stuttgart';


MySQL NOT operator 
------------------
The following SQL statement selects all fields from "Customers" where country is NOT "Germany"

SELECT * FROM Customers
WHERE NOT Country = 'Germany';

Combining AND, OR and NOT
-------------------------
The following SQL statement selects all fields from "Customers" where country is "Germany" AND city must be "Berlin" OR "Stuttgart" (use parenthesis to form complex expressions)

SELECT * FROM Customers
WHERE Country = 'Germany' AND (City = 'Berlin' OR City = 'Stuttgart'); 

The following SQL statement selects all fields from "Customers" where country is NOT "Germany" and NOT "USA"

SELECT * FROM Customers
WHERE NOT Country = 'Germany' AND NOT Country = 'USA'; 


The MySQL ORDER BY Keyword
--------------------------
The ORDER BY keyword is used to sort the result-set in ascending or descending order.

The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword

ORDER BY Several Columns Example
--------------------------------
SELECT * FROM Customers
ORDER BY Country, CustomerName; 

MySQL INSERT INTO Statement
---------------------------
The INSERT INTO statement is used to insert new records in a table
<img width="1298" height="586" alt="image" src="https://github.com/user-attachments/assets/ce6fba2f-9a26-47cb-abb0-fe070bc16a30" />

NuLL Values
-----------
A field with a NULL value is a field with no value.

The following SQL lists all customers with a NULL value in the "Address" field.

SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;


Update
-------
he UPDATE statement is used to modify the existing records in a table.

The following SQL statement updates the first customer (CustomerID = 1) with a new contact person and a new city.

update Customers
set ContactName ='Shariful',City='Dhaka'
where CustomerID=1;


Delete
------
The DELETE statement is used to delete existing records in a table.

The following SQL statement deletes the customer "Alfreds Futterkiste" from the "Customers" table

DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';


Limit
-----
The LIMIT clause is used to specify the number of records to return.

The following SQL statement selects the first three records from the Customers" table.

SELECT * FROM Customers
LIMIT 3; 


MIN
---
The MIN() function returns the smallest value of the selected column.

The following SQL statement finds the price of the cheapest product

select MIN(price) as SobcheyeKomdami
from Products;


MAX
---
The following SQL statement finds the price of the most expensive product:

The following SQL statement finds the price of the most expensive product:

select MAX(price) as SobcheyeDami
from Products;
















