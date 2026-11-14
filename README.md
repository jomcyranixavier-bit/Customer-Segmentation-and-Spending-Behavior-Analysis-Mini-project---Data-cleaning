Customer Segmentation and Spending Behavior Analysis Mini project
Excel Data Cleaning and Preparation

1. Project Overview
 This project analyzes customer demographics, purchasing behavior, and campaign responses to identify different customer segments and spending patterns. Using Excel Power Query and Power BI, the data was cleaned, transformed, and visualized to uncover insights that can help businesses improve marketing strategies and customer engagement.

2. Tools Used
Microsoft Excel
Power Query Editor

Applied Steps for Data cleaning
replace null value in income with median 51382
Changed data types
Deleted unnecessary columns from the original dataset 
Sort ascending, filteres
Renamed the columns as MntWines to 	Wine Spending
MntFruits	- Fruit Spending
MntMeatProducts-	Meat Spending
MntFishProducts	- Fish Spending
NumWebPurchases-	Web Purchases
NumStorePurchases-	Store Purchases
Dt_Customer	- Customer Since
and Response → Campaign Response
Check for ID Duplicates.
Check for Count Occurrences
Customer column added for Age using Date.Year(DateTime.LocalNow()) - [Year_Birth]
Created an Age column by subtracting the customer's birth year from the current year.
Created Custom column for Total spending by adding all the spendings.

Final Mini Project
--------------
# Customer Segmentation and Spending Behavior Analysis

## Project Overview

This Power BI project analyzes the behavior and spending patterns of 2.2K (2,240) customers using a dataset containing 2,240 rows and 20 columns including custom/calculated columns. The dashboard provides insights into customer demographics, income, spending habits, purchase methods, marital status, children at home, recency, and customer tenure. Interactive KPIs, charts, and slicers help identify trends and support data\-driven business decisions.

## Dataset Information

- Total Records: 2,240 Customers
- Data Source: Marketing Campaign Dataset
- Data Model: Single\-table model

## Data Preparation (Power Query)

### Custom Customer ID

"CUST" & Text.PadStart(Text.From([ID]), 2, "0")

### Created Columns

- Customer ID (Custom)
- Customer Tenure (Months)

## DAX Measures

### KPI Measures

Total Customers =

DISTINCTCOUNT(marketing\_campaign1[Customer ID])

Total Product Spending =

SUM(marketing\_campaign1[Wine Spending]) \+

SUM(marketing\_campaign1[Fruit Spending]) \+

SUM(marketing\_campaign1[Meat Spending]) \+

SUM(marketing\_campaign1[Fish Spending])

Average Spending =

AVERAGE(marketing\_campaign1[Total Spending])

Average Income =

AVERAGE(marketing\_campaign1[Income])

Response Rate =

AVERAGE(marketing\_campaign1[Campaign Response])

Total Web Purchases =

SUM(marketing\_campaign1[Web Purchases])

Average Tenure =

AVERAGE(marketing\_campaign1[Customer Tenure (Months)])

### Calculated Column

Customer Tenure (Months) =

DATEDIFF(

    marketing\_campaign1[Customer Since],

    TODAY(),

    MONTH

)

## Dashboard Pages

### Page 1: Customer Profile Analysis

**KPIs**

- Total Customers
- Total Product Spending
- Average Spending
- Average Income
- Response Rate
- Average Tenure

**Visualizations**

- Clustered Column Chart: Customers by Age
- Donut Chart: Marital Status Distribution
- Clustered Bar Chart: Customers by Education
- Scatter Chart: Income vs Total Spending

### Page 2: Purchase Behavior & Campaign Analysis

**Visualizations**

- Web Purchases vs Store Purchases by Marital Status
- Campaign Response Distribution
- Campaign Response by Education (Treemap)
- Income vs Total Spending
- Recency vs Total Spending

## Key Insights

### Customer Profile Insights

- The customer base consists of approximately 2.2K customers.
- The average customer age is 57 years.
- Married customers form the largest customer group.
- Graduation is the most common education level among customers.

### Purchase Behavior Insights

- Store purchases exceed web purchases across most customer segments.
- Married customers contribute the highest number of purchases.
- Average customer spending is 534.71.
- Campaign response rate is 14.91%.

### Spending Insights

- Higher\-income customers tend to spend more.
- Total product spending exceeds 1 million, indicating strong purchasing activity.

## Conclusion

The analysis shows that married and highly educated customers contribute significantly to overall business performance. Customer spending is positively influenced by income levels, while store purchases remain the preferred shopping channel. Future marketing efforts can focus on improving campaign response rates and targeting high\-value customer segments.

## Tools Used

- Power BI Desktop
- Power Query
- DAX
- Data Visualization
- Microsoft Excel



