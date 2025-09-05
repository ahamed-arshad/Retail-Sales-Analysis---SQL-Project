📊 Retail Sales Analysis SQL Project
====================================

📌 **Project Overview**
-----------------------

> This project provides a comprehensive demonstration of applying **SQL for retail sales analysis**. Designed for beginner to intermediate analysts, it simulates a real-world workflow where raw transactional data is transformed into strategic business insights.

*   **Complete Data Lifecycle:** The analysis covers the entire process from end to end:
    
    *   📂 **Database Engineering**: Creating and structuring a relational database from scratch.
        
    *   🧹 **Data Integrity**: Cleaning, validating, and preparing the dataset for analysis.
        
    *   🔎 **Exploratory Data Analysis (EDA)**: Uncovering initial patterns, distributions, and anomalies.
        
    *   📊 **Insight Generation**: Answering critical business questions through targeted SQL queries.
        
*   **Core Objective**: To bridge the gap between technical **SQL** execution and practical **business intelligence**, showcasing how data can directly inform and optimize decision-making.
    
*   **Level**: _Beginner-to-Intermediate_
    
*   **Database**: `p1_retail_db`
    

* * *

🎯 **Key Objectives**
---------------------

*   **Database Setup**: To construct a robust and structured database (`p1_retail_db`) to house retail sales data efficiently.
    
*   **Data Quality Assurance**: To identify and rectify inconsistencies, null values, and invalid records to ensure data reliability.
    
*   **Exploratory Analysis**: To understand the fundamental characteristics of the dataset, including sales distributions, customer demographics, and product category performance.
    
*   **Derive Business Insights**: To formulate and answer specific business questions using SQL queries, translating data into actionable recommendations.
    

* * *

🏗️ **Project Workflow & Structure**
------------------------------------

### **1\. Database and Table Setup**

*   **Action**: The foundation of the project involved creating a dedicated database and a well-defined table to store transactional records.
    
*   **Database Creation**: A new database named `p1_retail_db` was initialized.
    
*   **Table Schema**: The `retail_sales` table was designed with columns for transaction details, customer information, product specifics, and key sales metrics.
    

SQL

    -- Create the database
    CREATE DATABASE p1_retail_db;
    
    -- Switch to the newly created database
    USE p1_retail_db;
    
    -- Define the table schema for retail sales data
    CREATE TABLE retail_sales (
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

### **2\. Data Exploration & Cleaning**

*   **Action**: Initial queries were run to understand the dataset's scope and to perform necessary cleaning operations.
    
*   **Tasks Performed**:
    
    *   **Record Count**: Determined the total volume of transactions.
        
    *   **Unique Customers**: Calculated the size of the distinct customer base.
        
    *   **Product Categories**: Listed all unique product categories.
        
    *   **Null Value Checks**: Identified and removed incomplete records to ensure data integrity.
        

SQL

    -- Calculate the total number of records
    SELECT COUNT(*) AS total_records FROM retail_sales;
    
    -- Identify the number of distinct customers
    SELECT COUNT(DISTINCT customer_id) AS unique_customers FROM retail_sales;
    
    -- List all unique product categories
    SELECT DISTINCT category FROM retail_sales;
    
    -- Delete incomplete records to ensure data quality for analysis
    DELETE FROM retail_sales
    WHERE sale_date IS NULL
       OR sale_time IS NULL
       OR customer_id IS NULL
       OR gender IS NULL
       OR age IS NULL
       OR category IS NULL
       OR quantity IS NULL
       OR price_per_unit IS NULL
       OR cogs IS NULL; 

### **3\. Data Analysis & Answering Business Questions**

*   **Action**: A series of targeted SQL queries were developed to extract meaningful insights from the cleaned data.
    
*   **Key Business Questions Addressed**:
    
    1.  _What were the total sales on a specific date (e.g., '2022-11-05')?_
        
    2.  _Which transactions in the 'Clothing' category had high quantities in November 2022?_
        
    3.  _How do total sales and order counts break down by product category?_
        
    4.  _What is the average age of customers purchasing 'Beauty' products?_
        
    5.  _Can we identify all high-value transactions where the total sale exceeded $1000?_
        
    6.  _What is the transaction count for each gender within each product category?_
        
    7.  _Which month generated the highest sales revenue for each year on record?_
        
    8.  _Who are the top 5 customers by total spending?_
        
    9.  _How many unique customers has each product category attracted?_
        
    10.  _How does sales volume vary by time of day (Morning, Afternoon, Evening)?_
        

* * *

### 📊 **Key Findings**

*   👥 **Customer Demographics**: The _'Beauty'_ and _'Clothing'_ categories successfully attract a wide range of age groups, indicating broad market appeal.
    
*   💰 **High-Value Sales**: A notable number of transactions exceed **$1000**, pointing to significant bulk or premium product purchases.
    
*   📈 **Seasonal Trends**: Analysis revealed clear seasonality, with certain months consistently showing peak sales performance, which is crucial for inventory and marketing planning.
    
*   🏆 **Top Customer Contribution**: A small subset of high-spending customers accounts for a disproportionately large share of total revenue, highlighting the importance of customer loyalty programs.
    
*   ⏰ **Shift-Based Insights**: Customer purchasing patterns differ significantly across morning, afternoon, and evening shifts, suggesting opportunities for targeted promotions.
    

* * *

### 📄 **Reports & Deliverables**

*   **Sales Performance Summary**: A consolidated report detailing total revenue, transaction volumes, and sales contributions by category.
    
*   **Trend Analysis Report**: An analysis of month-over-month sales patterns to identify growth and seasonality.
    
*   **Customer Segmentation Insights**: A report identifying top spenders, category-specific customer counts, and key demographic trends.
    

* * *

🏁 **Conclusion**
-----------------

*   This project serves as a practical case study for aspiring data analysts, effectively merging technical **SQL skills** with **strategic business analysis**.
    
*   It demonstrates a repeatable framework for how an analyst can support decision-making, uncover customer behavior patterns, and help optimize sales performance.
    
*   By completing this project, one not only enhances **SQL proficiency** but also develops the critical ability to translate complex business challenges into clear, data-driven solutions.
    

* * *

⚙️ **Prerequisites**
--------------------

*   A functioning **SQL environment** (e.g., _PostgreSQL_, _MySQL_, _SQL Server_).
    
*   Basic understanding of **SQL commands** (_DDL_, _DML_, _Joins_, _Aggregate Functions_).
    
*   A **SQL client** for executing queries (e.g., _pgAdmin_, _MySQL Workbench_, _DBeaver_, or a _VS Code extension_).
    

* * *

🚀 **How to Run This Project**
------------------------------

1.  **Clone the Repository:**
    
    Bash
    
        git clone https://github.com/ahamed-arshad/Retail-Sales-Analysis---SQL-Project.git 
2.  **Database Setup**: Open your **SQL client**, connect to your database server, and run the SQL script to create the `p1_retail_db` database and the `retail_sales` table.
    
3.  **Data Import**: Import the provided dataset (e.g., from a `.csv` file) into the `retail_sales` table.
    
4.  **Execute Queries**: Run the analysis queries from the `queries.sql` file to explore the data and generate insights.
    
5.  **Review Results**: Analyze the output from the queries and compare them with the key findings and reports.
    

* * *

🔮 **Future Enhancements**
--------------------------

*   **BI Dashboard Integration**: Connect the database to **Power BI** or **Tableau** to create interactive visualizations and dashboards.
    
*   **Advanced SQL**: Implement more complex techniques like **Window Functions**, **Common Table Expressions (CTEs)**, and **Stored Procedures** for deeper analysis and automation.
    
*   **Predictive Analytics**: Incorporate sales forecasting models to predict future trends.
    
*   **Extended Analysis with Python**: Use **Python** (_Pandas_, _Matplotlib_) for more advanced statistical analysis and data visualization.
    

* * *

🧑‍💻 **Author**
----------------

### **Ahmed Arshad**

_Data Analyst | SQL Enthusiast | Turning Raw Data into Insights_
