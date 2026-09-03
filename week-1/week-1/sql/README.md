# SQL notes

## Intro to databases

What's a database? = an organised system for storing and managing data so it can be reliably added, updated, looked up, and deleted, usually by an app running live.

Flat file database = stores data in plain text format, single table. Often csv, for a single topic with a small amount of data.

Relational database = SQL, contains tables that are related to one another in some way.

Non-relational database = NoSQL, none relational databases.

RDBMS = the program used to operate the database. Takes instructions and interprets them by creating tables, updating data, or accessing records. Popular RDBMS: MySQL, Oracle, PostgreSQL, SQLite, Microsoft SQL Server.

How are tables connected? = by a relational factor (a key).

Primary keys = identify each record in the table, e.g. ID. Must be unique, cannot be empty, cannot change. Can also be a foreign key. Simple (single column) or composite (multiple columns).

Foreign keys = used with primary keys to codify a relationship. Does not have to be unique. References the primary key from another table. RDBMS will prevent changes that would violate this.

Data redundancy = repeating the same data within a database.

## Data modelling

Three levels of a data model:
- Conceptual - broad level business understanding (entity names, entity relationships)
- Logical - structure of data elements and relationships, independent of the DBMS
- Physical - specific implementation depending on the RDBMS

ERD (entity relationship diagram) represents all the entities in the database. Each entity has attributes. Crow's foot notation describes relationships in more detail (e.g. an author can write many books, but each book has one author).

Violation of first normal form = repeated groups / more than one thing per cell ("not atomic").

## Querying & joins

SELECT [columns] FROM [table] WHERE [condition] GROUP BY [optional] HAVING [optional] ORDER BY [optional]

JOIN combines matched rows from two or more tables.
- INNER JOIN - rows with a matched key in both tables
- LEFT JOIN - everything from the left table
- RIGHT JOIN - everything from the right table

## Questions I've done

Data Storage & Design: ETL, ELT, ETL vs ELT, what is a database, the two main database types, data warehouse, data lake, how a database is structured, normalisation (pros/cons), junction tables, dimensional modelling, star vs snowflake schema.

SQL: what SQL is, database vs table, primary key, foreign key, SELECT statement, WHERE vs HAVING, COUNT(*) vs COUNT(column), NULL values, sorting data, types of joins, INNER JOIN vs LEFT JOIN.
