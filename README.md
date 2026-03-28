# 🛒 Amazon Sales Database Management System

## 📌 Abstract

The **Amazon Sales Database Management System** is a MySQL-based project developed to design and manage an e-commerce sales database. The system stores and analyzes sales transactions including customer details, product information, payment methods, and customer ratings. The primary objective of this project is to demonstrate database creation, data manipulation, data analysis, and relational operations using SQL queries.

The project implements important SQL concepts such as table creation, data insertion, aggregate functions, string and date functions, joins, subqueries, window functions, and transaction control commands. Using these operations, the system enables efficient analysis of sales performance, customer behavior, and product category trends.

This project provides practical knowledge of how real-world e-commerce platforms manage and analyze large volumes of transactional data using relational database systems.
<img width="1378" height="617" alt="amazon sales " src="https://github.com/user-attachments/assets/d641984f-f7ed-4f93-86a0-2794596806b3" />

---

## 📖 Introduction

Modern e-commerce platforms generate massive amounts of sales data daily. Efficient management of this data requires a structured database system capable of storing, retrieving, and analyzing information effectively.

MySQL, a widely used Relational Database Management System (RDBMS), is used in this project to simulate a small-scale Amazon sales environment where:

* Customer orders are stored
* Product sales are tracked
* Payment methods are recorded
* Customer memberships are maintained
* Sales analytics are performed

---

## 🎯 Objectives

* Create and manage a relational database using MySQL.
* Perform CRUD operations (Create, Read, Update, Delete).
* Apply aggregate and analytical SQL functions.
* Understand relationships between tables using joins.
* Analyze sales data for business insights.
* Implement transaction management for data safety.

---

## 🛠️ Tools and Technologies Used

| Component      | Technology                     |
| -------------- | ------------------------------ |
| Database       | MySQL                          |
| Query Language | SQL                            |
| Platform       | MySQL Workbench / Command Line |
| Database Type  | Relational Database            |

---

## 🗄️ Database Design

### Database Name

```
amazon_sales
```

---

### 📊 Table: `sales`

Stores order and product transaction details.

| Column Name      | Data Type | Description             |
| ---------------- | --------- | ----------------------- |
| order_id         | INT       | Unique order identifier |
| order_date       | DATE      | Date of purchase        |
| customer_name    | VARCHAR   | Customer name           |
| city             | VARCHAR   | Customer city           |
| product_category | VARCHAR   | Product category        |
| product_name     | VARCHAR   | Product purchased       |
| quantity         | INT       | Quantity ordered        |
| price            | DECIMAL   | Product price           |
| payment_method   | VARCHAR   | Payment mode            |
| rating           | DECIMAL   | Customer rating         |
| customer_id      | INT       | Customer reference ID   |

---

### 👤 Table: `customers`

Stores customer membership information.

| Column Name   | Data Type | Description     |
| ------------- | --------- | --------------- |
| customer_id   | INT       | Customer ID     |
| customer_name | VARCHAR   | Name            |
| city          | VARCHAR   | Location        |
| membership    | VARCHAR   | Prime / Regular |

---

## ⚙️ SQL Operations Performed

### 🔹 Data Definition Language (DDL)

* CREATE DATABASE
* CREATE TABLE
* ALTER TABLE

---

### 🔹 Data Manipulation Language (DML)

* INSERT records
* UPDATE records
* DELETE records

---

### 🔹 Data Retrieval

```sql
SELECT * FROM sales;
```

---

### 🔹 Calculated Columns

```sql
quantity * price AS total_amount
```

Used to calculate total revenue per order.

---

### 🔹 Aggregate Functions

* `COUNT()` → Total orders
* `SUM()` → Total sales revenue
* `AVG()` → Average rating
* `MAX()` / `MIN()` → Price analysis

---

### 🔹 GROUP BY and HAVING

```sql
GROUP BY product_category
HAVING total_sales > 2000;
```

Identifies high-performing product categories.

---

### 🔹 String Functions

* UPPER()
* LOWER()
* CONCAT()
* LENGTH()

Used for formatting and text analysis.

---

### 🔹 Date Functions

* YEAR()
* MONTH()
* DAY()

Used for time-based sales reporting.

---

### 🔹 Conditional Function

```sql
IF(rating >= 4,'Good','Average')
```

Classifies customer reviews.

---

### 🔹 Sorting

```sql
ORDER BY price DESC;
```

---

### 🔹 Subqueries

```sql
WHERE price > (SELECT AVG(price) FROM sales);
```

Finds customers paying above-average price.

---

### 🔹 Window Functions

* ROW_NUMBER()
* RANK()

Used for ranking sales records.

---

### 🔹 Joins Implemented

* INNER JOIN
* LEFT JOIN
* RIGHT JOIN
* UNION

Used to combine customer and sales information.

---

### 🔹 Transaction Control Language (TCL)

* DELETE
* ROLLBACK
* COMMIT

Ensures data consistency and recovery.

---

## 📈 Results and Analysis

The database enables:

* Identification of best-selling product categories
* Total revenue calculation
* Customer rating analysis
* Membership-based tracking
* Product ranking based on price

### Key Findings

* Electronics category generated higher revenue.
* Customers with ratings ≥ 4 are categorized as good reviewers.
* Window functions improve analytical reporting.

---


## 🏁 Conclusion

The Amazon Sales Database project demonstrates how MySQL can be used to efficiently manage and analyze e-commerce sales data. The implementation of joins, aggregate functions, window functions, and transaction management provides practical exposure to real-world database operations and analytics.

---


