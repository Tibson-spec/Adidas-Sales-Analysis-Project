# Adidas-Sales-Analysis-Project

Creating a well-documented portfolio with a tailored focus on your skills and the analysis insights from the Adidas sales dataset will show potential clients or employers the depth of your expertise in data analysis, SQL, and Power BI. Here’s how you could structure the content for your portfolio website and GitHub.

---

### **Portfolio Website Content**

---

#### **Project Title**: Adidas Sales Analysis

**Project Overview**:
The Adidas Sales Analysis project is a comprehensive deep dive into Adidas's sales data, utilizing SQL Server for data cleaning and transformation, and Power BI for visualization and insights. This analysis provides actionable insights into sales trends, product performance, customer behavior, and profitability, equipping Adidas with data-driven decision-making tools to enhance business strategy.

---

**Objective**:
To analyze sales, customer demographics, and profitability data, identify key patterns and trends, and visualize findings in an interactive, easy-to-understand Power BI dashboard.

---

#### **Key Skills and Tools Used**
- **SQL Server**: Data cleaning, transformation, and querying.
- **Power BI**: Data visualization and interactive reporting.
- **Data Analysis**: Sales, customer, and profitability insights.
- **Excel**: Initial data processing and manipulation.

---

### **Project Breakdown**

#### **1. Data Preparation**
   - Imported and cleaned datasets in SQL Server.
   - Merged multiple tables to create unified datasets for sales, customer demographics, product details, and regional information.
   - Created calculated fields for metrics like **Average Operating Margin**, **Inventory Turnover Ratio**, and **Customer Lifetime Value (CLV)**.

**SQL Example**:
```sql
SELECT 
    Product,
    SUM(Sales) AS Total_Sales,
    AVG(Operating_Margin) AS Avg_Operating_Margin,
    (SUM(Sales) / SUM(Inventory)) AS Inventory_Turnover_Ratio
FROM 
    Sales_Data
GROUP BY 
    Product
ORDER BY 
    Total_Sales DESC;
```

---

#### **2. Power BI Dashboard Development**
   - Developed a Power BI dashboard with interactive features, allowing dynamic filtering by region, product category, and time period.
   - Created **KPI Cards** for quick insights on Total Sales, Average Order Value, and Total Units Sold.
   - Generated visualizations for easy interpretation of trends, customer segmentation, and profitability.

---

### **Core Analyses & Visual Insights**

#### **Sales Trend Analysis**
   - **Visualization**: Line Chart
   - **Insight**: Monthly sales trends revealed seasonality in customer demand, with peak sales periods aligning with major sporting events and holidays. This insight can guide inventory planning and promotional campaigns.

#### **Profitability Analysis by Product**
   - **Visualization**: Heat Map
   - **Insight**: Identified high-profit margin products within each category. Products with low margins but high sales indicate areas where pricing adjustments could enhance profitability.

#### **Top 10 Products by Sales**
   - **Visualization**: Bar Chart
   - **Insight**: Highlighted the top 10 products based on total sales, showing significant variations in product performance across regions. This analysis helps in regional-specific marketing strategies.

#### **Customer Demographic Analysis**
   - **Visualization**: Donut Chart
   - **Insight**: Breakdowns by age and gender uncovered the target demographic with the highest purchasing power. These insights inform Adidas’s advertising and promotional strategies.

#### **Inventory Turnover Analysis**
   - **Visualization**: Scatter Plot
   - **Insight**: Showcased inventory turnover rates by product, helping identify popular items and optimize stock levels to prevent overstock or understock scenarios.

---

### **Conclusion**

This analysis demonstrates how data insights can drive improved business outcomes. Leveraging SQL Server and Power BI enabled a full-spectrum view of sales performance, customer engagement, and product profitability, empowering Adidas to make more data-informed decisions.

---

---

### **GitHub Repository Content**

**Repository Name**: `Adidas-Sales-Analysis-Portfolio`

#### **README.md**

**Adidas Sales Analysis with SQL Server and Power BI**

---

**Project Description**:
This repository contains the SQL scripts, data preparation processes, and Power BI files for a comprehensive sales analysis project on Adidas's sales data. This analysis examines sales trends, customer behavior, and profitability metrics, using SQL Server for data transformation and Power BI for visualization.

**Project Structure**:
- **Data**: Contains sample data and schema for loading into SQL Server.
- **SQL Scripts**: All SQL scripts used for data preparation and analysis.
- **Power BI Dashboard**: `.pbix` file showcasing the interactive dashboard with detailed insights.
- **Documentation**: Analysis explanations and methodology used.

**Skills Highlighted**:
- SQL Server: Data transformation, calculated fields, and data aggregation.
- Power BI: Visualization, KPI creation, and dashboard interactivity.
- Data Analysis: Sales, profitability, and customer segmentation.

---

#### **Key Files**

- **Data Preparation Scripts**: `/scripts/data_preparation.sql`
  - SQL code for cleaning, merging, and transforming raw datasets.
- **Analysis Queries**: `/scripts/analysis_queries.sql`
  - Queries for deriving insights, such as top products, regional sales distribution, and customer demographics.
- **Power BI Report**: `/reports/adidas_sales_analysis.pbix`
  - The interactive Power BI report file containing all visuals and KPIs.

#### **Visuals and Insights**

1. **Sales Overview**: Total Sales, Operating Profit, Average Order Value, Units Sold.
2. **Sales Trends**: Time-series analysis of sales to identify high-demand periods.
3. **Top Products and Profitability**: Top-selling products and their profit margins.
4. **Customer Insights**: Segmentation by demographics and purchase frequency.
5. **Inventory Analysis**: Product demand and inventory turnover.

#### **Getting Started**

1. **Clone Repository**:
   ```bash
   git clone https://github.com/YourGitHubUsername/Adidas-Sales-Analysis-Portfolio.git
   ```

2. **Database Setup**:
   - Import the data into SQL Server.
   - Run the SQL scripts in the `scripts` folder to prepare and analyze data.

3. **Power BI**:
   - Open `adidas_sales_analysis.pbix` in Power BI Desktop.
   - Review and interact with the visuals to gain insights.

#### **Insights & Recommendations**

- **Trend Analysis**: Monthly and quarterly trends to plan stock levels and promotional events.
- **Customer Demographics**: Identify and target high-value segments.
- **Profitability**: Focus on high-margin products and adjust pricing for lower-margin items.
- **Inventory Management**: Optimize stock based on product demand and turnover rates.

#### **License**: MIT

#### **Contact**
For further inquiries, reach out via [YourEmail@example.com](mailto:YourEmail@example.com) or LinkedIn.

---

This documentation for your portfolio website and GitHub will clearly convey your expertise and thought process, providing a robust, professional showcase of your data analytics project.
