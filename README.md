# Sales-Analysis-Dashboard
This project presents an interactive Sales Analysis Dashboard developed using Power BI to analyze and monitor overall business performance. The dashboard focuses on identifying sales trends, profitability, customer purchasing behavior, regional performance, and sales channel effectiveness through data-driven insights.
## Project Overview
This project presents an end-to-end Retail Sales Analysis Dashboard built using Power BI. The dashboard analyzes sales performance, profitability, customer behavior, regional performance, and sales channel growth to help businesses make data-driven decisions.

The project focuses on transforming raw sales data into meaningful business insights through data cleaning, data modeling, DAX calculations, and interactive visualizations.

---

# Objectives

The main objectives of this project are:

- Analyze overall sales performance
- Identify top-performing product categories
- Evaluate regional profitability
- Compare Online vs Retail sales channels
- Understand customer purchasing behavior
- Analyze discount impact on profitability
- Track Year-over-Year (YoY) growth
- Generate actionable business insights

---

# Tools & Technologies Used

- Power Query
- Power BI
- DAX (Data Analysis Expressions)
- Data Modeling
- Interactive Visualizations

---

# Dataset Information

The dataset contains Sales transaction data including:

- Product Category
- Sales Amount
- Unit Cost
- Unit Price
- Quantity Sold
- Customer Type
- Payment Method
- Sales Channel
- Region
- Sales Representative
- Discounts
- Sale Date

---

# Data Cleaning & Transformation

The following data preparation steps were performed:

- Checked null and missing values
- Verified data types
- Created Date Calendar Table
- Removed redundant fields
- Created relationships between tables
- Formatted discount and financial columns
- Created calculated columns and measures

---

# Data Modeling

A star-schema inspired data model was used:

- Fact Table: Sales Data
- Dimension Table: Calendar Table

Relationships were created using:
- Sale_Date ↔ Calendar Date

---

# Key DAX Measures

## Gross Revenue

```DAX
Gross Revenue =
SUMX(
    Fact_Sales,
    Fact_Sales[Unit_Price] *
    Fact_Sales[Quantity_Sold]
)
Total Cost
Total Cost =
SUMX(
    Fact_Sales,
    Fact_Sales[Unit_Cost] *
    Fact_Sales[Quantity_Sold]
)
Discount Amount
Discount Amount =
SUMX(
    Fact_Sales,
    (Fact_Sales[Unit_Price] *
    Fact_Sales[Quantity_Sold]) *
    Fact_Sales[Discount]
)
Net Sales
Net Sales =
[Gross Revenue] - [Discount Amount]
Profit
Profit =
[Net Sales] - [Total Cost]
YoY Growth %
YoY Growth % =
DIVIDE(
    [Total Sales] - [Previous Year Sales],
    [Previous Year Sales],
    0
)
Dashboard Features

The dashboard includes:

KPI Cards
Total Sales
Total Cost
Total Profit
Total Discount
YoY Growth %
Product Category Analysis
Regional Profit Analysis
Sales Channel Comparison
Sales Representative Performance
Customer Type Analysis
Monthly Financial Summary
Interactive Filters & Slicers
Key Business Insights
Clothing category generated the highest sales revenue.
Regional sales performance remained balanced across all regions.
Retail channel showed stronger YoY growth compared to Online sales.
Returning customers contributed significantly to total revenue.
Discounts had a noticeable impact on overall profitability.
Product profitability varied despite similar revenue levels.
Business Recommendations
Focus marketing efforts on high-performing product categories.
Optimize discount strategies to improve profit margins.
Strengthen customer retention programs for returning customers.
Expand high-performing sales channels and regions.
Monitor discount-heavy categories to reduce margin pressure.
Conclusion

This project demonstrates how Power BI can be used to transform raw sales data into actionable business insights. Through DAX calculations, interactive dashboards, and storytelling techniques, the analysis helps identify growth opportunities, profitability trends, and customer behavior patterns.

# Dashboard Preview
<img width="1183" height="682" alt="Screenshot 2026-05-24 035756" src="https://github.com/user-attachments/assets/1aabb459-8f04-4226-a0d3-38778948ea9d" />



Author
Sushma Verma
