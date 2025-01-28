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

   `=IFS(E2<=20, "15-20", E2<=30, "21-30", E2<=40, "31-40", E2<=50, "41-50", E2>=51, "51+")`

   ### Descriptive Analysis
- Calculated the average revenue for May 2023 using the `AVERAGEIFS` function:
  
  ` =AVERAGEIFS(Table1[Total Amount], Table1[Month], "May", Table1[Year], "2023")`
  
- Calculated the total revenue generated from the Beauty product category using the SUMIF function

`=SUMIF('Retail Sales Data'!F:F, 'Beauty', 'Retail Sales Data'!I:I)`

- Determined the number of female customers in November 2023 using the COUNTIFS function:

`=COUNTIFS(Table1[Gender], "Female", Table1[Month], "November", Table1[Year], "2023")`

### Data Aggregation

- Created pivot tables to aggregate data for customer insights and product performance:

 - Customer Insights: Aggregated data by gender, age group, and revenue.

 - Product Performance: Aggregated data by product category, gender, and revenue.

### Data Visualization

- Created two dashboards in Excel to visualize insights:

 - Customer Analysis Dashboard: Focused on customer demographics and purchasing behavior.

 - Product Performance Dashboard: Focused on product category performance and sales trends.

- Used charts such as donut charts, bar charts, and line charts to present insights effectively.

<img width="737" alt="customer analysis dashboard" src="https://github.com/user-attachments/assets/0d2a1fcd-dc3c-484f-8e2b-1eb8cea1b49f" />

<img width="734" alt="Product Performance dashboard" src="https://github.com/user-attachments/assets/90efdc09-ab4a-4c85-8012-94298b5f952e" />




## Insights:
### Customer Analysis:
-	51% of our customers are female. This shows that we have more female customers then male but the gap between the both gender is very close. 51% of our Revenue also came from the female gender which makes them our most valuable customer segment.

