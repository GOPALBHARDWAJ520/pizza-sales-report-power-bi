
# 🍕 Pizza Sales Dashboard Project

## 📌 Problem Statement

The objective of this project is to analyze key performance indicators (KPIs) and visualize insights from pizza sales data to assess business performance using Power BI.

---

## 🎯 Project Goals

- Identify trends in pizza orders over time.
- Evaluate sales performance across categories and sizes.
- Discover top and bottom-performing pizzas.
- Provide actionable insights through visual dashboards.

---

## ✅ KPI Metrics

The following KPIs are calculated:

- **Total Revenue**: Sum of total price of all pizza orders.
- **Average Order Value**: Total revenue ÷ Total number of orders.
- **Total Pizzas Sold**: Sum of the quantity of all pizzas sold.
- **Total Orders**: Total number of orders placed.
- **Average Pizzas Per Order**: Total pizzas sold ÷ Total number of orders.

---

## 📊 Dashboard Visuals


<img width="1365" height="725" alt="image" src="https://github.com/user-attachments/assets/d14e2a22-6cfb-4c77-a257-78c67606f22a" />



<img width="1410" height="732" alt="image" src="https://github.com/user-attachments/assets/efd51bb4-48fc-49f9-9d1a-08490145ec88" />



### 📈 Trends

- **Daily Trend for Total Orders**: Bar chart of orders per day.
- **Monthly Trend for Total Orders**: Line chart showing hourly order trends.

### 🍕 Category-wise Insights

- **% of Sales by Pizza Category**: Pie chart by pizza category.
- **% of Sales by Pizza Size**: Pie chart by pizza size.
- **Total Pizzas Sold by Category**: Funnel chart of total pizzas sold per category.

### 🏆 Performance Analysis

- **Top 5 Best Sellers**: Bar chart by Revenue, Quantity, and Orders.
- **Bottom 5 Sellers**: Bar chart for least-selling pizzas by Revenue, Quantity, and Orders.

---

## 🛠️ Tools & Technologies

- **Excel/MS Office** – Data pre-processing and overview.
- **MS SQL Server** – Data querying and transformation.
- **SSMS (SQL Server Management Studio)** – SQL execution.
- **Power BI** – Dashboard creation and visualization.

---

## 📌 Step-by-Step Guide to Recreate This Dashboard

### 1. **Data Collection & Preparation**
- Extract pizza sales data from Excel or CSV format.
- Load it into **SQL Server** or **Power BI** directly (Power Query).
- Ensure tables for orders, order details, pizzas, and pizza types are available.

### 2. **Data Cleaning**
- Remove duplicates and nulls.
- Convert data types (e.g., date formats).
- Create calculated columns (e.g., total price = quantity × unit price).

### 3. **SQL Queries (If Using SSMS)**
```sql
-- Example: Total Revenue
SELECT SUM(quantity * price) AS total_revenue FROM order_details;

-- Example: Total Orders
SELECT COUNT(DISTINCT order_id) AS total_orders FROM orders;
```

### 4. **Load Data into Power BI**
- Use **Get Data → SQL Server / Excel** to connect your data source.
- Load all relevant tables into the Power BI data model.
- Manage relationships between tables (e.g., Orders ↔ Order Details ↔ Pizzas).

### 5. **Create Measures in Power BI**
Use DAX formulas to create KPIs:

```DAX
Total Revenue = SUM(order_details[total_price])
Total Orders = DISTINCTCOUNT(order_details[order_id])
Total Pizzas Sold = SUM(order_details[quantity])
Avg Order Value = [Total Revenue] / [Total Orders]
Avg Pizzas Per Order = [Total Pizzas Sold] / [Total Orders]
```

### 6. **Build Visualizations**
- Use **Bar, Line, Funnel, and Pie charts**.
- Drag fields into the visual pane.
- Apply filters/slicers for interactive analysis (e.g., by Category or Size).

### 7. **Design Tips**
- Use clean and minimalistic color schemes.
- Group visuals by insights (Trends, Category, Performance).
- Add titles, legends, and labels to every visual for clarity.

### 8. **Publish**
- Publish your report to **Power BI Service**.
- Share the dashboard with stakeholders or embed it into web apps.

---

## 📁 Files Included

- `PIZZA SALES REPORT.pbix` – Final Power BI dashboard file.
- `pizza sales dashboard problem statement.docx` – Project brief and requirements.

---

## 🤝 Contributing

Feel free to fork this repo and enhance the visuals, add forecasting models, or integrate more data!

---

## 📬 Contact

For any questions or suggestions:
**Gopal Bhardwaj**  
📧 [bhardwaj520gopal@gmail.com]  
📍 India

---

⭐ *If you found this project helpful, feel free to star the repo and share it with your network!*
