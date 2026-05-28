# Experiment 6: Joins

## AIM
To study and implement different types of joins.

## THEORY

SQL Joins are used to combine records from two or more tables based on a related column.

### 1. INNER JOIN
Returns records with matching values in both tables.

**Syntax:**
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

### 2. LEFT JOIN
Returns all records from the left table, and matched records from the right.

**Syntax:**

```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```
### 3. RIGHT JOIN
Returns all records from the right table, and matched records from the left.

**Syntax:**

```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```
### 4. FULL OUTER JOIN
Returns all records when there is a match in either left or right table.

**Syntax:**

```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.column = table2.column;
```

**Question 1**
--
-- Paste Question 1 here

<img width="1253" height="498" alt="image" src="https://github.com/user-attachments/assets/fdfbfd28-26e1-4f8c-a2d0-34beb2dc0fa8" />

**Output:**

<img width="1290" height="894" alt="image" src="https://github.com/user-attachments/assets/ca01ce51-6c40-41ee-b33e-e7e826d38b5e" />

**Question 2**
---
-- Paste Question 2 here

```sql
From the following tables write a SQL query to find the details of an order. Return ord_no, ord_date, purch_amt, Customer Name, grade, Salesman, commission. 

Sample table: orders

ord_no      purch_amt   ord_date    customer_id  salesman_id
----------  ----------  ----------  -----------  -----------
70001       150.5       2012-10-05  3005         5002
70009       270.65      2012-09-10  3001         5005
70002       65.26       2012-10-05  3002         5001
70004       110.5       2012-08-17  3009         5003
70007       948.5       2012-09-10  3005         5002
70005       2400.6      2012-07-27  3007         5001
70008       5760        2012-09-10  3002         5001
70010       1983.43     2012-10-10  3004         5006
70003       2480.4      2012-10-10  3009         5003
70012       250.45      2012-06-27  3008         5002
70011       75.29       2012-08-17  3003         5007
70013       3045.6      2012-04-25  3002         5001
Sample table: customer

 customer_id |   cust_name    |    city    | grade | salesman_id 
-------------+----------------+------------+-------+-------------
        3002 | Nick Rimando   | New York   |   100 |        5001
        3007 | Brad Davis     | New York   |   200 |        5001
        3005 | Graham Zusi    | California |   200 |        5002
        3008 | Julian Green   | London     |   300 |        5002
        3004 | Fabian Johnson | Paris      |   300 |        5006
        3009 | Geoff Cameron  | Berlin     |   100 |        5003
        3003 | Jozy Altidor   | Moscow     |   200 |        5007
        3001 | Brad Guzan     | London     |       |        5005
Sample table: salesman

 salesman_id |    name    |   city   | commission 
-------------+------------+----------+------------
        5001 | James Hoog | New York |       0.15
        5002 | Nail Knite | Paris    |       0.13
        5005 | Pit Alex   | London   |       0.11
        5006 | Mc Lyon    | Paris    |       0.14
        5007 | Paul Adam  | Rome     |       0.13
        5003 | Lauson Hen | San Jose |       0.12
For example:

Result
ord_no           ord_date         purch_amt        Customer Name    grade       Salesman    commission
---------------  ---------------  ---------------  ---------------  ----------  ----------  ----------
70001            2012-10-05       150.5            Graham Zusi      200         Nail Knite  0.13
70009            2012-09-10       270.65           Brad Guzan       100         Pit Alex    0.11
70002            2012-10-05       65.26            Nick Rimando     100         Bob Emily   0.15
70004            2012-08-17       110.5            Geoff Cameron    100         Lauson Hen  0.12
70007            2012-09-10       948.5            Graham Zusi      200         Nail Knite  0.13
70005            2012-07-27       2400.6           Brad Davis       200         Bob Emily   0.15
70008            2012-09-10       5760.0           Nick Rimando     100         Bob Emily   0.15
70010            2012-10-10       1983.43          Fabian Johns     300         Mc Lyon     0.14
70003            2012-10-10       2480.4           Geoff Cameron    100         Lauson Hen  0.12
70012            2012-06-27       250.45           Julian Green     300         Nail Knite  0.13
70011            2012-08-17       75.29            Jozy Altidore    200         Paul Adam   0.13
70013            2012-04-25       3045.6           Nick Rimando     100         Bob Emily   0.15
```

**Output:**

<img width="1274" height="927" alt="image" src="https://github.com/user-attachments/assets/7ec0632f-a372-4e1c-bc7b-35facde5ead5" />

**Question 3**
---
-- Paste Question 3 here

```sql
Write a SQL statement to join the tables salesman, customer and orders so that the same column of each table appears once and only the relational rows are returned. 

Sample table: orders

ord_no      purch_amt   ord_date    customer_id  salesman_id
----------  ----------  ----------  -----------  -----------
70001       150.5       2012-10-05  3005         5002
70009       270.65      2012-09-10  3001         5005
70002       65.26       2012-10-05  3002         5001
70004       110.5       2012-08-17  3009         5003
70007       948.5       2012-09-10  3005         5002
70005       2400.6      2012-07-27  3007         5001
70008       5760        2012-09-10  3002         5001
70010       1983.43     2012-10-10  3004         5006
70003       2480.4      2012-10-10  3009         5003
70012       250.45      2012-06-27  3008         5002
70011       75.29       2012-08-17  3003         5007
70013       3045.6      2012-04-25  3002         5001
Sample table: customer

 customer_id |   cust_name    |    city    | grade | salesman_id 
-------------+----------------+------------+-------+-------------
        3002 | Nick Rimando   | New York   |   100 |        5001
        3007 | Brad Davis     | New York   |   200 |        5001
        3005 | Graham Zusi    | California |   200 |        5002
        3008 | Julian Green   | London     |   300 |        5002
        3004 | Fabian Johnson | Paris      |   300 |        5006
        3009 | Geoff Cameron  | Berlin     |   100 |        5003
        3003 | Jozy Altidor   | Moscow     |   200 |        5007
        3001 | Brad Guzan     | London     |       |        5005
Sample table : salesman

 salesman_id |    name    |   city   | commission 
-------------+------------+----------+------------
        5001 | James Hoog | New York |       0.15
        5002 | Nail Knite | Paris    |       0.13
        5005 | Pit Alex   | London   |       0.11
        5006 | Mc Lyon    | Paris    |       0.14
        5007 | Paul Adam  | Rome     |       0.13
        5003 | Lauson Hen | San Jose |       0.12
For example:

Result
ord_no           purch_amt        ord_date         customer_id      salesman_id  cust_name   city        grade       name        commission
---------------  ---------------  ---------------  ---------------  -----------  ----------  ----------  ----------  ----------  ----------
70009            270.65           2012-09-10       3001             5005         Brad Guzan  London      100         Pit Alex    0.11
70005            2400.6           2012-07-27       3007             5001         Brad Davis  New York    200         Bob Emily   0.15
70010            1983.43          2012-10-10       3004             5006         Fabian Joh  Paris       300         Mc Lyon     0.14
```

**Output:**

<img width="1291" height="912" alt="image" src="https://github.com/user-attachments/assets/986b801d-feb1-4125-860e-4db3790f81a4" />


**Question 4**
---
-- Paste Question 4 here

<img width="1252" height="481" alt="image" src="https://github.com/user-attachments/assets/0128b377-f3d5-4941-b7e2-d23c2da5f51e" />


**Output:**

<img width="1275" height="801" alt="image" src="https://github.com/user-attachments/assets/be46ff17-c8ea-4565-b21e-72b6c733c9ed" />

**Question 5**
---
-- Paste Question 5 here

<img width="1268" height="576" alt="image" src="https://github.com/user-attachments/assets/49095335-c8df-44de-8fb4-4a0f03700c60" />

**Output:**

<img width="1290" height="914" alt="image" src="https://github.com/user-attachments/assets/a946fe5d-bd81-4991-b975-69b2defafb6f" />

**Question 6**
---
-- Paste Question 6 here

<img width="1266" height="488" alt="image" src="https://github.com/user-attachments/assets/49f7b4d4-163c-47e1-9aad-fadaf2e8c4fb" />

**Output:**

<img width="1273" height="798" alt="image" src="https://github.com/user-attachments/assets/8fbf2f1d-69d3-469d-af53-36886c85960b" />


**Question 7**
---
-- Paste Question 7 here

<img width="1261" height="487" alt="image" src="https://github.com/user-attachments/assets/0321bd6f-ea4a-4858-aab8-c107e1ac20dc" />

**Output:**

<img width="1288" height="835" alt="image" src="https://github.com/user-attachments/assets/37670628-30e3-47c9-a532-dda5c096acc0" />

**Question 8**
---
-- Paste Question 8 here

```sql
Write the SQL query that accomplishes the selection of all columns from the "patients" table and the first name of doctors from the "doctors" table, with an inner join on the "doctor_id" column.

PATIENTS TABLE:
name             type
---------------  ---------------
patient_id       INT
first_name       VARCHAR(50)
last_name        VARCHAR(50)
date_of_birth    DATE
admission_date   DATE
discharge_date   DATE
doctor_id        INT

DOCTORS TABLE:

name             type
---------------  ---------------
doctor_id        INT
first_name       VARCHAR(50)
last_name        VARCHAR(50)
specialization   VARCHAR(100)

For example:

Result
patient_id       first_name       last_name        date_of_birth    admission_date  discharge_date  doctor_id   doctor_name
---------------  ---------------  ---------------  ---------------  --------------  --------------  ----------  -----------
1                Alice            Williams         1980-05-12       2024-01-10                      1           John
2                Bob              Miller           1995-08-23       2024-02-15      2024-03-01      2           Emily
3                Charlie          Davis            1972-11-30       2024-03-10                      3           Michael

```

**Output:**

<img width="1274" height="883" alt="image" src="https://github.com/user-attachments/assets/12ba399c-2342-4a9e-8fac-b3cb66b55cc3" />

**Question 9**
---
-- Paste Question 9 here

```sql
From the following tables write a SQL query to find those customers with a grade less than 300. Return cust_name, customer city, grade, Salesman, salesmancity. The result should be ordered by ascending customer_id. 

Sample table: customer

 customer_id |   cust_name    |    city    | grade | salesman_id 
-------------+----------------+------------+-------+-------------
        3002 | Nick Rimando   | New York   |   100 |        5001
        3007 | Brad Davis     | New York   |   200 |        5001
        3005 | Graham Zusi    | California |   200 |        5002
        3008 | Julian Green   | London     |   300 |        5002
        3004 | Fabian Johnson | Paris      |   300 |        5006
        3009 | Geoff Cameron  | Berlin     |   100 |        5003
        3003 | Jozy Altidor   | Moscow     |   200 |        5007
        3001 | Brad Guzan     | London     |       |        5005
Sample table: salesman

 salesman_id |    name    |   city   | commission 
-------------+------------+----------+------------
        5001 | James Hoog | New York |       0.15
        5002 | Nail Knite | Paris    |       0.13
        5005 | Pit Alex   | London   |       0.11
        5006 | Mc Lyon    | Paris    |       0.14
        5007 | Paul Adam  | Rome     |       0.13
        5003 | Lauson Hen | San Jose |       0.12
For example:

Result
cust_name        city             grade            Salesman         city
---------------  ---------------  ---------------  ---------------  ----------
Brad Guzan       London           100              Pit Alex         London
Nick Rimando     Chennai          100              Bob Emily        New York
Jozy Altidore    Moscow           200              Paul Adam        Rome
Graham Zusi      California       200              Nail Knite       Paris
Brad Davis       New York         200              Bob Emily        New York
Geoff Cameron    Berlin           100              Lauson Hen       San Jose

```

**Output:**

<img width="1272" height="894" alt="image" src="https://github.com/user-attachments/assets/3512bd10-89b6-4fb1-ba16-dd6c5a036284" />


**Question 10**
---
-- Paste Question 10 here


<img width="1219" height="499" alt="image" src="https://github.com/user-attachments/assets/47555eb7-f29d-4732-9cac-660c475e1e67" />


**Output:**


<img width="1282" height="889" alt="image" src="https://github.com/user-attachments/assets/7d1b31df-3e7c-4c5a-bbcf-e053cbff4762" />


<img width="1898" height="970" alt="image" src="https://github.com/user-attachments/assets/fbd5b02a-1c06-4b59-8b13-37c9ed8bbc27" />


## RESULT
Thus, the SQL queries to implement different types of joins have been executed successfully.
