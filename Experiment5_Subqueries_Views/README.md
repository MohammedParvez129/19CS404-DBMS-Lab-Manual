# Experiment 5: Subqueries and Views

## AIM
To study and implement subqueries and views.

## THEORY

### Subqueries
A subquery is a query inside another SQL query and is embedded in:
- WHERE clause
- HAVING clause
- FROM clause

**Types:**
- **Single-row subquery**:
  Sub queries can also return more than one value. Such results should be made use along with the operators in and any.
- **Multiple-row subquery**:
  Here more than one subquery is used. These multiple sub queries are combined by means of ‘and’ & ‘or’ keywords.
- **Correlated subquery**:
  A subquery is evaluated once for the entire parent statement whereas a correlated Sub query is evaluated once per row processed by the parent statement.

**Example:**
```sql
SELECT * FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```
### Views
A view is a virtual table based on the result of an SQL SELECT query.
**Create View:**
```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name WHERE condition;
```
**Drop View:**
```sql
DROP VIEW view_name;
```

**Question 1**
--
-- Paste Question 1 here

```sql
Write a SQL query that retrieve all the columns from the table "Grades", where the grade is equal to the maximum grade achieved in each subject.

Sample table: GRADES



For example:

Result
student_id       student_name     subject          grade
---------------  ---------------  ---------------  ---------------
3                Charlie          Math             95
5                Emma             Science          92
7                John             Social           85
```

**Output:**

<img width="1282" height="805" alt="image" src="https://github.com/user-attachments/assets/9840c5ed-3008-4da3-9d92-a81792460b42" />

**Question 2**
---
-- Paste Question 2 here

```sql
Write a query to display all the customers whose ID is the difference between the salesperson ID of Mc Lyon and 2001.

salesman table

name             type
---------------  ---------------
salesman_id      numeric(5)
name                 varchar(30)
city                    varchar(15)
commission       decimal(5,2)

customer table

name         type
-----------  ----------
customer_id  int
cust_name    text
city         text
grade        int
salesman_id  int
 

For example:

Result
customer_id  cust_name    city        grade       salesman_id
-----------  -----------  ----------  ----------  -----------
3005         Graham Zusi  California  200         5002

```

**Output:**

<img width="1283" height="776" alt="image" src="https://github.com/user-attachments/assets/f98e66d2-78c8-4039-a90c-fc298af8bfb1" />


**Question 3**
---
-- Paste Question 3 here

```sql
Write a SQL query to retrieve all columns from the CUSTOMERS table for customers whose Address as Delhi and age below 30

Sample table: CUSTOMERS

ID          NAME        AGE         ADDRESS     SALARY
----------  ----------  ----------  ----------  ----------

1          Ramesh     32              Ahmedabad     2000
2          Khilan        25              Delhi                 1500
3          Kaushik      23              Kota                  2000
4          Chaitali       25             Mumbai            6500
5          Hardik        27              Bhopal              8500
6          Komal         22              Hyderabad       4500

7           Muffy          24              Indore            10000

 
 

For example:

Result
ID          NAME        AGE         ADDRESS     SALARY
----------  ----------  ----------  ----------  ----------
2           Khilan      25          Delhi       1500

```

**Output:**

<img width="1281" height="810" alt="image" src="https://github.com/user-attachments/assets/122b6294-a900-45be-a9c0-8b18117cdbda" />


**Question 4**
---
-- Paste Question 4 here

```sql
From the following tables, write a SQL query to find all the orders generated in New York city. Return ord_no, purch_amt, ord_date, customer_id and salesman_id.

SALESMAN TABLE

name               type
-----------        ----------
salesman_id  numeric(5)
name             varchar(30)
city                 varchar(15)
commission   decimal(5,2)

ORDERS TABLE

name            type
----------      ----------
ord_no          int
purch_amt    real
ord_date       text
customer_id  int
salesman_id  int

For example:

Result
ord_no      purch_amt   ord_date    customer_id  salesman_id
----------  ----------  ----------  -----------  -----------
70002       65.26       2012-10-05  3002         5001
70005       2400.6      2012-07-27  3007         5001
70008       5760.0      2012-09-10  3002         5001
70013       3045.6      2012-04-25  3002         5001

```

**Output:**

<img width="1278" height="888" alt="image" src="https://github.com/user-attachments/assets/42bd4fde-3930-4cf2-955c-00ac7f0a76d5" />

**Question 5**
---
-- Paste Question 5 here

```sql
Write a SQL query to Retrieve the medications with dosages equal to the highest dosage

Medications Table



For example:

Result
medic  medication_name  dosage
-----  ---------------  ---------------
4      Acetaminophen    600mg

```

**Output:**

  <img width="1284" height="827" alt="image" src="https://github.com/user-attachments/assets/cc0980e3-7db4-4851-9377-be46a761a003" />


**Question 6**
---
-- Paste Question 6 here

```sql
Write a SQL query that retrieves the names of students and their corresponding grades, where the grade is equal to the maximum grade achieved in each subject.

Sample table: GRADES



For example:

Result
student_name     grade
---------------  ---------------
Charlie          95
Emma             92
John             85
```

**Output:**

<img width="1270" height="859" alt="image" src="https://github.com/user-attachments/assets/5320cfc1-cdc1-4eb3-b964-ccb28157d0ee" />


**Question 7**
---
-- Paste Question 7 here

```sql
Write a SQL query to retrieve all columns from the CUSTOMERS table for customers whose salary is LESS than $2500.

Sample table: CUSTOMERS

ID          NAME        AGE         ADDRESS     SALARY
----------  ----------  ----------  ----------  ----------

1          Ramesh     32              Ahmedabad     2000
2          Khilan        25              Delhi                 1500
3          Kaushik      23              Kota                  2000
4          Chaitali       25             Mumbai            6500
5          Hardik        27              Bhopal              8500
6          Komal         22              Hyderabad       4500

7           Muffy          24              Indore            10000

 
 

For example:

Result
ID          NAME        AGE         ADDRESS     SALARY
----------  ----------  ----------  ----------  ----------
1           Ramesh      32          Ahmedabad   2000
2           Khilan      25          Delhi       1500
3           Kaushik     23          Kota        2000
```

**Output:**

<img width="1284" height="870" alt="image" src="https://github.com/user-attachments/assets/df356d93-a723-4cfb-b74b-8931a5b07c44" />


**Question 8**
---
-- Paste Question 8 here

```sql
Write a SQL query to retrieve all columns from the CUSTOMERS table for customers whose salary is greater than $1500.

Sample table: CUSTOMERS

ID          NAME        AGE         ADDRESS     SALARY
----------  ----------  ----------  ----------  ----------

1          Ramesh     32              Ahmedabad     2000
2          Khilan        25              Delhi                 1500
3          Kaushik      23              Kota                  2000
4          Chaitali       25             Mumbai            6500
5          Hardik        27              Bhopal              8500
6          Komal         22              Hyderabad       4500

7           Muffy          24              Indore            10000

 
 

For example:

Result
ID          NAME        AGE         ADDRESS     SALARY
----------  ----------  ----------  ----------  ----------
1           Ramesh      32          Ahmedabad   2000
3           Kaushik     23          Kota        2000
4           Chaitali    25          Mumbai      6500
5           Hardik      27          Bhopal      8500
6           Komal       22          Hyderabad   4500
7           Muffy       24          Indore      10000
```

**Output:**

<img width="1280" height="925" alt="image" src="https://github.com/user-attachments/assets/1c67019a-f499-4b2d-b674-3a396c542939" />


**Question 9**
---
-- Paste Question 9 here

```sql
Write a SQL query to List departments with names longer than the average length

Departments Table



For example:

Result
depar  department_name
-----  ---------------
5      Anesthesiologis

```

**Output:**

<img width="1293" height="838" alt="image" src="https://github.com/user-attachments/assets/d9a70775-bd7e-445a-b54a-1548b5ffa627" />


**Question 10**
---
-- Paste Question 10 here

```sql
Write a SQL query that retrieves the all the columns from the Table Grades, where the grade is equal to the minimum grade achieved in each subject.

Sample table: GRADES



For example:

Result
student_id       student_name     subject          grade
---------------  ---------------  ---------------  ---------------
2                Bob              Math             85
6                Frank            Science          85
7                John             Social           85
```

**Output:**

<img width="1291" height="859" alt="image" src="https://github.com/user-attachments/assets/a2ff9302-26fc-4df2-b7b4-368b64f0ac33" />

<img width="1895" height="969" alt="image" src="https://github.com/user-attachments/assets/5e43d43a-b048-47d3-8e4c-cab93c47ed26" />

## RESULT
Thus, the SQL queries to implement subqueries and views have been executed successfully.
