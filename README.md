# Retail Sales Analysis SQL Project  

## 📌 Project Overview  

**Project Title**: Retail Sales Analysis  
**Level**: Beginner-to-Intermediate  
**Database**: `p1_retail_db`  

This project demonstrates practical SQL applications for **retail sales analytics**, simulating real-world scenarios where businesses leverage data to optimize decision-making. It covers the **end-to-end workflow**:  

- 📂 Database creation  
- 🧹 Data cleaning and validation  
- 🔎 Exploratory data analysis (EDA)  
- 📊 Business-driven SQL queries  

The goal is not only technical but also **business-oriented**, showcasing how raw transactional data can be transformed into **actionable insights**.  

---

## 🎯 Objectives  

- **Database Setup**: Build a structured database to store retail sales data.  
- **Data Quality & Cleaning**: Identify and handle missing or invalid records.  
- **Exploratory Data Analysis (EDA)**: Understand dataset distributions, anomalies, and patterns.  
- **Business Insights**: Solve business questions using SQL queries.  

---

## 🏗️ Project Structure  

### 1. Database Setup  

- **Database Creation**: A new database `p1_retail_db` was created.  
- **Table Creation**: A table `retail_sales` was designed to capture transactional data including customer demographics, product categories, and sales metrics.  

```sql
CREATE DATABASE p1_retail_db;

CREATE TABLE retail_sales
(
    transactions_id INT PRIMARY KEY,
    sale_date DATE,	
    sale_time TIME,
    customer_id INT,	
    gender VARCHAR(10),
    age INT,
    category VARCHAR(35),
    quantity INT,
    price_per_unit FLOAT,	
    cogs FLOAT,
    total_sale FLOAT
);

### 2. Data Exploration & Cleaning

- **Record Count**: Calculate the total number of records.
- **Customer Count**: Identify the number of distinct customers.
- **Category Count**: List all unique product categories.
- **Null Value Check**: Detect and remove missing or invalid records.

-- Total records
SELECT COUNT(*) FROM retail_sales;

-- Unique customers
SELECT COUNT(DISTINCT customer_id) FROM retail_sales;

-- Categories
SELECT DISTINCT category FROM retail_sales;

-- Null value detection
SELECT * FROM retail_sales
WHERE 
    sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL OR 
    gender IS NULL OR age IS NULL OR category IS NULL OR 
    quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;

-- Delete incomplete records
DELETE FROM retail_sales
WHERE 
    sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL OR 
    gender IS NULL OR age IS NULL OR category IS NULL OR 
    quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;

### 3. Data Analysis & Business Questions

SQL queries were written to address business-driven questions, including:

- 1. Retrieve sales on a specific date (2022-11-05).

- 2. Find high-volume Clothing sales in Nov 2022.

- 3. Calculate total sales and order counts by category.

- 4. Determine the average age of Beauty customers.

- 5. Identify high-value transactions (total_sale > 1000).

- 6. Count gender-wise transactions across categories.

- 7. Find the best-selling month each year.

- 8. Identify the top 5 customers by sales.

- 9. Count unique customers per category.

- 10. Analyze sales distribution by shift (Morning, Afternoon, Evening).

### 📊 Key Findings

- 👥 **Customer Demographics**: Beauty and Clothing categories attract diverse age groups.

- 💰 **Premium Sales**: Transactions above 1000 highlight bulk/premium purchases.

 - 📈 **Seasonality**: Certain months consistently outperform others, revealing peak sales periods.

- 🏆 **Top Customers**: A small percentage of customers drive a majority of revenue.

- ⏰ **Shift Insights**: Buying behavior varies across Morning, Afternoon, and Evening.

## Reports

- **Sales Performance Summary**: Total revenue, transaction counts, and category contributions.
- **Trend Analysis**: Month-over-month patterns and seasonality.
- **Customer Insights**: Top spenders, unique customers per category, and demographic trends.

## Conclusion

This project serves as a comprehensive SQL case study for data analysts, blending technical skills with business-driven insights. It demonstrates how analysts can:

- Support strategic decision-making

- Understand customer behavior

- Optimize sales and product performance

By completing this project, one not only builds SQL proficiency but also the ability to translate business challenges into data-driven solutions.

##⚙️ Prerequisites

- SQL environment (PostgreSQL, MySQL, or equivalent)

- Basic knowledge of SQL commands (DDL, DML, Joins, Aggregations)

- Access to a SQL client (pgAdmin, MySQL Workbench, or VS Code SQL extension)

## 🚀 How to Run

- 1. Clone this repository:
        git clone https://github.com/ahamed-arshad/Retail-Sales-Analysis---SQL-Project.git

- 2. Open your SQL environment and run the database setup script.

- 3. Import or insert retail sales dataset into retail_sales table.

- 4. Execute analysis queries from the queries.sql file.

- 5. Review findings and compare with provided reports.

## 🔮 Future Enhancements

- Integration with Power BI/Tableau for visualization.

- Advanced SQL techniques (Window Functions, CTE optimizations, Stored Procedures).

- Incorporation of predictive analytics for sales forecasting.

- Adding Python/Pandas scripts for extended analysis.

## 🧑‍💻 Author

Ahmed Arshad
Data Analyst | SQL Enthusiast | Turning Raw Data into Insights
