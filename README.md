# Adidas-Sales-Analysis-Project

Here’s a comprehensive GitHub and portfolio documentation template that incorporates all the steps for cleaning, analyzing, and visualizing Adidas sales data with Excel, SQL, and Power BI. This template is structured for clarity, showcasing your process and insights to prospective employers or clients.

---

### **GitHub Documentation**

**Repository Title**: *Adidas Sales Analysis Project*

---

#### **README.md**

```markdown
# Adidas Sales Analysis Project

This project provides a full analysis of Adidas sales data to derive actionable insights using Excel, SQL Server, and Power BI. Each tool is utilized in a specific capacity: Excel for data cleaning and transformation, SQL Server for in-depth analysis, and Power BI for interactive visualization. This project demonstrates expertise in data cleaning, ETL processes, SQL queries, and data visualization to uncover trends in product performance, customer demographics, and regional sales.

---

## Project Overview

- **Data Source**: Adidas Sales Dataset
- **Tools**: Excel (Power Query), SQL Server, Power BI
- **Key Objectives**:
  - Clean and transform raw sales data
  - Perform time-based and product-based sales analysis
  - Visualize trends for actionable insights in sales, marketing, and inventory management

---

## Table of Contents

1. [Data Cleaning in Excel Power Query](#data-cleaning-in-excel-power-query)
2. [SQL Server Analysis](#sql-server-analysis)
3. [Power BI Visualization](#power-bi-visualization)
4. [Insights and Findings](#insights-and-findings)

---

## Data Cleaning in Excel Power Query

### Steps:
1. **Load the Data**: Imported the dataset into Excel and launched Power Query for transformations.
2. **Remove Duplicates**: Cleaned the data by removing any duplicate entries to ensure data integrity.
3. **Handle Missing Values**: Used fill-down and replacement methods to manage null values.
4. **Filter Unnecessary Data**: Removed non-essential columns to streamline the dataset.
5. **Rename Columns**: Standardized column names for compatibility with SQL and Power BI.
6. **Unpivot Data for Time Analysis**: Unpivoted month-based columns to prepare for time-series analysis.
7. **Create Custom Columns**: Generated new columns to calculate profit margin and extract quarters.

   *Code Example for Unpivoting in Power Query*:
   ```excel
   // Unpivot selected columns for month-based sales data
   Transform > Unpivot Columns
   ```

8. **Export to SQL**: Saved the cleaned data in CSV format and imported it into SQL Server.

---

## SQL Server Analysis

In SQL Server, I performed comprehensive data analysis on the cleaned dataset to derive insights on sales trends, product performance, and customer demographics.

### Key Queries

#### 1. Top Performing Products
   ```sql
   SELECT 
       Product,
       SUM(Sales) AS Total_Sales,
       SUM(Operating_Profit) AS Total_Profit
   FROM 
       AdidasSales
   GROUP BY 
       Product
   ORDER BY 
       Total_Sales DESC;
   ```

#### 2. Monthly Sales Trends
   ```sql
   SELECT 
       DATEPART(MONTH, SaleDate) AS Month,
       SUM(Sales) AS Monthly_Sales
   FROM 
       AdidasSales
   GROUP BY 
       DATEPART(MONTH, SaleDate)
   ORDER BY 
       Month;
   ```

#### 3. Regional Performance
   ```sql
   SELECT 
       Region,
       SUM(Sales) AS Regional_Sales,
       AVG(Operating_Margin) AS Avg_Operating_Margin
   FROM 
       AdidasSales
   GROUP BY 
       Region
   ORDER BY 
       Regional_Sales DESC;
   ```

---

## Power BI Visualization

With Power BI, I created an interactive dashboard to visualize the sales data, allowing for dynamic insights into Adidas’s performance across various dimensions.

### Visualizations

1. **Sales by Product**: A bar chart showing the total sales and profit by product category to highlight top-performing items.
2. **Monthly Sales Trend**: A line graph depicting monthly sales trends to identify seasonality and peak periods.
3. **Regional Sales Performance**: A map visualization showing sales distribution across regions for geographic insights.
4. **Profit Margin by Product**: A scatter plot to identify the relationship between profit margin and product sales.

*Screenshot of Power BI Dashboard*

![Power BI Dashboard Screenshot](./assets/power_bi_dashboard.png)

---

## Insights and Findings

Based on the analysis in SQL Server and visualizations in Power BI, here are some key insights:

1. **Top Products**: Products A, B, and C emerged as top sellers with high profitability, indicating potential for focused marketing.
2. **Seasonality in Sales**: Sales peak in Q2 and Q4, likely due to seasonal promotions and holiday purchases.
3. **Regional Differences**: Region X recorded the highest sales, while Region Y shows a strong growth trend. This can inform region-specific marketing strategies.
4. **Profit Margins**: Some low-sales products showed high profit margins, suggesting opportunities for targeted upselling strategies.

---

## Files in Repository

- `Adidas Sales Dataset.xlsx`: Raw dataset used for the analysis.
- `Data Cleaning Script.txt`: Excel Power Query script for data cleaning and transformation.
- `SQL Queries.sql`: SQL Server queries for data analysis.
- `Power BI Dashboard.pbix`: Power BI file for interactive visualizations.
- `README.md`: Project documentation.

---

## How to Run This Project

1. Open `Adidas Sales Dataset.xlsx` in Excel and review the data structure.
2. Follow the Power Query steps to clean and transform data.
3. Use SQL Server to load the cleaned dataset and run the queries provided.
4. Open `Power BI Dashboard.pbix` in Power BI to interact with the visualizations.

---

## Conclusion

This project demonstrates an end-to-end analysis workflow, transforming raw sales data into actionable insights with Excel, SQL, and Power BI. This approach is applicable for businesses seeking to leverage data for strategic decision-making across sales, marketing, and inventory management.

```

---

### **Portfolio Documentation (Hosted on GitHub Pages)**

#### **Project Title**: *Adidas Sales Data Analysis: An End-to-End Approach with Excel, SQL, and Power BI*

#### **Project Summary**

In this project, I conducted a comprehensive analysis of Adidas sales data using Excel, SQL Server, and Power BI. This project demonstrates my ability to clean, analyze, and visualize large datasets, providing actionable insights into sales trends, customer demographics, and product performance.

---

#### **Steps**

1. **Data Cleaning with Excel Power Query**: 
   - Removed duplicates, filled missing values, filtered columns, and unpivoted data to prepare for analysis.

2. **In-Depth Analysis with SQL Server**:
   - Using SQL Server, I explored top-selling products, seasonal sales trends, and regional performance to highlight sales opportunities and challenges.

3. **Data Visualization in Power BI**:
   - Created interactive dashboards to visualize findings, allowing dynamic filtering for detailed insights by product and region.

---

#### **Key Findings**

1. **Top Performers**: Identified high-revenue products and regions that can benefit from targeted promotions.
2. **Seasonal Patterns**: Sales peak during Q2 and Q4, indicating opportunities for strategic seasonal marketing.
3. **Regional Growth**: Identified regions with strong sales growth for targeted expansion.
4. **Profitability Insights**: Uncovered products with high-profit margins that could benefit from upselling.

---

#### **Project Files**

- **Data Cleaning Scripts**: Power Query steps for data preparation.
- **SQL Analysis Scripts**: SQL queries used for deriving insights.
- **Power BI Dashboard**: A dynamic, interactive dashboard for exploring findings.

---

#### **Conclusion**

This project showcases a complete data analysis workflow, highlighting how data cleaning, SQL queries, and data visualizations can drive business decisions in sales and marketing. The analysis provides a clear, structured approach for transforming raw data into strategic insights, making it a strong portfolio project for data analysis roles.

--- 

This documentation structure will clearly present your approach, findings, and technical skills across platforms, making it easy to understand and compelling for your audience.
