# SQL-Basics
SQL Basics

CREATE TABLE student (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) DEFAULT 'undecided'

);

DESCRIBE student;

ALTER TABLE student ADD gpa DECIMAL(3, 2);

ALTER TABLE student DROP COLUMN gpa;

INSERT INTO student (name, major) VALUES('Vivian', 'Data science');
INSERT INTO student (name, major) VALUES('Sharon', 'Marketing');
INSERT INTO student (name, major) VALUES('Jesse', 'Aviation');
INSERT INTO student (name, major) VALUES('Amy', 'Software Engineering');
INSERT INTO student (name, major) VALUES ('Claire', 'Chemistry');
INSERT INTO student (name, major) VALUES('Vivian', 'Statistics');
INSERT INTO student (name)VALUES('Jack');

SELECT * FROM student;

DROP TABLE student;


UPDATE student
SET major = 'DS'
WHERE major = 'Data Science';

UPDATE student
set major = 'Engineering'
WHERE major = 'Software Engineering' OR major= 'Aviation';


DELETE FROM student
WHERE student_id = 5;



SELECT student.name, student.major 
FROM student
ORDER BY name DESC;

SELECT * FROM student
ORDER BY major DESC
LIMIT 2;

SELECT * FROM student
WHERE major = 'Engineering' OR major = 'Marketing';

SELECT * FROM student
WHERE major <> 'Engineering';

SELECT * FROM student
WHERE student_id <= 4 AND name <> 'Sharon';

SELECT * FROM student
WHERE name IN ('Jesse', 'Amy', 'Sharon');

SELECT * FROM student;
