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
