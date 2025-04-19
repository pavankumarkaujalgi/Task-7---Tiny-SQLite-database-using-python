# Task-7---Tiny-SQLite-database-using-python

# 🧾 Sales Summary using SQLite & Python (Task 7 - Data Analyst Internship)

This project demonstrates how to extract and visualize basic sales data using **SQLite in Python**.

---

## 🎯 Objective

- Connect Python to a small SQLite database (`sales_data.db`)
- Run SQL queries to calculate:
  - Total quantity sold
  - Total revenue
- Display results using `print()` and visualize with a `matplotlib` bar chart

---

## 🧰 Tools & Technologies

- Python
- SQLite (`sqlite3`)
- Pandas
- Matplotlib

---

## 🗃️ Dataset Structure

SQLite table: `sales`

| id | product   | quantity | price  |
|----|-----------|----------|--------|
| 1  | Product A | 10       | 20.00  |
| 2  | Product B | 5        | 15.00  |
| 3  | Product A | 7        | 20.00  |
| 4  | Product C | 12       | 10.00  |

---

## 🧪 SQL Query Used

```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
