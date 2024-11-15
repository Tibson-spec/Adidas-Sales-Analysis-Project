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

- Data Source: Adidas Sales Dataset(Kaggle)
- Tools: Excel Power Query, SQL Server, Power BI
- Objectives:
  - Clean and transform raw sales data for analysis
  - Conduct time-based and product-based sales analysis
  - Visualize trends for actionable insights across key business areas

---

## Data Cleaning with Excel Power Query

The data was cleaned and transformed in Excel Power Query to ensure consistency and prepare for analysis.

### Steps
1. Removed Duplicates: Ensured data integrity by eliminating duplicate entries.
3. Filtered Columns: Removed non-essential columns for a streamlined dataset.
4. Standardized Column Names: Renamed columns for compatibility across tools and Used first row as header
5. Export to SQL Server: Saved the cleaned data in Excel format and loaded it into SQL Server for further analysis.

---

## SQL Server Analysis

Using SQL Server, I performed data analysis to uncover insights on sales trends, product performance, and regional distribution.

### Key SQL Queries

#### 1. Top Performing Products
 ```sql
 SELECT
    Product,
    SUM([Units Sold]) AS Total_Units_Sold
FROM 
    ['Data_Sales _Adidas]
GROUP BY 
    Product
ORDER BY 
    Total_Units_Sold DESC;
 ```
#### 2. Monthly Sales Trends
  ```sql
 SELECT d.MonthName, 
       d.Year, 
       SUM(s.[Total Sales]) AS MonthlySales
FROM ['Data_Sales _Adidas] s
JOIN DateTable d ON s.[Invoice Date] = d.Invoicedate
GROUP BY d.MonthName, 
         d.Year
ORDER BY MonthlySales DESC;
   ```

#### 3. Regional Performance
   ```sql
  SELECT 
   Region,
   SUM([Units Sold]) AS TotalUnitSold,
   SUM([Total Sales]) AS TotalSalesAmount
FROM 
    ['Data_Sales _Adidas] s
JOIN Location l ON s.[Location Key] = l.LocationKey
GROUP BY 
    Region
ORDER BY 
     TotalSalesAmount DESC;

   ```

---

## Power BI Visualization

In Power BI, I created an interactive dashboard to visualize Adidas’s sales data, enabling dynamic filtering and deep dives into key metrics.

### Key Visualizations

1. Sales by Product: Bar chart showing total sales by product category.
2. Monthly Sales Trend: Area chart illustrating sales trends over months and quarters for seasonality insights.
3. Regional Sales Performance: Map visualization for geographic sales distribution.
4. Profit Margin by Product: Line and clustered column chart showing profit margin and total profit across different products.

---

## Key Findings

1. Top Products: Certain product categories emerged as high-revenue drivers, offering opportunities for strategic promotions.
2. Seasonality in Sales: Peaks in Q3 and Q4 indicate opportunities for holiday and seasonal marketing.
3. Seasonal Trends: Identified Q3 and Q4 peak sales months, revealing key times of demand for Adidas products.
4. Quarterly Patterns: Sales consistently spiked in Q3, indicating a high-performing season – a strategic period for promotions and inventory management.
5. Year-Over-Year Growth: Observed steady growth in total sales, with notable increases in 2021.
6. Regional Performance: Regions like North America and Europe lead in overall sales, with North America showing the highest growth rates.
Emerging markets have lower but gradually increasing sales, indicating potential growth with tailored marketing efforts.
7. Profit Margins: Products with higher profit margins but lower sales volumes may benefit from targeted upselling.

---

## Recommendations
- Optimize Marketing for Top Products:
Action: Increase marketing investments for high-performing products, especially in regions where they are most popular.
Impact: Enhances revenue and profit through the promotion of products with proven customer demand and profitability.

- Leverage Seasonality in Sales:
Action: Plan promotional campaigns around Q3 and Q4 to capitalize on seasonal demand. Introduce seasonal discounts or limited-edition products during peak sales periods.
Impact: Maximizes sales during high-demand periods and drives revenue growth by targeting customer purchase patterns.

- Strategic Upselling of High-Margin, Low-Volume Products:
Action: Implement upselling techniques, such as bundling or targeted promotions, for products with higher profit margins but lower sales.
Impact: Boosts profitability without the need to increase high-cost marketing, by leveraging existing high-margin items.

## Project Files

- [Adidas Sales Dataset.xlsx](Raw dataset used for the analysis).
- [https://github.com/Tibson-spec/Adidas-Sales-Analysis Project/blob/main/Adidas%20Sales%20Dataset(Personal%20Projects)/Adidas%20analysis(portfolio%20p).sql](Excel Power Query script for data cleaning and transformation).
- `SQL Queries.sql`: SQL Server queries for analysis.
- `Power BI Dashboard.pbix`: Power BI file with interactive dashboards.
- `README.md`: Project documentation.
Click 👉[here](https://drive.google.com/file/d/1uIO7j8wKBYpNeZq6XTf_AGe7_B3NbxvM/view?usp=sharing)👈
---

## Conclusion

This project demonstrates a full data analysis pipeline, from data cleaning and transformation to analysis and visualization. By using Excel, SQL, and Power BI, this project exemplifies a strategic approach to transforming raw data into insights for decision-making across Adidas’s business areas.

---

