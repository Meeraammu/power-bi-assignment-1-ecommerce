# power-bi-assignment-1-ecommerce
Power BI Assignment: Data transformation, data cleansing, and data modeling of an e-commerce sales dataset
# E-Commerce Sales Analysis: Power BI Data Transformation & Modeling

## Project Overview
This repository contains an end-to-end data preparation and modeling project built in Power BI. The objective of this project is to extract raw e-commerce sales data, perform robust data transformations using Power Query, and build a fully functional relational data model ready for business intelligence reporting. 

## Dataset Details
The project utilizes three primary raw datasets:
*   `List of Orders.csv` - Contains order-level metadata including dates and customer details.
*   `Order Details.csv` - Contains line-item details such as categories, amounts, and profit.
*   `Sales target.csv` - Contains monthly category-level sales goals.

## Core Operations Performed

### 1. Data Transformation (Power Query)
*   **Data Type Optimization:** Converted financial columns to 'Fixed Decimal Number' and standardized date formatting.
*   **Text Cleaning:** Formatted customer names to Proper Case and merged `City` and `State` into a unified `Location` column.
*   **Custom & Conditional Columns:** Calculated `Profit Margin` percentages and generated a `Profit Status` categorical label (Profit, Loss, Break-Even).
*   **Data Reduction:** Restricted initial order imports to optimize load times and isolated target regions (e.g., Tamil Nadu) for regional analysis.
*   **Aggregations & Grouping:** Created standalone lookup tables summarizing count of orders, average profit by category, and monthly target totals.

### 2. Data Cleansing
*   Implemented strategies to identify and handle missing values across critical financial and geographical columns.
*   Deduplicated records to ensure data integrity before establishing relationships.

### 3. Data Modeling
*   **Order Relationship:** Established a `1-to-Many` relationship between `List of Orders` and `Order Details` using the `Order ID` primary key.
*   **Target Mapping:** Built and activated a relationship connecting the `Order Details` and `Sales Target` tables via the `Category` dimension, utilizing a bridge table to resolve Many-to-Many cardinality conflicts.

## Tools & Technologies
*   **Power BI Desktop**
*   **Power Query Editor** 
*   **Data Modeling** 
