# Sales Data Cleaning and Dashboard

  <img src="https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white" alt="Excel" />

## Overview: 
This project focuses on cleaning, preprocessing, and analyzing a sales dataset to extract actionable business insights. It features comprehensive data cleaning steps, handling of missing values, and the creation of an interactive dashboard to visualize sales performance across different dimensions.   

## 📑 Table of Contents
- [Dataset Characteristics](#-data-characteristics)

- [Data Engineering & Preprocessing](#-data-engineering-&-preprocessing)

- [Exploratory Data Analysis (EDA) & Statistics]()

- [Interactive Dashboard & Visualizations]()

## 📈 Data Characteristics
- File Format: xlsx   
- Original Dataset Shape: 1000 rows   
- Schema:
  1. OrderID: Numerical (Unique Identifier)
  2. Date: Temporal (Standardized to Short Date Format)
  3. Customer Name: String
  4. Region: Categorical (North, South, East, West)
  5. Category: Categorical (Home, Office, Tech)
  6. Product: Categorical (Sub-categories)
  7. Quantity: Numerical
  8. Price: Numerical
  9. Discount: String (Converted to Numerical)
  10. Total: Numerical (Engineered Feature)  

## 🛠️ Data Engineering & Preprocessing
The dataset underwent strict cleaning protocols to ensure the integrity of the downstream financial analysis.

1. Standardization:

    - Deduplication: Verified zero duplicate transaction rows.

    - Formatting: Transformed Customer Name strings to Proper format. Converted Discount values from string representations to strict numerical formats. Standardized Date column to Short Date Format.

2. Handling Missing Values (Data Integrity Decisions):

    - Region (24 missing): Rows deleted. Reasoning: Imputing geographic data via mode risks artificially skewing regional statistics and misleading subsequent geographical analysis.

    - Customer Name (21 missing): Left blank. Reasoning: Missing personal identifiers do not hamper or skew aggregate quantitative revenue analysis.

    - Price (15 missing): Rows deleted. Reasoning: Price variance is highly subjective; identical products sold in the same region on the same date exhibited significant price fluctuations. Imputing with mean or median would introduce inaccurate data points detrimental to revenue modeling.

3. Feature Engineering:

    - Recalculated the Total revenue column using the standardized formula: Total = Quantity * Price * (1 - Discount). 

### Final Dataset Size: 962 rows left after handling missing values.   

## Feature Engineering: 
Recalculated the Total column using the formula Total = Quantity * Price * (1 - Discount).   

## 📊 Exploratory Data Analysis (EDA) & Statistics 
(For detailed steps, charts, and methodologies used during the exploratory data analysis phase, please refer to the EDA.docx file in this repository).
### Key Revenue Metrics:

- Total Sales: INR 6,559,062.50
- Average Order Value: INR 6,818.15
- Highest Single Order Value: INR 45,000
- Total Valid Orders: 962

### Top 5 Products by Revenue:

- Stapler: INR 513,767.50
- Bluetooth Speaker: INR 492,815.00
- Pen Set: INR 485,767.50
- Whiteboard: INR 482,727.50
- Laptop Stand: INR 479,620.00

  

## 🖥️ Interactive Dashboard & Visualizations
A centralized Sales Performance Dashboard was generated to visualize total revenue, top-performing regions, and products, integrating slicers for dynamic region and date filtering.

A centralized Sales Performance Dashboard was generated to visualize total revenue, top-performing regions, and products, integrating slicers for dynamic region and date filtering. 

<img width="2085" height="1065" alt="image" src="https://github.com/user-attachments/assets/c69205be-61b5-471a-b4f3-9b84a53df2ef" />

Key Dimensional Analysis:
- Category vs Revenue
<img width="1423" height="950" alt="image" src="https://github.com/user-attachments/assets/3da56b66-a1d3-4c2e-82b2-c62d08194eba" />

- Product vs Revenue
<img width="1878" height="1075" alt="image" src="https://github.com/user-attachments/assets/2404a997-496e-437f-8c93-4ed695cbc5d4" />

- Region vs Revenue
<img width="1297" height="759" alt="image" src="https://github.com/user-attachments/assets/557f691d-1ce8-492b-9b2d-b28b1eeb0637" />

- Revenue over time
<img width="1379" height="795" alt="image" src="https://github.com/user-attachments/assets/79ca85ba-061b-4081-a907-9d643dc98c61" />

- Discount vs Revenue   
<img width="1253" height="828" alt="image" src="https://github.com/user-attachments/assets/e293c7fa-0001-4741-a392-a0ab7fb9b9b4" />


