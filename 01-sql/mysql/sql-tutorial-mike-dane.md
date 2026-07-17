# SQL Tutorial for Beginners Notes

**Source:** freeCodeCamp.org  
**Instructor:** Mike Dane

**Progress:** ~1 hour 48 minutes  
**Database:** MySQL  
**Environment:** Beekeeper Studio

---

# Overview

This tutorial introduces SQL fundamentals, relational databases, table creation, constraints, inserting data, and basic queries using MySQL.

---

# Databases

## Relational Databases

- Store data in **tables**
- Tables consist of **rows** and **columns**
- Tables can be related to one another through keys

## Non-Relational Databases

Other methods of storing data include:

- Documents
- Graphs
- Nodes

Database Management Systems (DBMS) exist for both relational and non-relational databases.

---

# SQL

**SQL (Structured Query Language)** is used to communicate with a Database Management System (DBMS).

Common tasks include:

- Creating databases
- Creating tables
- Retrieving data
- Updating data
- Deleting data
- Managing database objects

SQL syntax varies slightly between database systems such as MySQL and PostgreSQL.

---

# SQL Language Categories

| Category | Meaning |
|----------|---------|
| DQL | Data Query Language |
| DDL | Data Definition Language |
| DML | Data Manipulation Language |
| DCL | Data Control Language |

---

# Queries

A **query** is a request for information from a database.

Common query keywords:

- `SELECT`
- `FROM`
- `WHERE`

---

# Tables & Keys

## Primary Key

- Uniquely identifies each row
- Every table should have one primary key
- A table can only have one primary key

Example:

```sql
PRIMARY KEY (student_id)
```

---

## Surrogate Key

A key with no real-world meaning.

Example:

```text
student_id = 1
student_id = 2
student_id = 3
```

Often auto-generated.

---

## Natural Key

A key with real-world meaning.

Examples:

- Employee ID
- Social Security Number

---

## Foreign Key

References the primary key in another table.

Used to create relationships between tables.

A table may contain multiple foreign keys.

---

## Composite Key

A key made from two or more columns that together uniquely identify a record.

---

# Common Data Types

## INT

Stores whole numbers.

```sql
student_id INT
```

---

## DECIMAL(M,N)

Stores exact decimal numbers.

- **M** = total digits
- **N** = digits after the decimal

Example:

```sql
salary DECIMAL(8,2)
```

---

## VARCHAR(n)

Stores variable-length text.

Example:

```sql
name VARCHAR(20)
```

---

## BLOB

Stores binary data such as:

- Images
- Files
- Audio

---

## DATE

Stores dates.

```text
YYYY-MM-DD
```

---

## TIMESTAMP

Stores both date and time.

```text
YYYY-MM-DD HH:MM:SS
```

---

# Table Constraints

## PRIMARY KEY

Uniquely identifies each record.

```sql
PRIMARY KEY (student_id)
```

---

## AUTO_INCREMENT

Automatically generates the next numeric value.

```sql
student_id INT AUTO_INCREMENT
```

---

## DEFAULT

Assigns a default value when none is provided.

```sql
major VARCHAR(20) DEFAULT 'Undecided'
```

---

# SQL Statements Learned

## DROP TABLE

Deletes an existing table.

```sql
DROP TABLE student;
```

---

## CREATE TABLE

Creates a new table.

```sql
CREATE TABLE student (
    student_id INT AUTO_INCREMENT,
    name VARCHAR(20),
    major VARCHAR(20) DEFAULT 'Undecided',
    PRIMARY KEY (student_id)
);
```

---

## SELECT

Returns data from a table.

```sql
SELECT *
FROM student;
```

---

## INSERT

Adds new records to a table.

```sql
INSERT INTO student (name, major)
VALUES ('Jack', 'Bio');
```

```sql
INSERT INTO student (name)
VALUES ('Kate');
```

```sql
INSERT INTO student (name, major)
VALUES ('Mike', 'Comp Sci');
```

```sql
INSERT INTO student (name, major)
VALUES ('Jack', 'Bio');
```

```sql
INSERT INTO student (name, major)
VALUES ('Aven', 'Comp Sci');
```

---

# Practice Code

```sql
DROP TABLE student;

CREATE TABLE student (
    student_id INT AUTO_INCREMENT,
    name VARCHAR(20),
    major VARCHAR(20) DEFAULT 'Undecided',
    PRIMARY KEY (student_id)
);

SELECT *
FROM student;

INSERT INTO student (name, major)
VALUES ('Jack', 'Bio');

INSERT INTO student (name)
VALUES ('Kate');

INSERT INTO student (name, major)
VALUES ('Mike', 'Comp Sci');

INSERT INTO student (name, major)
VALUES ('Jack', 'Bio');

INSERT INTO student (name, major)
VALUES ('Aven', 'Comp Sci');
```
