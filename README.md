# SQL-PROJECT

# Trendora SQL Queries

## 📌 Project Overview

This repository contains a set of **basic to intermediate SQL queries** written to explore and analyze the `task.trendora` table. The queries are designed as practice exercises to demonstrate understanding of:

* Data retrieval using `SELECT`
* Filtering records with `WHERE`
* Logical operators (`AND`, `OR`, `IN`, `BETWEEN`, `NOT LIKE`)
* Sorting results with `ORDER BY`
* Limiting results using `LIMIT` and `OFFSET`

This project is ideal for **SQL beginners**, data analyst trainees, and anyone practicing querying transactional datasets.

---

## 🗂 Dataset Description

**Table Name:** `task.trendora`

The table represents customer purchase data from an e-commerce store and includes fields such as:

* `CustomerID`
* `ItemPurchased`
* `PurchaseAmount`
* `Category`
* `Color`
* `Size`
* `Season`
* `PaymentMethod`
* `Gender`
* `PromoCodeUsed`
* `DiscountValue`
* `ShippingType`

---

## 🧠 SQL Questions & Solutions

### Question 1: View all records

```sql
SELECT *
FROM task.trendora;
```

### Question 2: Retrieve customer purchases and amounts

```sql
SELECT CustomerID, ItemPurchased, PurchaseAmount
FROM task.trendora;
```

### Question 3: Items with purchase amount greater than 60

```sql
SELECT ItemPurchased, PurchaseAmount
FROM task.trendora
WHERE PurchaseAmount > 60;
```

### Question 4: Items in the Clothing or Footwear category

```sql
SELECT *
FROM task.trendora
WHERE Category = 'Clothing' OR Category = 'Footwear';
```

### Question 5: Gray items of size M

```sql
SELECT *
FROM task.trendora
WHERE Color = 'Gray' AND Size = 'M';
```

### Question 6: Purchases between 30 and 70

```sql
SELECT *
FROM task.trendora
WHERE PurchaseAmount BETWEEN 30 AND 70;
```

### Question 7: Items purchased in Summer or Winter

```sql
SELECT ItemPurchased, Season
FROM task.trendora
WHERE Season IN ('Summer', 'Winter');
```

### Question 8: Exclude payment methods starting with 'CA'

```sql
SELECT *
FROM task.trendora
WHERE PaymentMethod NOT LIKE 'CA%';
```

### Question 9: Female customers who purchased Clothing

```sql
SELECT Gender, Category
FROM task.trendora
WHERE Gender = 'Female' AND Category = 'Clothing';
```

### Question 10: Purchases with promo code and discount applied

```sql
SELECT *
FROM task.trendora
WHERE PromoCodeUsed = 'Yes'
  AND DiscountValue > 0;
```

### Question 11: Items ordered by highest purchase amount

```sql
SELECT ItemPurchased, PurchaseAmount
FROM task.trendora
ORDER BY PurchaseAmount DESC;
```

### Question 12: Top 3 most expensive items

```sql
SELECT ItemPurchased, PurchaseAmount
FROM task.trendora
ORDER BY PurchaseAmount DESC
LIMIT 3;
```

### Question 13: 2 cheapest items

```sql
SELECT ItemPurchased, PurchaseAmount
FROM task.trendora
ORDER BY PurchaseAmount ASC
LIMIT 2;
```

### Question 14: 10 items after skipping the top 5 expensive ones

```sql
SELECT ItemPurchased, PurchaseAmount
FROM task.trendora
ORDER BY PurchaseAmount DESC
LIMIT 10 OFFSET 5;
```

### Question 15: First 5 express shipping orders

```sql
SELECT *
FROM task.trendora
WHERE ShippingType = 'Express'
LIMIT 5;
```

---

## 🛠 Tools Used

* SQL (MySQL / PostgreSQL compatible syntax)


---

## 🚀 How to Use

1. Clone the repository
2. Load the `trendora` dataset into your SQL environment
3. Run the queries individually to explore the data

---

## 📬 Author

**Onome Otomewo**
Junior Data Analyst | SQL | Excel | Power BI


