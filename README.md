# 2025 Electronics Sales Performance Dashboard

An enterprise-grade Business Intelligence project developed using Power BI to analyze and monitor sales performance for a multinational electronics retail company. The project delivers a fully interactive three-page dashboard designed to support operational monitoring, pricing analysis, and executive decision-making.

Rather than using a single overcrowded dashboard, the report architecture separates operational, transactional, and pricing analytics into dedicated analytical views. This approach improves readability, simplifies navigation, and enables more focused business analysis.

The project demonstrates practical expertise in data transformation, dimensional modeling, advanced DAX calculations, and professional dashboard design.

---

# Project Overview

The dashboard was developed to evaluate sales trends, customer performance, product profitability, and discount strategies throughout 2025.

The project focuses on transforming raw transactional data into a structured Business Intelligence solution capable of delivering actionable insights for management and financial analysis.

Key areas of analysis include:

- Product sales performance
- Regional revenue trends
- Seasonal sales patterns
- Discount strategy effectiveness
- Profitability analysis
- Customer acquisition insights

The final solution was designed with a strong emphasis on usability, analytical depth, and performance optimization.

---

# Business Objectives

The primary objectives of this project are:

- To identify top and bottom performing electronic products
- To evaluate regional sales performance across multiple markets
- To analyze monthly and quarterly sales trends throughout 2025
- To measure the impact of promotional discounts on profitability
- To support strategic decision-making using interactive analytics

---

# Data Cleaning and Transformation

All preprocessing and transformation steps were performed using Power Query.

## Data Type Validation

- Corrected inconsistent formatting issues across numerical columns
- Converted currency-related fields into decimal data types
- Validated decimal precision for discount and promotional metrics

## String Standardization

- Removed whitespace inconsistencies from structural keys
- Standardized Product IDs and Customer IDs
- Improved relational consistency across tables

## Granularity Verification

- Verified that revenue values represented row-level transactional data
- Prevented aggregation inconsistencies during reporting and DAX calculations

These transformation steps ensured high-quality analytical outputs and reliable dashboard performance.

---

# Data Modeling and Architecture

The dashboard uses an optimized Star Schema architecture to improve query performance and maintain clean filtering behavior.

## Fact Table

### `Sales`

Contains core transactional metrics including:

- Sale ID
- Product ID
- Customer ID
- Date
- Quantity
- Revenue
- Discount

## Dimension Tables

### `Customers`

- Customer ID
- Customer Name
- Region

### `Products`

- Product ID
- Product Name
- Category
- Price

### `Dates`

- Date
- Month
- Quarter
- Year

## Relationship Structure

- One-to-many relationships between dimension tables and the fact table
- Single-direction filtering to prevent ambiguity
- Optimized DAX propagation and report responsiveness

This architecture enabled efficient cross-filtering and improved dashboard scalability.

---

# DAX Engineering and KPI Development

Several advanced DAX measures were created to accurately evaluate revenue performance, customer trends, and discount impacts.

## Core Revenue Calculation

dax
Total_Revenue =
SUM(Sales[Revenue])

Avg_Revenue_Per_Customer =
DIVIDE(
    [Total_Revenue],
    DISTINCTCOUNT(Sales[CustomerID]),
    0
)

Discount Amount =
SUMX(
    Sales,
    Sales[Revenue] * Sales[Discount]
)

Discount Impact % =
DIVIDE(
    [Discount Amount],
    [Total_Revenue],
    0
)

Average_Discount_Rate =
AVERAGE(Sales[Discount])

Dashboard Architecture and Visualizations

The report is divided into three specialized analytical pages, each designed for a specific business objective.

<img width="1225" height="695" alt="Sales_Dash_1" src="https://github.com/user-attachments/assets/301b48cb-86ef-4752-b2dc-04c36d31e445" />


Page 1: Executive Sales Overview
Focus

High-level monitoring of overall business performance.

Visual Components
KPI cards for:
Total Revenue
Total Profit
Month-over-Month Growth
Units Sold
Revenue trend analysis across time
Category-wise sales distribution
Monthly and quarterly performance tracking

This page provides executives with a concise overview of business health and growth trends.

<img width="1223" height="696" alt="Sales_Dash_2" src="https://github.com/user-attachments/assets/4489b45e-395f-4c8c-a8d0-f14fc96b6595" />

Page 2: Product and Customer Deep-Dive
Focus

Detailed analysis of product performance and customer behavior.

Visual Components
Product-level sales comparison using optimized horizontal bar charts
Regional customer contribution analysis
Customer segmentation insights
Margin-focused account analysis

Special attention was given to layout optimization and label spacing to improve readability and eliminate truncated visual elements.

<img width="1216" height="698" alt="Sales_Dash_3" src="https://github.com/user-attachments/assets/0b379cdd-3eaa-4550-9f66-21ad47fcb00f" />

Page 3: Pricing and Discount Strategy Analysis
Focus

Evaluation of pricing strategies and discount effectiveness.

Visual Components
Scatter plot comparing discount values against generated revenue
Regional profit margin analysis
Discount impact tracking
Profitability comparison across product categories

This page helps financial analysts understand how promotional strategies influence revenue and profit margins.

Interaction Design
The dashboard includes several interactive features to improve user experience and analytical flexibility.

Global Slicers
Dropdown slicers integrated into the dashboard header
Clean layout without excessive filter clutter
Cross-Filtering
Synchronized filters across all dashboard pages
Interactive drill-down exploration across the full 2025 timeline

These interaction mechanics create a seamless analytical experience across all reporting layers.
Technologies Used
Power BI Desktop
Power Query
DAX (Data Analysis Expressions)
Data Modeling
Star Schema Architecture
Skills Demonstrated

This project highlights practical expertise in:
Business Intelligence
Data Transformation
Power Query
Data Modeling
Star Schema Design
Advanced DAX Calculations
KPI Development
Dashboard Architecture
Data Visualization
Interactive Reporting
Revenue and Profitability Analysis
Business Relevance

The dashboard supports business stakeholders by enabling them to:
Monitor sales performance in real time
Identify high-performing and underperforming products
Evaluate regional growth opportunities
Analyze pricing and discount effectiveness
Improve profitability through data-driven decisions

How to Use the Dashboard
Download the Sales_Performance_Analysis.pbix file from this repository.
Open the file using the latest version of Power BI Desktop.
Explore the Power Query transformations and data model relationships.
Navigate through the three dashboard pages using the report tabs.
Use slicers and cross-filtering features to interact with the data.

Conclusion
This project demonstrates my ability to design and develop a complete Business Intelligence solution using Power BI. By combining structured data modeling, advanced DAX calculations, and interactive dashboard design, I created a scalable analytical platform capable of supporting executive and operational decision-making.
The 2025 Electronics Sales Performance Dashboard reflects my capability to transform raw transactional data into actionable business insights through data engineering, analytics, and visualization.
