# SQL Queries: Database Validation & Data Testing Practice

## 📌 Project Overview

This project demonstrates my proficiency in **SQL for Database Validation**, a core competency for any QA Engineer. The ability to query databases directly allows for verification of data integrity, testing of back-end logic, and ensuring that the information shown on the UI matches the stored records.

In these tasks, I utilized: \* **Conditional Filtering:** `IN`,
`BETWEEN`, `LIKE`, `NOT LIKE`. \* **Aggregate Functions:** `AVG`,
`COUNT`, `MAX`, `MIN`. \* **Data Organization:** `GROUP BY`, `ORDER BY`,
`DISTINCT`. \* **Table Joins/Manipulation:** String concatenation and
column aliasing.

------------------------------------------------------------------------

## 📑 SQL Task Suite

### 1. Customer & Location Analysis
[Database](https://imgur.com/a/iaQyphD)

**Task:** Identify specific customer segments based on their geographic
location.

**Show the full names of customers from Prague and Oslo**

``` sql
SELECT (FirstName || ' ' || LastName) AS FullName
FROM customers
WHERE city IN ('Oslo', 'Prague');
```

**Show all unique countries where customers are located**

``` sql
SELECT DISTINCT country
FROM customers;
```

**Count the number of customers by country**

``` sql
SELECT country, COUNT(*) AS customer_count
FROM customers
GROUP BY country;
```

------------------------------------------------------------------------

### 2. Media & Track Validation
[Database](https://imgur.com/a/0tl36Oc)

**Task:** Perform statistical analysis and data retrieval on track
inventory.

**Calculate the average duration of a track**

``` sql
SELECT AVG(milliseconds)
FROM tracks;
```

**Count the number of tracks that do not have a composer listed**
[Database]()

``` sql
SELECT COUNT(*)
FROM tracks
WHERE composer IS NULL;
```

**Find the longest track**

``` sql
SELECT *
FROM tracks
ORDER BY milliseconds DESC
LIMIT 1;
```

**Find the shortest track**

``` sql
SELECT MIN(milliseconds) AS shortest_track
FROM tracks;
```

**Select all tracks where the composer is Angus Young**

``` sql
SELECT *
FROM tracks
WHERE composer = 'Angus Young';
```

------------------------------------------------------------------------

### 3. Content Management System (CMS) Testing
[Database](https://i.imgur.com/kKUemhu.png)

**Task:** Verify article metadata and user account status within a CMS
database.

**Select article titles where the author ID is 2**

``` sql
SELECT title
FROM article
WHERE author_id = 2;
```

**Select article titles where the author ID is not 1**

``` sql
SELECT title
FROM article
WHERE author_id != 1;
```

**Select articles created between 2020-09-21 and 2020-10-10**

``` sql
SELECT *
FROM article 
WHERE createdAt BETWEEN '2020-09-21' AND '2020-10-10';
```

**Select articles where the title contains the word "test"**

``` sql
SELECT *
FROM article
WHERE title LIKE '%test%';
```

**Select articles where the slug contains "test" and the author ID is
1**

``` sql
SELECT *
FROM article
WHERE slug LIKE '%test%' AND author_id = 1;
```

------------------------------------------------------------------------

### 4. User & Employee Profile Validation

**Task:** Search and validate email formats and HR records.

**Select users whose email is not a Gmail account**
[Database](https://i.imgur.com/jdKjCVo.png)

``` sql
SELECT *
FROM users
WHERE email NOT LIKE '%gmail.com';
```

**Show customers who use Gmail**
[Database](https://imgur.com/a/iaQyphD)]
``` sql
SELECT *
FROM customers
WHERE email LIKE '%gmail.com';
```

**Show all 'Sales Support Agents' with the last name 'Park'**
[Database](https://imgur.com/a/jZbNm9B)

``` sql
SELECT *
FROM employees
WHERE title = 'Sales Support Agent' AND lastName = 'Park';
```

**Show all employees born in the 1960s**
[Database](https://imgur.com/a/jZbNm9B)

``` sql
SELECT *
FROM employees
WHERE birthDate BETWEEN '1960-01-01' AND '1969-12-31';
```

------------------------------------------------------------------------

**Created by Alina Kuliak**
