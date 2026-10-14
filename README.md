# Sales Data Cleaning and Dashboard

## Overview: 
This project focuses on cleaning, preprocessing, and analyzing a sales dataset to extract actionable business insights. It features comprehensive data cleaning steps, handling of missing values, and the creation of an interactive dashboard to visualize sales performance across different dimensions.   

## Data Information
- File Format: xlsx   
- Original Dataset Shape: 1000 rows   
- Columns and Data Types:
1. OrderID: Numerical Unique   
2. Date: Changed to Short Date Format   
3. Customer Name: String   
4. Region: Categorical (North, South, East, and West)   
5. Category: Categorical (Home, Office, and Tech)   
6. Product: Categorical (Sub-categories of the category column)   
7. Quantity: Numerical   
8. Price: Numerical   
9. Discount: String converted to Numerical   
10. Total: Numerical   

## Data Cleaning & Preprocessing
1) Duplicates: No duplicate rows were found in the dataset.   
2) Formatting Fixes:
-Customer Name: Transformed names to Proper Format.   
-Discount: Converted from string to Numerical Format.   
-Date: Converted to Short Date Format.   
3) Handling Missing Values:
- Region (24 missing): Rows deleted. Imputing geographic data via mode risks artificially skewing regional statistics and misleading subsequent analysis.   
- Customer Name (21 missing): Left blank. Missing identifiers do not hamper or skew aggregate quantitative analysis.   
- Price (15 missing): Rows deleted. Price variance is highly subjective; identical products sold in the same region on the same date exhibit significant price fluctuations. Imputing with mean or median would introduce inaccurate data points detrimental to revenue analysis.   

### Final Dataset Size: 962 rows left after handling missing values.   

## Feature Engineering: 
Recalculated the Total column using the formula Total = Quantity * Price * (1 - Discount).   

## Exploratory Data Analysis: 
For detailed steps, charts, and methodologies used during the exploratory data analysis phase, please refer to the EDA.docx file.

## Summary Statistics
- Total Sales: INR 6,559,062.50   
- Average Order Value: INR 6,818.15   
- Highest Single Order Value: INR 45,000   
- Total Number of Orders: 962 (after cleaning, originally 1000)   
- Top 5 Products by Revenue
- Stapler: INR 513,767.50   
- Bluetooth Speaker: INR 492,815.00   
- Pen Set: INR 485,767.50   
- Whiteboard: INR 482,727.50   
- Laptop Stand: INR 479,620.00   

## Visualizations and Dashboard
The project involved plotting the following key graphs:
- Category vs Revenue   
- Product vs Revenue   
- Region vs Revenue   
- Revenue over time   
- Discount vs Revenue   

A centralized Sales Performance Dashboard was generated to visualize total revenue, top-performing regions, and products, integrating slicers for dynamic region and date filtering. 
