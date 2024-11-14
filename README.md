# Adidas Sales Analysis Project

This project showcases a comprehensive analysis of Adidas sales data, leveraging Excel Power Query for data cleaning, SQL Server for in-depth analysis, and Power BI for interactive visualizations. The goal was to derive actionable insights into product performance, customer demographics, and regional sales to guide decisions in sales, marketing, and inventory planning.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Data Cleaning with Excel Power Query](#data-cleaning-with-excel-power-query)
  - [Steps](#steps)
- [SQL Server Analysis](#sql-server-analysis)
  - [Key SQL Queries](#key-sql-queries)
    - [Top Performing Products](#1-top-performing-products)
    - [Monthly Sales Trends](#2-monthly-sales-trends)
    - [Regional Performance](#3-regional-performance)
- [Power BI Visualization](#power-bi-visualization)
  - [Key Visualizations](#key-visualizations)
- [Key Findings](#key-findings)
- [Project Files](#project-files)
- [Conclusion](#conclusion)

---

## Project Overview

- **Data Source**: Adidas Sales Dataset
- **Tools**: Excel Power Query, SQL Server, Power BI
- **Objectives**:
  - Clean and transform raw sales data for analysis
  - Conduct time-based and product-based sales analysis
  - Visualize trends for actionable insights across key business areas

---

## Data Cleaning with Excel Power Query

The data was cleaned and transformed in Excel Power Query to ensure consistency and prepare for analysis.

### Steps
1. **Removed Duplicates**: Ensured data integrity by eliminating duplicate entries.
2. **Handled Missing Values**: Applied fill-down and replacement methods to manage null values.
3. **Filtered Columns**: Removed non-essential columns for a streamlined dataset.
4. **Standardized Column Names**: Renamed columns for compatibility across tools.
5. **Unpivoted Data**: Transformed month-based columns to facilitate time-based analysis.
6. **Created Calculated Columns**: Generated custom columns for profit margin and quarter extraction.

*Example Power Query Step for Unpivoting*:
   ```plaintext
   Transform > Unpivot Columns
   ```

7. **Export to SQL Server**: Saved the cleaned data in CSV format and loaded it into SQL Server for further analysis.

---

## SQL Server Analysis

Using SQL Server, I performed data analysis to uncover insights on sales trends, product performance, and regional distribution.

### Key SQL Queries

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

In Power BI, I created an interactive dashboard to visualize Adidas’s sales data, enabling dynamic filtering and deep dives into key metrics.

### Key Visualizations

1. **Sales by Product**: Bar chart showing total sales and profit by product category.
2. **Monthly Sales Trend**: Line graph illustrating sales trends over months for seasonality insights.
3. **Regional Sales Performance**: Map visualization for geographic sales distribution.
4. **Profit Margin by Product**: Scatter plot showing profit margin across different products.

---

## Key Findings

1. **Top Products**: Certain product categories emerged as high-revenue drivers, offering opportunities for strategic promotions.
2. **Seasonality in Sales**: Peaks in Q2 and Q4 indicate opportunities for holiday and seasonal marketing.
3. **Regional Differences**: Certain regions show higher growth rates, suggesting potential for regional-focused strategies.
4. **Profit Margins**: Products with higher profit margins but lower sales volumes may benefit from targeted upselling.

---

## Project Files

- `Adidas Sales Dataset.xlsx`: Raw dataset used for the analysis.
- `Data Cleaning Script.txt`: Excel Power Query script for data cleaning and transformation.
- `SQL Queries.sql`: SQL Server queries for analysis.
- `Power BI Dashboard.pbix`: Power BI file with interactive dashboards.
- `README.md`: Project documentation.

---

## Conclusion

This project demonstrates a full data analysis pipeline, from data cleaning and transformation to analysis and visualization. By using Excel, SQL, and Power BI, this project exemplifies a strategic approach to transforming raw data into insights for decision-making across Adidas’s business areas.

---

Copy this documentation into GitHub (README.md) or your portfolio website to effectively present your project, skills, and insights in data analysis.
