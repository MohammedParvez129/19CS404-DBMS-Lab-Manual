# Experiment 9: PL/SQL – Procedures and Functions

## AIM
To understand and implement procedures and functions in PL/SQL for performing various operations such as calculations, decision-making, and looping.

---

## THEORY

PL/SQL (Procedural Language/SQL) extends SQL by adding procedural constructs like variables, conditions, loops, procedures, and functions. Procedures and functions are subprograms that help modularize the code and improve reusability.

### **Procedure**
A PL/SQL **procedure** is a subprogram that performs a specific action. It does not return a value directly but can return values using `OUT` parameters.

**Syntax:**
```sql
CREATE OR REPLACE PROCEDURE procedure_name (parameters)
IS
BEGIN
   -- statements
END;
```

To call the procedure

```sql
EXEC procedure_name(arguments);
```

### **Function**
A PL/SQL **function** is a subprogram that returns a single value using the RETURN keyword.

```sql
CREATE OR REPLACE FUNCTION function_name (parameters)
RETURN datatype
IS
BEGIN
   -- statements
   RETURN value;
END;
```

To call the function:

```sql
SELECT function_name(arguments) FROM DUAL;
```

Key Differences:

-A procedure does not return a value, whereas a function must return a value.
-Functions can be called from SQL queries, procedures cannot (in most cases).

## 1. Write a PL/SQL Procedure to Find the Square of a Number

### Steps:
- Create a procedure named `find_square`.
- Declare a parameter to accept a number.
- Inside the procedure, compute the square of the input number.
- Use `DBMS_OUTPUT.PUT_LINE` to display the result.
- Call the procedure with a number as input.

<img width="490" height="591" alt="image" src="https://github.com/user-attachments/assets/9775f5e4-7713-4d54-91ca-a3cbad7036c8" />

**Expected Output:**  
Square of 6 is 36
<img width="947" height="156" alt="image" src="https://github.com/user-attachments/assets/33fb8e28-c163-4cb3-8cc2-ebafc26dc6c0" />

---

## 2. Write a PL/SQL Function to Return the Factorial of a Number

### Steps:
- Create a function named `get_factorial`.
- Declare a parameter to accept a number.
- Use a loop to calculate the factorial.
- Return the result using the `RETURN` statement.
- Call the function using a `SELECT` statement or in an anonymous block.

<img width="486" height="595" alt="image" src="https://github.com/user-attachments/assets/bf3b9d09-ed56-438d-9d87-468e82d09533" />

**Expected Output:**  
Factorial of 5 is 120

<img width="476" height="592" alt="image" src="https://github.com/user-attachments/assets/a9457ab7-d584-4d2f-bd56-d160d933be2e" />

---

## 3. Write a PL/SQL Procedure to Check Whether a Number is Even or Odd

### Steps:
- Create a procedure named `check_even_odd`.
- Accept an input parameter.
- Use the `MOD` function to check if the number is divisible by 2.
- Display whether it is Even or Odd using `DBMS_OUTPUT.PUT_LINE`.

<img width="484" height="560" alt="image" src="https://github.com/user-attachments/assets/701c1a44-670a-477a-9ebd-343591a597e1" />

**Expected Output:**  
12 is Even

<img width="525" height="167" alt="image" src="https://github.com/user-attachments/assets/ead77769-c082-48b7-8130-9364abbd751a" />

---

## 4. Write a PL/SQL Function to Return the Reverse of a Number

### Steps:
- Create a function named `reverse_number`.
- Accept an input number as parameter.
- Use a loop to reverse the digits of the number.
- Return the reversed number.
- Call the function and display the output.

<img width="479" height="633" alt="image" src="https://github.com/user-attachments/assets/dc5e037b-1f14-40af-92ed-e80df3a2c157" />


**Expected Output:**  
Reversed number of 1234 is 4321

<img width="481" height="500" alt="image" src="https://github.com/user-attachments/assets/d7da0738-307f-436d-b2cd-83641492851b" />

---

## 5. Write a PL/SQL Procedure to Display the Multiplication Table of a Number

### Steps:
- Create a procedure named `print_table`.
- Accept an input number.
- Use a loop from 1 to 10 to multiply the input number.
- Display the multiplication results using `DBMS_OUTPUT.PUT_LINE`.

<img width="478" height="579" alt="image" src="https://github.com/user-attachments/assets/c96ccaf0-ee72-49b1-b2a7-502086420db4" />

**Expected Output:**  
Multiplication table of 5:  
5 x 1 = 5  
5 x 2 = 10  
5 x 3 = 15  
...  
5 x 10 = 50

<img width="440" height="288" alt="image" src="https://github.com/user-attachments/assets/0bdc2ed9-6cd9-43c7-973e-f849658a5b59" />

## RESULT
Thus, the PL/SQL programs using procedures and functions were written, compiled, and executed successfully.
