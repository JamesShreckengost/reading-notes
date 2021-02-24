# Reading Notes 8
# Sources: https://sqlbolt.com/, https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all


## Reading Notes
- To retrieve datat from a SQL database, we need to write a select statement, which are often referred to as queries. 
- A query is just a statement which declares what data we are looking for, where to find it , and how to trandsform it before it is returned.n
- Think of table in SQL as a type of an entity , and each row in that table as a specific instance of that ype
- the most basic query we could write would be one that slects for a couple columns of the table with all the rows
- The result of this query will be a two-dimensional set of rows and clumns, effectively a copy of the table, but onnly with the columns we requested.
- use * to select all

## otes from SQLBolt exercises
What is SQL? language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database
Popular SQL databases: SQLite, MySQL, Postgres, Oracle, Microsoft SQL Server
SQL databases are 2-dimensional tables aka spreadsheets
SELECT = query:
data we are looking for
where to find it in the database
(sometimes) how to transform it before returning it
When making queries you essentially communicate which data you want collected via rows and columns
* collects all data
filter = WHERE
SELECT * 
FROM mytable;
Queries with constraints 1
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
Operator	Condition	SQL Example
=, !=, < <=, >, >=	Standard numerical operators	col_name != 4
BETWEEN … AND …	Number is within range of two values (inclusive)	col_name BETWEEN 1.5 AND 10.5
NOT BETWEEN … AND …	Number is not within range of two values (inclusive)	col_name NOT BETWEEN 1 AND 10
IN (…)	Number exists in a list col_name IN	(2, 4, 6)
NOT IN (…)	Number does not exist in a list col_name NOT IN	(1, 3, 5)
Queries with constraints 2
Operator	Condition	Example
=	Case sensitive exact string comparison (notice the single equals)	col_name = “abc”
!= or <>	Case sensitive exact string inequality comparison	col_name != “abcd”
LIKE	Case insensitive exact string comparison	col_name LIKE “ABC”
NOT LIKE	Case insensitive exact string inequality comparison	col_name NOT LIKE “ABCD”
%	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)	col_name LIKE “%AT%” (matches “AT”, “ATTIC”, “CAT” or even “BATS”)
_	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)	col_name LIKE “AN_” (matches “AND”, but not “AN”)
IN (…)	String exists in a list	col_name IN (“A”, “B”, “C”)
NOT IN (…)	String does not exist in a list	col_name NOT IN (“D”, “E”, “F”)
Filtering and sorting Query results
DISTINCT removes duplicate rows

SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);
ORDER BY: sorts rows alpha-numerically

LIMIT: reduce the number of rows to return
OFFSET: specifies where to begin counting
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;
Inserting rows
INSERT

INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;
----------------------
INSERT INTO mytable
(column, another_column, …)
VALUES (value_or_expr, another_value_or_expr, …),
      (value_or_expr_2, another_value_or_expr_2, …),
      …;
Updating Rows
WHERE: for updating rows

UPDATE mytable
SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;
Deleting rows
DELETE FROM mytable
WHERE condition;
Creating tables
CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);
Altering tables
Adding Columns

ALTER TABLE mytable
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value
Removing Columns

ALTER TABLE mytable
DROP column_to_be_deleted;
Renaming

ALTER TABLE mytable
RENAME TO new_table_name;
Dropping tables
DROP TABLE IF EXISTS mytable;