# sales-performance-dashboard

# Project Overview
This project focuses on analyzing Superstore sales data using Microsoft Power BI to gain a better understanding of business performance from 2014 to 2017. Using the Sample Superstore dataset obtained from Kaggle, I explored sales trends, profitability, product performance, and customer segments to identify patterns and areas that may require further attention.

The project involves preparing and analyzing the data, creating key business metrics, and presenting the results through an interactive dashboard. The dashboard allows users to explore sales and profit across different time periods, product categories, customer segments, and geographical regions using interactive filters and visualizations.

Through this project, I aim to develop my skills in data analysis, data visualization, and business insight generation. Beyond presenting numbers, this analysis encourages a closer look at what the data reveals about sales performance and profitability, providing a foundation for more informed, data-driven business decisions.

# Project Objectives
The main objectives of this project are to:
- Analyze monthly sales and profit trends from 2014 to 2017 to understand changes in business performance over time.
- Compare sales distribution across product categories and customer segments to understand their respective contributions to total sales.
- Analyze sales and profit by product sub-category to identify differences in performance across sub-categories.
- Evaluate profitability by state by comparing total sales, total profit, and profit margin.
- Develop an interactive Power BI dashboard with year, region, and category filters, allowing users to explore the data based on their needs.

# Business Questions
This analysis aims to answer the following business questions:
1. How do monthly sales and profit change over the 2014–2017 period?
2. Which product categories contribute the most to total sales?
3. Which customer segments contribute the most to total sales?
4. Which product sub-categories generate the highest sales and profit, and which generate the lowest profit?
5. How do total sales, total profit, and profit margin differ across states?
These questions provide a structure for exploring the dataset and identifying patterns that may be relevant to business performance.

# Dataset
The dataset used in this project is Sample Superstore, obtained from Kaggle. It contains sales transaction data from 2014 to 2017.

The dataset includes the following columns: Row ID, Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Customer Name, Segment, Country, City, State, Postal Code, Region, Product ID, Category, Sub-Category, Product Name, Sales, Quantity, Discount, and Profit.

This dataset is used for learning and data analysis practice. Therefore, the findings do not directly represent the actual operational performance of a real company.
**Dataset source:** https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

# Data Preparation and Analysis
Before developing the dashboard, the dataset should be inspected to ensure that its structure and values are suitable for analysis.

The preparation process includes:
1. Reviewing column names and data types.
2. Ensuring that Order Date and Ship Date are recognized as date fields.
3. Checking that Sales, Profit, Quantity, and Discount use appropriate numeric data types.
4. Reviewing missing values and potential data-quality issues.
5. Creating DAX measures for the dashboard

DAX measures were created to summarize the main business metrics used in the report.
- Total Sales: Total sales revenue
- Total Profit: Total profit earned from sales
- Profit Margin: Total profit divided by total sales, expressed as a percentage
- Total Orders: Number of unique orders based on Order ID
- Total Quantity: Total quantity of products sold

The following DAX measures were used:
- Total Sales = SUM('Sample - Superstore'[Sales])
- Total Profit = SUM('Sample - Superstore'[Profit])
- Profit Margin = DIVIDE(SUM('Sample - Superstore'[Profit]), SUM('Sample - Superstore'[Sales]), 0)
- Total Orders = DISTINCTCOUNT('Sample - Superstore'[Order ID])
- Total Quantity = SUM('Sample - Superstore'[Quantity])

# Dashboard Preview
![Superstore Sales Dashboard](Superstore%20Sales%20Dashboard.jpg)
