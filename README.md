# 🍕 Pizza Sales Analysis (SQL Project)

This project explores pizza sales data using SQL to derive actionable business insights. It covers data cleaning, aggregation, and analysis techniques to answer targeted questions about sales volume, revenue, and customer behavior.

---

## 📂 Dataset

The dataset includes tables such as:

- `orders` (order_id, pizza_id, quantity, price, order_date, customer_id, etc.)
- `pizzas` (pizza_id, name, size, category, unit_price, etc.)
-## 📂 Data Sources

1. [Order Details CSV](https://bit.ly/sql-pizza-orders)  
2. [Pizza Types CSV](https://bit.ly/sql-pizza-types)  
3. [Pizza Categories CSV](https://bit.ly/sql-pizza-categories)  
4. [Pizza Sales Notes](https://bit.ly/sql-pizza-report)
-

---

## 🎯 Project Goals

- Calculate total sales and revenue  
- Identify top-selling pizzas and categories  
- Analyze order distribution over time (hours, days, months)  
- Examine average check size and customer spending  
- Segment data by size, category, or other dimensions  

---

## 🧩 SQL Analysis

The project includes a set of SQL scripts implementing key queries:

1. **Total Orders & Revenue**
    ```sql
    SELECT COUNT(*) AS total_orders, SUM(quantity * price) AS total_revenue 
    FROM orders;
    ```

2. **Top 5 Selling Pizzas**
    ```sql
    SELECT p.name, SUM(o.quantity) AS sold_qty
    FROM orders o
    JOIN pizzas p ON o.pizza_id = p.pizza_id
    GROUP BY p.name
    ORDER BY sold_qty DESC
    LIMIT 5;
    ```

3. **Sales Distribution by Hour**
4. **Revenue Contribution by Pizza Category**
5. **Top Revenue Pizza Each Month**
6. **Revenue Share by Pizza Size**

---

## 📋 Tools & Tech

- **SQL dialect**: MySQL   
- **IDE**: MySQL Workbench 
- **Scripts included**:  

---

## ✅ How to Run

1. **Clone this repo**  
   ```bash
   git clone https://github.com/Bishakhakapur/Sales-Analysis-SQL.git
