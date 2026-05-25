# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
-- Paste Question 1 here

```sql
Write a SQL query to Delete All Doctors with a NULL Specialization

Sample table: Doctors

attributes : doctor_id, first_name, last_name, specialization
For example:

Test	Result
SELECT * FROM doctors;
doctor_id   first_name  last_name   specialization
----------  ----------  ----------  --------------
1           John        Smith       Cardiology
2           Emily       Johnson     Orthopedics
3           Michael     Brown       Pediatrics
4           Febin       Jones
doctor_id   first_name  last_name   specialization
----------  ----------  ----------  --------------
1           John        Smith       Cardiology
2           Emily       Johnson     Orthopedics
3           Michael     Brown       Pediatrics
```

**Output:**

<img width="1189" height="871" alt="image" src="https://github.com/user-attachments/assets/ba7f4fe5-ea44-4a41-b476-73f50f03cec2" />


**Question 2**
---
-- Paste Question 2 here

```sql
Write a SQL query to find the details of those salespeople who live in cities other than Paris and Rome. Return salesman_id, name, city, commission.

Sample table: salesman

 salesman_id |    name    |   city   | commission 
-------------+------------+----------+------------
        5001 | James Hoog | New York |       0.15
        5002 | Nail Knite | Paris    |       0.13
        5005 | Pit Alex   | London   |       0.11
For example:

Result
salesman_id  name        city        commission
-----------  ----------  ----------  ----------
5005         Pit Alex    London      0.11
5003         Lauson Hen  San Jose    0.12

```

**Output:**

<img width="1254" height="908" alt="image" src="https://github.com/user-attachments/assets/3b7fa387-19ea-4a08-a1c6-78117ca613e4" />


**Question 3**
---
-- Paste Question 3 here

```sql
Write a SQL query to calculate the absolute value of the value1 column from the Calculations table.

cid         name        type        notnull     dflt_value  pk
----------  ----------  ----------  ----------  ----------  ----------
0           id          INTEGER     0                       1
1           value1      REAL        0                       0
2           value2      REAL        0                       0
3           base        INTEGER     0                       0
4           exponent    INTEGER     0                       0
5           number      REAL        0                       0
6           decimal     REAL        0                       0
 

For example:

Result
id          value1      absolute_value
----------  ----------  --------------
1           -87.65      87.65
2           45.78       45.78
3           89.99       89.99
4           -0.005      0.005

```

**Output:**

<img width="1246" height="812" alt="image" src="https://github.com/user-attachments/assets/edeed96e-2c2c-42d3-b0d0-fab7c4f81af2" />


**Question 4**
---
-- Paste Question 4 here

```sql
Update the 'Selling_Price' to add 10% extra margin for all products supplied by the supplier with id 6.

PRODUCTS TABLE

name               type
-----------------  ---------------
product_id         INT
product_name       VARCHAR(100)
category           VARCHAR(50)
cost_price         DECIMAL(10,2)
sell_price         DECIMAL(10,2)
reorder_lvl        INT
quantity           INT
supplier_id        INT
For example:

Test	Result
select changes();
changes()
----------
4

```

**Output:**

<img width="1278" height="917" alt="image" src="https://github.com/user-attachments/assets/f1301ab3-a93d-44bf-857b-094d6d97e175" />


**Question 5**
---
-- Paste Question 5 here

```sql
Write a SQL query to delete a doctor from Doctors table whose Specialization is 'Pediatrics' and First name is 'Michael'.

Sample table: Doctors

attributes: doctor_id, first_name, last_name, specialization
```

**Output:**

<img width="1272" height="807" alt="image" src="https://github.com/user-attachments/assets/b0d9f2b1-2e73-49a2-a65c-df37d2a88794" />


**Question 6**
---
-- Paste Question 6 here

```sql
 Write a query to fetch 3 top salaried records from EmployeePosition table.
EmpID

EmpPosition

DateOfJoining

Salary

1

Manager

01/05/2024

500000

2

Executive

02/05/2024

75000

 
 

For example:

Result
EmpID       EmpPosition  DateOfJoining  Salary
----------  -----------  -------------  ----------
1           Manager      2024-05-01     500000
1           Executive    2024-05-01     300000
3           Manager      2024-05-01     90000

```

**Output:**

<img width="1285" height="733" alt="image" src="https://github.com/user-attachments/assets/5c787b7f-62f9-4ae0-8142-d1dbdd9d2104" />


**Question 7**
---
-- Paste Question 7 here

```sql
Write a SQL query to calculate the number of years each employee has been with the company till '2024-08-30'.

Calculations table

cid         name        type        
----------  ----------  ---------- 
0           empno       INT         
1           ename       VARCHAR(100)
2           job         VARCHAR(50)
3           mgr         INT        
4           hiredate    DATE        
5           sal         DECIMAL(10,2)  
6           comm        DECIMAL(10,2)  
7           deptno      INT         
For example:

Result
ename       Tenure
----------  ----------
JONES       43
MARTIN      42
BLAKE       43
CLARK       43
SCOTT       41
KING        42
TURNER      42
```

**Output:**

<img width="1283" height="809" alt="image" src="https://github.com/user-attachments/assets/707cc2c8-e012-40d8-b69f-ed8856d993fa" />


**Question 8**
---
-- Paste Question 8 here

```sql
Write a SQL statement to Increase quantity of all products by 10% to adjust for surplus stock counted

Products table

---------------
product_id
product_name
category
cost_price
sell_price
reorder_lvl
quantity
supplier_id
```

**Output:**

<img width="1258" height="923" alt="image" src="https://github.com/user-attachments/assets/8cc86e4a-d480-4be5-b4ac-402627bfad25" />


**Question 9**
---
-- Paste Question 9 here

```sql
Write a SQL query to find all employees along with the day of the week on which they were hired from the emp table

emp table

cid         name        type        
----------  ----------  ---------- 
0           empno       INT         
1           ename       VARCHAR(100)
2           job         VARCHAR(50)
3           mgr         INT        
4           hiredate    DATE        
5           sal         DECIMAL(10,2)  
6           comm        DECIMAL(10,2)  
7           deptno      INT         
For example:

Result
ename       hiredate    day_of_week
----------  ----------  -----------
JONES       1981-04-02  Thursday
MARTIN      1981-09-28  Monday
BLAKE       1981-05-01  Friday
CLARK       1981-06-09  Tuesday
SCOTT       1982-12-09  Thursday
KING        1981-11-17  Tuesday
TURNER      1981-09-08  Tuesday

```

**Output:**

<img width="1269" height="797" alt="image" src="https://github.com/user-attachments/assets/2929082d-fa93-49e4-8733-cd23262c24a5" />


**Question 10**
---
-- Paste Question 10 here

```sql
Write a SQL statement to change the email column of employees table with 'Unavailable' for all employees in employees table.


Employees table

---------------
employee_id
first_name
last_name
email
phone_number
hire_date
job_id
salary
commission_pct
manager_id
department_id

                             

For example:

Test	Result
SELECT EMPLOYEE_ID,FIRST_NAME,EMAIL FROM EMPLOYEES LIMIT 2;
EMPLOYEE_ID  FIRST_NAME  EMAIL
-----------  ----------  -----------
100          Steven      Unavailable
101          Neena       Unavailable

```

**Output:**

<img width="1287" height="865" alt="image" src="https://github.com/user-attachments/assets/05226450-4816-4f68-8fea-03e425eddcda" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
