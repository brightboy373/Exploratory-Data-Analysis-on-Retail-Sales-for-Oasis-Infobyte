# Exploratory Data Analysis on Retail Sales Data 

## Project Overview:
This project explores retail sales data to uncover patterns, trends, and insights that can help Oasis Infobyte make data-driven decisions. Through exploratory data analysis (EDA), we analyze customer demographics, purchasing behavior, and product performance to provide actionable recommendations.

## Dataset Description:

This dataset is a snapshot of a fictional retail landscape, capturing essential attributes that drive retail operations and customer interactions. It includes key details such as Transaction ID, Date, Customer ID, Gender, Age, Product Category, Quantity, Price per Unit, and Total Amount. These attributes enable a multifaceted exploration of sales trends, demographic influences, and purchasing behaviors.

## Goal of Analysis: To analyze customer demographics and purchasing behavior.

## Tasks:
-	Descriptive Statistics
-	Time Series Analysis: Analyze sales trends over time using time series techniques.
-	Customer and Product Analysis: Analyze customer demographics and purchasing behavior.
-	Visualization: Present insights through bar charts, line plots, and pie charts.
-	Recommendations: Provide actionable recommendations based on the EDA.

## Methods

### Data Understanding
- Reviewed the dataset description and identified key attributes (e.g., Transaction ID, Date, Customer ID, Gender, Age, Product Category, Quantity, Price per Unit, Total Amount).
- Defined the goal of the analysis: to uncover patterns, trends, and insights related to customer demographics, purchasing behavior, and product performance.

### Data Loading and Cleaning
- Loaded the dataset into Excel and formatted it as a table using `Ctrl + T`.
- Checked for null values, inconsistencies, and anomalies using Excel's filter functionality.
- Extracted the month and year from the `Date` column using the `TEXT` function:
  ```excel
  =TEXT([@Date], "MMM")  // Extracts month (e.g., "May")
  =TEXT([@Date], "YYYY") // Extracts year (e.g., "2023")
- Created an Age Group column to categorize customers into age brackets using the IFS function:
  =IFS(E2<=20, "15-20", E2<=30, "21-30", E2<=40, "31-40", E2<=50, "41-50", E2>=51, "51+")
