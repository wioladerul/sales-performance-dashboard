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

# Dashboard Component
The dashboard includes the following visualizations:
1. Key Business Metrics: Displays Total Sales, Total Profit, Profit Margin, Total Orders, and Total Quantity.
2. Monthly Sales and Profit Trend: Shows changes in sales and profit over time.
3. Profitability by State: Compares Total Sales, Total Profit, and Profit Margin across states.
4. Sales Distribution by Category: Shows the contribution of each product category to total sales.
5. Sales Distribution by Segment: Compares sales across customer segments.
6. Sales by Sub-Category: Compares sales values across product sub-categories.
7. Profit by Sub-Category: Compares profit across product sub-categories.

# Interactive Filters
The dashboard includes three filters:
- Year: Filters the report by year.
- Region: Filters the report by geographical region.
- Category: Filters the report by product category.

# Key Insights
1. Monthly sales from 2014 to 2017 fluctuated throughout the year, with significant increases in March and September, followed by declines in April and October. Sales remained relatively stable from May to August before increasing significantly in September. After declining in October, sales rose sharply in November, reaching the highest value of approximately $352.46K. In December, sales decreased to approximately $325.29K, but remained relatively high compared with most other months.

Profit followed a broadly similar pattern. The highest monthly profit was recorded in December at approximately $43.37K, while the lowest occurred in January at approximately $9.13K. Profit increased significantly in March and September, although fluctuations occurred in several other months.

Overall, sales and profit generally moved in the same direction. However, their movements were not always proportional. This is evident in November, when sales reached their highest level, but profit was lower than in December. Conversely, December recorded the highest profit of $43.37K, despite having lower sales than November. These findings indicate that the month with the highest sales does not necessarily generate the highest profit.

2. Technology generated the highest sales among the three product categories, contributing approximately $836.15K, or 36.4% of total sales. This makes Technology the largest category by sales contribution in the analyzed dataset. The result indicates that Technology plays an important role in overall sales performance.

3. The Consumer segment generated approximately $1,161.40K in sales, accounting for 50.56% of total sales. This makes Consumer the largest contributor to sales compared with the Corporate and Home Office segments. The result shows that more than half of the recorded sales came from Consumer customers. Therefore, this segment represents an important part of the sales distribution in the dataset.

4. The Phones sub-category generated the highest sales, amounting to $330,007.05K, while Copiers recorded the highest profit at $55,617.82K. In contrast, Tables recorded the lowest profit, with a loss of $17,725.48K. Additionally, Bookcases and Supplies also incurred losses of $3,472.56K and $1,189.10K, respectively.

These findings show that the sub-category with the highest sales does not necessarily generate the highest profit. Phones led in sales, while Copiers generated the highest profit. Meanwhile, Tables experienced the largest loss, highlighting differences in profitability across product sub-categories.

5. California recorded the highest total sales at $457,687.63K and the highest total profit at $76,381.39K, making it the leading state in terms of sales and profit. Meanwhile, District of Columbia achieved the highest profit margin at 36.98%, with total sales of $2,865.02K and total profit of $1,095.59K.

These findings indicate that the state with the highest sales and total profit does not necessarily have the highest profit margin. Although California generated the largest sales and profit, District of Columbia achieved a higher profit margin, indicating a greater proportion of profit relative to sales.
