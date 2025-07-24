
# 🛍️ Retail Orders Data Analysis Project

## 🎯 Objective
Conduct a complete end-to-end data analysis pipeline to uncover key business insights from a retail orders dataset. The project spans data ingestion, transformation, SQL querying, DAX modeling, and dashboard visualization.

---

## 📈 Dashboard Preview

![Dashboard Screenshot](Screenshot2025-07-24151647.png)

---

## 📌 Key Insights

- 🔝 Top-performing products identified by sub-category and region
- 🌍 West region had the highest total sales; South the lowest
- 📦 Distribution of total quantity and profit across regions
- 📅 Clear month-over-month trend analysis using line charts
- 📊 Profits and sales contribution by product categories and sub-categories

---

## 🛠️ Tools & Skills Used

| Phase              | Tools / Technologies |
|--------------------|----------------------|
| Data Sourcing      | Kaggle API (Python) |
| Data Cleaning      | Python (pandas, Jupyter in VS Code) |
| Data Storage       | SQL Server (SSMS) |
| Data Transfer      | SQLAlchemy |
| Querying           | SQL |
| Visualization      | Power BI |
| Analytics          | DAX (Power BI Measures) |
| Version Control    | Git, GitHub |

---

## 🔄 Workflow Summary

1. 📥 Pulled dataset using **Kaggle API**
2. 🧹 Cleaned and transformed using **pandas** in **Jupyter Notebook VSCode**
3. 💾 Pushed cleaned data into **SQL Server Management Studio (SSMS)** using **SQLAlchemy**
4. 🔍 Queried data in **SSMS** to extract insights like top products and sales per region
5. 📊 Built a full **Power BI dashboard** using DAX to calculate KPIs
6. 🚀 Uploaded project to **GitHub** with clean structure and documentation

---

## 📊 Power BI Dashboard Features

- ✅ KPIs: 
  - Total Quantity: **379M**
  - Total Sales: **22bn**
  - Total Orders: **100M**
  - Average Sales: **2M**
  - Total Profit: **205K**

- 📌 Visuals:
  - Pie Charts: Quantity and Profit by Region
  - Bar Charts: Sales by Category, Sub-category, and Region
  - Line Chart: Monthly Sales Trend (2022 & 2023)
  - Map: Regional sales across North America

---

## 🧠 DAX Measures Used

```dax
Total Sales = SUM(orders[sale_price])
Total Orders = DISTINCTCOUNT(orders[order_id])
Total Quantity = SUM(orders[quantity])
Average Sales = DIVIDE([Total Sales], [Total Orders])
Total Profit = SUM(orders[profit])
Sales % of Total = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(orders)))
Product Rank = RANKX(ALL(orders[product]), [Total Sales], , DESC)
```

---

## 🗂️ Project Structure

```
RetailOrdersProject/
├── data/
│   └── orders.csv
├── notebooks/
│   └── retail_analysis.ipynb
├── sql/
│   ├── push_to_sql.sql
│   └── queries.sql
├── dashboard/
│   ├── powerbi_dashboard.pbix
│   └── Screenshot_2025-07-24_151647.png
├── README.md
```

---

## 🚀 How to Run This Project

1. Clone this repository:
   ```bash
   git clone https://github.com/debkanta-12102002/orders_analysis.git
   ```

2. Run Jupyter notebook:
   - Open `Data_Processing.ipynb` in VS Code
   - Run all cells to process data and push to SQL

3. Launch Power BI Dashboard:
   - Open `df_orders_dashboard.pbix` in Power BI Desktop
   - Refresh if connected to your local SQL Server

---


