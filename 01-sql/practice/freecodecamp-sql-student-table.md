/*
====================================================
Title: SQL Tutorial for Beginners
Source: freeCodeCamp.org
Instructor: Mike Dane

Video Progress: ~1 hour 48 minutes
Date Completed: YYYY-MM-DD

Concepts Covered:
- CREATE TABLE
- DROP TABLE
- PRIMARY KEY
- AUTO_INCREMENT
- NOT NULL
- UNIQUE
- DEFAULT
- INT
- VARCHAR
- INSERT
- SELECT

Description:
Creating tables, defining columns and constraints,
and inserting and retrieving data from a database.

====================================================
*/
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
