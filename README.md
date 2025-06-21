# Olist-Sales-Analysis
Data Analytics Project
 
An end-to-end data analytics project focused on deriving insights from Brazil's Olist e-commerce dataset. This project involves **data cleaning**, **modelling**, and **visual analysis** using tools like **Excel**, **SQL**, **Power BI**, and **Tableau**.

---

## ✅ Project Workflow

### 1. 🧹 Data Cleaning
- Removed null or missing values across key columns (`order_delivered_customer_date`, `payment_type`, etc.)
- Standardized city and state names for consistency
- Converted date columns to proper datetime formats
- Removed duplicates and outliers in price and payment fields

### 2. 🧩 Data Modelling
- Created relational models using customer, order, payment, and review datasets
- Built star schema for reporting purposes
- Defined primary and foreign keys across tables
- Performed data transformations in SQL for integration into Power BI and Tableau

### 3. 📌 Working on Requirements
This project focuses on answering business questions through KPI-based analysis.

---

## 📌 KPI-Based Analysis

### 📅 Weekday vs Weekend – Payment Statistics
**Objective:** Understand customer spending behavior based on order purchase day.

- Used SQL and Excel pivot tables to group orders by weekday/weekend
- Aggregated payment values and number of transactions per group
- Visualized using Power BI bar charts

### 💳 Review Score 5 with Credit Card
**Objective:** Count how many customers gave 5-star reviews when paying by credit card.

- Filtered data in SQL:
  ```sql
  SELECT COUNT(*) 
  FROM orders o
  JOIN reviews r ON o.order_id = r.order_id
  JOIN payments p ON o.order_id = p.order_id
  WHERE r.review_score = 5 AND p.payment_type = 'credit_card';
### 3. 🐾 Avg. Delivery Time for Pet Shop Orders
**Goal:** Calculate delivery time for pet shop products.

- Filtered for `product_category_name = 'pet_shop'`
- Calculated delivery duration:  
  `Delivery Days = order_delivered_customer_date - order_purchase_timestamp`
- Displayed as an average metric

### 4. 🏙️ Sao Paulo – Avg. Price & Payment Value
**Goal:** Analyze customer spend in São Paulo.

- Filtered for `customer_city = 'sao paulo'`
- Calculated:
  - Average product price (`price`)
  - Average payment value (`payment_value`)
- Displayed in summary table

### 5. 🚚 Shipping Days vs Review Scores
**Goal:** Explore the impact of delivery speed on customer satisfaction.

- Calculated:
  - `Shipping Days = order_delivered_customer_date - order_purchase_timestamp`
- Plotted `Shipping Days` vs `Review Score` in scatter plot to observe trend


  ## Tools & Technologies

| Tool               | Role                                                |
|--------------------|-----------------------------------------------------|
| **Excel And SQL**  | Data Cleaning, Initial Data Modelling               |
| **Power BI**       | Interactive visualizations & dashboard creation     |
| **Tableau**        | Deep-dive data visualization & analysis             |

## 📂 Dataset

This project uses the [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) from Kaggle, which includes:

- Orders
- Customers
- Order Items
- Products
- Payments
- Reviews
- Geolocation

---

## 📸 Dashboard Snapshots

- 📊 Power BI Dashboard: ![Screenshot 2025-05-24 200907](https://github.com/user-attachments/assets/6fea288f-dfa9-49c4-982b-c21ed1d41acc)
- 📈 Tableau Dashboard: ![Screenshot 2025-05-24 200907](https://github.com/user-attachments/assets/2cd443bd-9864-40ff-b5e1-b85e6502998c)


---

## 🎯 Outcomes

- Delivered key metrics for business decisions
- Demonstrated customer behavior patterns
- Built clean and interactive dashboards for stakeholders

---

## 🤝 Let's Connect

If you're interested in analytics, BI tools, or collaborating, feel free to connect!

📬 https://www.linkedin.com/in/vidhyashree-a-s/ 
📧 vidhyashree54321@gmail.com

---

**⭐ Don’t forget to star the repo if you found it useful!**

*Happy Analyzing!*
