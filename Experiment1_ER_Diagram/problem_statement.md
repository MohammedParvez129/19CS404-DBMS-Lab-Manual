# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
<img width="1400" height="778" alt="image" src="https://github.com/user-attachments/assets/a420c301-200c-45dc-b320-003721c4a10d" />


### 1. Entity List and Attributes
1. Customer 

• CustomerID (PK)  
• CustomerName  
• PhoneNumber  
• Email  
2. Reservation 

• ReservationID (PK)  
• ReservationDate  
• ReservationTime  
• NumberOfGuests  
• ReservationType (Advance / Walk-in)  
3. Table 

• TableID (PK)  
• TableNumber  
• Capacity  
• Location  
4. Waiter 

• WaiterID (PK)  
• WaiterName  
• PhoneNumber  
• ShiftTiming  
5. Order 

• OrderID (PK)  
• OrderDate  
• OrderStatus  
• TotalAmount  
6. Dish 

• DishID (PK)  
• DishName  
• Price  
• CategoryID (FK)   
7. OrderItem 

• OrderItemID (PK)  
• Quantity  
• SubTotal  
• OrderID (FK)  
8. Bill 

• BillID (PK)  
• BillDate  
• FoodCharges  
• ServiceCharges  
• TotalBillAmount  
### 2. Primary Keys (PK) 
| Entity      |   Primary Key |
| ----------- | ------------: |
| Customer    |    CustomerID |
| Reservation | ReservationID |
| Table       |       TableID |
| Waiter      |      WaiterID |
| Order       |       OrderID |
| Dish        |        DishID |
| OrderItem   |   OrderItemID |
| Bill        |        BillID |



### 3. Relationship Documentation 
| Relationship           | Cardinality | Explanation                                            |
| ---------------------- | ----------: | ------------------------------------------------------ |
| Customer → Reservation |       1 : N | One customer can make many reservations                |
| Reservation → Table    |       N : 1 | Many reservations can use one table at different times |
| Waiter → Reservation   |       1 : N | One waiter serves many reservations                    |
| Reservation → Order    |       1 : N | One reservation can have multiple orders               |
| Order → OrderItem      |       1 : N | One order contains many order items                    |
| Dish → OrderItem       |       1 : N | One dish can appear in many order items                |
| Reservation → Bill     |       1 : 1 | Each reservation generates one bill                    |


### 4. Assumptions 

1. A customer can make multiple reservations.  
2. Walk-in customers are also recorded as customers in the system.  
3. Each reservation is assigned to one table.  
4. One waiter can handle multiple reservations during a shift.  
5. A reservation may contain multiple food orders.  
6. Each order can contain multiple dishes through the OrderItem entity.  
7. Each dish belongs to only one category.  
8. One bill is generated for each reservation.  
9. Service charges are included in the final bill amount.

---

### Result:
The given experiment is successfuly completed.
