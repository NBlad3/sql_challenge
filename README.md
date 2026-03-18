# 🟢 Level 1 – Basic SELECT & Filtering (Solutions)

---

## 1️⃣ Retrieve all records from the `sales` table

```sql
SELECT *
FROM sales;
```

---

## 2️⃣ Retrieve all records from the `menu` table

```sql
SELECT *
FROM menu;
```

---

## 3️⃣ Show a list of unique customers who have made purchases

```sql
SELECT DISTINCT customer_id
FROM sales;
```

---

## 4️⃣ Retrieve all sales made in January 2021

### ✅ Using comparison operators

```sql
SELECT *
FROM sales
WHERE order_date >= '2021-01-01'
  AND order_date <= '2021-01-31';
```

### ✅ Using BETWEEN (inclusive)

```sql
SELECT *
FROM sales
WHERE order_date BETWEEN '2021-01-01' AND '2021-01-31';
```

---

## 5️⃣ Retrieve all sales made by customer A

```sql
SELECT *
FROM sales
WHERE customer_id = 'A';
```

---

## 6️⃣ Show all menu items with a price greater than 15

```sql
SELECT *
FROM menu
WHERE price > 15;
```

---

## 7️⃣ Display the menu items sorted by price in descending order

```sql
SELECT *
FROM menu
ORDER BY price DESC;
```

---

## 8️⃣ Count total rows in the `sales` table

```sql
SELECT COUNT(*) AS total_sales
FROM sales;
```

---

## 9️⃣ Calculate the total revenue from all sales (without grouping)

```sql
SELECT SUM(m.price) AS total_revenue
FROM sales s
JOIN menu m
  ON s.product_id = m.product_id;
```

---

## 🔟 Calculate the average price of all menu items

```sql
SELECT AVG(price) AS average_price
FROM menu;
```

---

✨ These queries cover:

- Basic `SELECT`
- `DISTINCT`
- `WHERE`
- `BETWEEN`
- `ORDER BY`
- `COUNT`
- `SUM`
- `AVG`
- `JOIN`
