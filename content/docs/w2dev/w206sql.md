---
title: "SQL"
description: ""
summary: ""
date: 2024-10-18T20:27:56+08:00
lastmod: 2024-10-18T20:27:56+08:00
weight: 206
draft: false
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### SQL

Relational Database Database

| SQL | Use Case | Description |
| - | - | - |
| PostgreSQL | Complex web app | Most functionality |
| MySQL | Simple web app | Oracle owned, widely supported, strict |
| SQLite | Mobile/Desktop/Embedded | Simple, minimal, no-concurrency |
| MS SQL Server | Microsoft enterprise stack | Integration with Microsoft |
| MariaDB | Open source MySQL alternative | PostgreSQL alternative |

### Concepts

| Concept | Description |
| - | - |
| Table | An entity or relation |
| Row | A tuple of record in table |
| Column | A field of attribute in table |
| Primary Key | A column that uniquely identify a row |
| Foreign Key | A column that references a row in another table |

- JSON as datatype for flexibility
- Secondary entity / relation in textbook are implemented into tables
- A M x N relation is made on a new table
- Keys are attributes that its value is unique
- Avoid modification anomalies
- Normalization forms are some throrical practice

### Syntax

```sql
-- Format

USE     <database schema>
SELECT  <attribute list, project operation>
FROM    <table list, cross product operation>
WHERE   <condition, select operation>
GROUP BY<grouping attributes>
HAVING  <condition after grouping>
ORDER BY<attributes>

```

#### Table

```sql
CREATE TABLE EMPLOYEE (
  DNAME VARCHAR(10) NOT NULL,
  DNUMBER INTEGER NOT NULL,
  SALARY FLOAT
  MGRSSN CHAR(9) NOT NULL DEFAULT '888665555',
  MGRSTARTDATE CHAR(10),
  PRIMARY KEY (DNUMBER),
  UNIQUE (DNAME),
  FOREIGN KEY (MGRSSN) REFERENCES EMPLOYEE(SSN)
  ON DELETE SET DEFAULT
  ON UPDATE CASCADE
);

DROP TABLE EMPLOYEE RESTRICT -- Cannot drop table with foreign key
DROP TABLE EMPLOYEE CASCADE -- Drop table with foreign key

ALTER TABLE EMPLOYEE ADD JOB VARCHAR(12) SET DEFAULT "Engineer";
```

#### Query

```sql
SELECT FNAME, LNAME FROM EMPLOYEE WHERE NOT EXISTS (SELECT * FROM DEPENDENT WHERE SSN=ESSN)

-- Retrieve department no, no of employee, avg salary of employee on which number of employee is more than one
SELECT DNO, COUNT (*), AVG (SALARY) FROM EMPLOYEE GROUP BY DNO

-- For each department that has more than five employees, retrieve the department number and the number of its employees who are making more than $40,000
SELECT DNO, COUNT(*) 
FROM EMPLOYEE 
WHERE SALARY > 40000 AND 
      DNO IN (SELECT DNO 
              FROM EMPLOYEE 
              GROUP BY DNO 
              HAVING COUNT(*) > 5 )
GROUP BY DNO
```

#### Update

```sql
INSERT INTO <table> (<attr1>, <attr2>, ...) VALUES ('char', 0, ...)

DELETE FROM <table> WHERE ...

UPDATE <table>  SET <attribute1>=<value1>, attribute2>=<value2>, .. WHERE ...
```
