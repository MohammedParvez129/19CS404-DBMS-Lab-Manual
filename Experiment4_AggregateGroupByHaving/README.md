# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
-- Paste Question 1 here

```sql
Write a SQL query to find the number of employees whose age is greater than 32.

Sample table: employee

id

name

age

address

salary

1

Paul

32

California

20000

4

Mark

25

Richtown

65000

5

David

27

Texas

85000

 

For example:

Result
COUNT
----------
5

```

**Output:**

<img width="1273" height="753" alt="image" src="https://github.com/user-attachments/assets/67e790df-9071-4f0f-87b0-983d5e4d45b4" />


**Question 2**
---
-- Paste Question 2 here

```sql
Write a SQL query to find the number of employees who are having the same age removing the duplicate values.

Sample table: employee

id

name

age

address

salary

1

Paul

32

California

20000

4

Mark

25

Richtown

65000

5

David

27

Texas

85000

 

For example:

Result
COUNT
----------
4

```

**Output:**

<img width="1283" height="771" alt="image" src="https://github.com/user-attachments/assets/1fc9a884-4b8c-4202-a3ca-60fc1d912919" />


**Question 3**
---
-- Paste Question 3 here

```sql
Write a SQL query to find the youngest employee in the company?

Table: employee

name        type
----------  ----------
id          INTEGER
name        TEXT
age         INTEGER
city        TEXT
income      INTEGER
 

For example:

Result
Employee_Name  Age
-------------  ----------
Peter          32

```

**Output:**

<img width="1273" height="766" alt="image" src="https://github.com/user-attachments/assets/34f7467c-3d2f-46c7-9225-b9a05a73af11" />


**Question 4**
---
-- Paste Question 4 here

```sql
How many patients have insurance coverage valid in each year?

Sample table:Insurance Table

name               type
-----------------  ----------
InsuranceID        INTEGER
PatientID          INTEGER
InsuranceCompany   TEXT
PolicyNumber       TEXT
PolicyHolder       TEXT
ValidityPeriod     TEXT
For example:

Result
ValidityYear  TotalPatients
------------  -------------
2024          3
2025          1
2027          4
2031          2

```

**Output:**

<img width="1283" height="809" alt="image" src="https://github.com/user-attachments/assets/ee129919-ddf3-4627-83b5-3ba1f4b329e1" />


**Question 5**
---
-- Paste Question 5 here

```sql
What is the total number of appointments scheduled for each day?

Sample table:Appointments Table



For example:

Result
AppointmentDate  TotalAppointments
---------------  -----------------
2024-02-16       4
2024-02-18       1
2024-02-20       1
2024-02-21       1
2024-02-22       1
2024-02-23       2

```

**Output:**

<img width="1303" height="925" alt="image" src="https://github.com/user-attachments/assets/d15119c5-832d-424a-8989-5adc6cbd9d62" />


**Question 6**
---
-- Paste Question 6 here

```sql
What is the count of male and female patients?

Sample table: Patients Table



For example:

Result
Gender      TotalPatients
----------  -------------
Female      5
Male        5

```

**Output:**

<img width="1306" height="731" alt="image" src="https://github.com/user-attachments/assets/af679516-594c-45a5-bc91-201757873797" />


**Question 7**
---
-- Paste Question 7 here

```sql
Write the SQL query that performs grouping by age groups and displays the maximum salary for each group, excluding groups where the maximum salary is not greater than 8000. 

Note: Calculate the age group as multiples of 5.

Eg., 20,22,23 comes in age group 20. 

25,27,29 comes in age group 25.

Sample table: customer1



For example:

Result
age_group   MAX(salary)
----------  -----------
20          10000
25          8500

```

**Output:**

<img width="1299" height="751" alt="image" src="https://github.com/user-attachments/assets/3f4461c6-61e9-464e-8c20-4f875d3a046f" />


**Question 8**
---
-- Paste Question 8 here

```sql
Write the SQL query to find how many patients have more than 3 medical records?.

Sample table: MedicalRecords

name        type
----------  ----------
RecordID    INTEGER
PatientID   INTEGER
DoctorID    INTEGER
Date        DATE
Diagnosis   TEXT
Treatment   TEXT
Medication  TEXT
For example:

Result
PatientID   TotalRecords
----------  ------------
1           4

```

**Output:**

<img width="1267" height="779" alt="image" src="https://github.com/user-attachments/assets/61826cc0-3f64-4000-9eb7-5d0ca9e38e58" />


**Question 9**
---
-- Paste Question 9 here

```sql
Write the SQL query that achieves the grouping of data by age intervals using the expression (age/5)5, calculates the total salary sum for each group, and excludes groups where the total salary sum is not greater than 5000.

Sample table: customer1



For example:

Result
age_group   SUM(salary)
----------  -----------
20          16500
25          16500

```

**Output:**

<img width="1283" height="781" alt="image" src="https://github.com/user-attachments/assets/daf1ef7a-146c-4986-80e1-dc6d0969ecfd" />


**Question 10**
---
-- Paste Question 10 here

```sql
Write the SQL query that accomplishes the selection of average price for each category from the "products" table and includes only those products where the average price falls between 10 and 15.

Sample table: products



For example:

Result
category_id  AVG(Price)
-----------  ----------
1            12.375

```

**Output:**

<img width="1283" height="741" alt="image" src="https://github.com/user-attachments/assets/bdfc7cfa-bd22-4676-b088-c5af8cd282bb" />

<img width="1863" height="924" alt="image" src="https://github.com/user-attachments/assets/e72c5ee5-e342-4dd6-bcb6-c68bc4fddee9" />


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
