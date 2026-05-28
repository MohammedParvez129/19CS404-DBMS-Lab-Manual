# Experiment 10: PL/SQL – Triggers

## AIM
To write and execute PL/SQL trigger programs for automating actions in response to specific table events like INSERT, UPDATE, or DELETE.

---

## THEORY

A **trigger** is a stored PL/SQL block that is automatically executed or fired when a specified event occurs on a table or view. Triggers can be used for enforcing business rules, auditing changes, or automatic updates.

### Types of Triggers:
- **Before Trigger**: Executes before the operation (INSERT, UPDATE, DELETE).
- **After Trigger**: Executes after the operation.
- **Row-level Trigger**: Executes for each affected row.
- **Statement-level Trigger**: Executes once for the triggering statement.

**Basic Syntax:**
```sql
CREATE OR REPLACE TRIGGER trigger_name
BEFORE|AFTER INSERT|UPDATE|DELETE ON table_name
[FOR EACH ROW]
BEGIN
   -- trigger logic
END;
```

## 1. Write a trigger to log every insertion into a table.
**Steps:**
- Create two tables: `employees` (for storing data) and `employee_log` (for logging the inserts).
- Write an **AFTER INSERT** trigger on the `employees` table to log the new data into the `employee_log` table.

**Expected Output:**
- A new entry is added to the `employee_log` table each time a new record is inserted into the `employees` table.

<img width="545" height="723" alt="image" src="https://github.com/user-attachments/assets/34300bf1-3dc4-4405-bcdc-8c0af15f1e8c" />

<img width="943" height="170" alt="image" src="https://github.com/user-attachments/assets/0dd6edde-01f4-41ba-a30f-38a3bd7d9202" />


---

## 2. Write a trigger to prevent deletion of records from a sensitive table.
**Steps:**
- Write a **BEFORE DELETE** trigger on the `sensitive_data` table.
- Use `RAISE_APPLICATION_ERROR` to prevent deletion and issue a custom error message.

**Expected Output:**
- If an attempt is made to delete a record from `sensitive_data`, an error message is raised, e.g., `ERROR: Deletion not allowed on this table.`

<img width="548" height="526" alt="image" src="https://github.com/user-attachments/assets/76fde6f5-da66-4cc4-85eb-94086822ae21" />

<img width="928" height="170" alt="image" src="https://github.com/user-attachments/assets/e6bf82ce-d6b1-408d-bc69-5994f6c1d84d" />

---

## 3. Write a trigger to automatically update a `last_modified` timestamp.
**Steps:**
- Add a `last_modified` column to the `products` table.
- Write a **BEFORE UPDATE** trigger on the `products` table to set the `last_modified` column to the current timestamp whenever an update occurs.

**Expected Output:**
- The `last_modified` column in the `products` table is updated automatically to the current date and time when any record is updated.

<img width="545" height="494" alt="image" src="https://github.com/user-attachments/assets/7fe41104-c547-4a61-a2ee-a4800bd0412c" />

<img width="943" height="240" alt="image" src="https://github.com/user-attachments/assets/f257437f-fbdb-4c36-825f-07720ed2341c" />

---

## 4. Write a trigger to keep track of the number of updates made to a table.
**Steps:**
- Create an `audit_log` table with a counter column.
- Write an **AFTER UPDATE** trigger on the `customer_orders` table to increment the counter in the `audit_log` table every time a record is updated.

**Expected Output:**
- The `audit_log` table will maintain a count of how many updates have been made to the `customer_orders` table.

<img width="543" height="520" alt="image" src="https://github.com/user-attachments/assets/483c29f8-9bae-4725-9b67-edbf63825e5c" />

<img width="857" height="164" alt="image" src="https://github.com/user-attachments/assets/abaaaa80-bfcf-4845-9978-3f16b58d4f5d" />

---

## 5. Write a trigger that checks a condition before allowing insertion into a table.
**Steps:**
- Write a **BEFORE INSERT** trigger on the `employees` table to check if the inserted salary meets a specific condition (e.g., salary must be greater than 3000).
- If the condition is not met, raise an error to prevent the insert.

**Expected Output:**
- If the inserted salary in the `employees` table is below the condition (e.g., salary < 3000), the insert operation is blocked, and an error message is raised, such as: `ERROR: Salary below minimum threshold.`

<img width="545" height="569" alt="image" src="https://github.com/user-attachments/assets/6a7faf41-fc1a-4b1d-8ded-d06365ba772e" />

<img width="936" height="322" alt="image" src="https://github.com/user-attachments/assets/ef45abca-b3a8-430a-bb04-b1e1468331d2" />

## RESULT
Thus, the PL/SQL trigger programs were written and executed successfully.
