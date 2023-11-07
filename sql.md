# SQL

https://hedgedoc.groot.rocks/s/qqTxYd3GL#

## MySQL Data Types

CHAR
```
String (0 - 255)
```
VARCHAR
```
String (0 - 255)
```
TINYTEXT
```
String (0 - 255)
```
TEXT
```
String (0 - 65535)
```
BLOB
```
String (0 - 65535)
```
MEDIUMTEXT
```
String (0 - 16777215)
```
MEDIUMBLOB
```
String (0 - 16777215)
```
LONGTEXT
```
String (0-4294967295)
```
LONGBLOB
```
String (0-4294967295)
```
TINYINT x
```
Integer (-128 - 127)
```
SMALLINT x
```
Integer (-32768 - 32767)
```
MEDIUMINT x
```
Integer (-8388608 - 8388607)
```
INT x
```
Integer (-2147­483648 to 214748­3647)
```
BIGINT x
```
Integer (-9223­372­036­854­775808 to 922337­203­685­477­5807)
```
FLOAT
```
Decimal (precise to 23 digits)
```
DOUBLE
```
Decimal (24 to 53 digits)
```
DECIMAL
```
"­DOU­BLE­" stored as string
```
DATE
```
YYYY-MM-DD
```
DATETIME
```
YYYY-MM-DD HH:MM:SS
```
TIMESTAMP
```
YYYYMM­DDH­HMMSS
```
TIME
```
HH:MM:SS
```
ENUM
```
One of preset options
```
SET
```
Selection of preset options
```
<br>
<br>

## Select queries

Select all columns
```
SELECT * FROM tbl;
```
Select some columns
```
SELECT col1, col2 FROM tbl;
```
Column alias with AS
```
SELECT col FROM tbl AS newname;
```
Select only unique records
```
SELECT DISTINCT FROM tbl WHERE condition;
```
Order results
```
SELECT * FROM tbl ORDER BY col [ASC | DESC];
```
Group results
```
SELECT col1, SUM(col2) FROM tbl GROUP BY col1;
```
<br>
<br>

## Creating and modifying

Create a database
```
CREATE DATABASE db_name;
```
Select a database
```
USE db_name;
```
List the databases on the server
```
SHOW DATABASES;
```
Show a table's fields
```
DESCRIBE tbl;
```
create a new table
```
CREATE TABLE tbl (field1, field2);
```
Insert data into a table
```
INSERT INTO tbl VALUES ("va­l1", "­val­2");
```
Delete a row
```
DELETE * FROM tbl WHERE condition;
```
Add a column from a table
```
ALTER TABLE tbl ADD COLUMN col;
```
Remove a column from a table
```
ALTER TABLE tbl DROP COLUMN col;
```
Make a column a primary key
```
ALTER TABLE tbl ADD PRIMARY KEY (col);
```
Return only 1 row matching query
```
... LIMIT = 1
```
Amend the values of a column
```
UPDATE table SET column­1="v­al1­" WHERE ...
```
Clear all the values, leaving the table structure
```
TRUNCATE TABLE tbl;
```
Delete the table
```
DROP TABLE tbl;
```
Delete the database
```
DROP DATABASE db_name;
```
<br>
<br>

## Matching data

Matching data using LIKE
```
SELECT * FROM tbl1 WHERE col LIKE ‘%value%’
```
Matching data using REGEX
```
SELECT * FROM tbl1 WHERE col RLIKE ‘regul­ar_­exp­res­sion’
```
<br>
<br>

## Joins

INNER JOIN
```
returns only where match in both tables
```
OUTER JOIN
```
also returns non-matching records from both tables
```
LEFT JOIN
```
also returns non-matching records from left table
```
RIGHT JOIN
```
also returns non-matching records from right table
```

#### JOIN syntax:
```
SELECT * FROM tbl1 INNER JOIN tbl2 ON tbl1.id = tbl2.id;
```
<br>
<br>

## String functions mySQL

Compare strings
```
STRCMP­("st­r1",­"­str­2")
```
Convert to lower case
```
LOWER(­"­str­")
```
Convert to upper case
```
UPPER(­"­str­")
```
Left trim
```
LTRIM(­"­str­")
```
Substring of a string
```
SUBSTR­ING­("st­r","i­nx1­"­,"in­x2")
```
Concatenate
```
CONCAT­("st­r1",­"­str­2")
```
<br>
<br>

## MySQL calculation functions

Count rows
```
COUNT(col)
```
Average
```
AVG(col)
```
Minimum value
```
MIN(col)
```
Maximum value
```
MAX(col)
```
Sum of values
```
SUM(col)
```
<br>
<br>

## Create table with auto-incrementing primary key

```
CREATE TABLE table_name (
id INT AUTO_I­NCR­EMENT,
column VARCHA­R(2),
column VARCHA­R(32),
PRIMARY KEY (id)
);
```