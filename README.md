# Customer_Behavior_Dashboard
Project Overview
This project provides a comprehensive analysis of customer shopping behavior using a dataset of 3,900 transactions. The analysis combines Python data processing, SQL querying, and Power BI visualization to uncover key trends in customer demographics, purchasing patterns, product preferences, and revenue drivers.

The project demonstrates a complete data analytics pipeline - from raw data ingestion and cleaning to interactive dashboard creation and actionable business insights.

## Tech Stack
Python 3.13 - Data processing & analysis

Pandas - Data manipulation and cleaning

Jupyter Notebook - Interactive development environment

PostgreSQL - Relational database for querying

SQLAlchemy - Database connection and ORM

Power BI - Interactive dashboard creation

psycopg2-binary - PostgreSQL adapter for Python

## Project Structure

├── customer-trends-data-analysis-SQL-Python-PowerBI.ipynb
│   └── Jupyter Notebook with complete data processing pipeline
│
├── customer_shopping_behavior.csv
│   └── Raw dataset (3,900 transactions, 18 columns)
│
├── SQL_Queries.sql
│   └── 10 analytical queries for business insights
│
├── Customer_Shopping_Behavior_Analysis_Report.pdf
│   └── Comprehensive analysis report
│
├── PowerBI_Dashboard.pbix
│   └── Interactive dashboard with visualizations
│
└── README.md
    └── Project documentation

## Data Pipeline
1. Data Ingestion
Load CSV data into Pandas DataFrame

Initial exploration of structure and data types

2. Data Cleaning
Handle missing values in Review Rating (37 entries)

Impute missing values using category median

3. Feature Engineering
Standardize column names (lowercase, underscores)

Create age_group (Young Adult, Adult, Middle-aged, Senior)

Map frequency_of_purchases to purchase_frequency_days (7, 14, 30, 90, 365 days)

Remove redundant promo_code_used column

4. Database Loading
Export cleaned data to PostgreSQL

Table name: customer

Schema: 19 columns with appropriate data types

5. SQL Analysis
10 business questions answered

Revenue by gender, discount effectiveness, product ratings

Customer segmentation and loyalty analysis

6. Power BI Dashboard
Interactive filters (Subscription, Gender, Category, Shipping)

Key metrics cards (Avg Rating, Avg Purchase Amount)

Revenue and sales visualizations

Subscription status pie chart    


## Power BI Dashboard Features
Filters (Slicers)
Subscription Status (Yes/No)

Gender (Male/Female)

Category (Clothing, Footwear, Outerwear)

Shipping Type (6 options)

Key Visuals
Revenue by Age Group - Bar chart showing revenue distribution

Sales by Category - Sales volume by product category

Sales by Age Group - Stacked bar chart

Revenue by Category - Revenue contribution breakdown

Subscription Status - Pie chart (73% No, 27% Yes)

Average Review Rating - 3.75 / 5.0 KPI card

Average Purchase Amount - $59.76 KPI card

# Key Findings Summary
## Demographics
Gender: 68% Male, 32% Female

Age: Average 44 years (range: 18-70)

Age Group: Middle-aged customers generate highest revenue

Purchasing Behavior
Discount Usage: 57% of purchases have discounts applied

Shipping: Free Shipping most popular (675 transactions)

Payment: PayPal preferred (677 users)

Loyalty: Average previous purchases = 25.35

Revenue Insights
Clothing generates ~$0.73M in revenue

Male customers contribute 2.1x more revenue than females



Subscribers have higher average spend per transaction

Product Performance
Top Rated: Footwear & Accessories (3.8-3.86)

Highest Discount Rate: Hat (50%), Sneakers (49%)

Top Selling: Blouse, Sandals, Jacket

## Lessons Learned
Data Quality Matters: 37 missing values needed careful imputation using category medians to avoid bias.

Feature Engineering Adds Value: Creating age_group and purchase_frequency_days enabled more meaningful analysis.

SQL and Visualization Work Together: SQL provided granular insights, while Power BI enabled interactive exploration.

Clean Data is Essential: Redundant columns (promo_code_used) were removed to simplify analysis.

Business Impact: Insights directly inform marketing strategies, inventory planning, and customer retention programs.
