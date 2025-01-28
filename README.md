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
-	Gender Distribution:
51% of our customers are female, while 49% are male. This indicates a nearly equal gender distribution, with a slight majority of female customers. Notably, female customers also contribute 51% of the total revenue, making them the most valuable customer segment. This suggests that women are not only more frequent shoppers but also have a higher purchasing power compared to men.
- Age Group Analysis:
Customers aged 51 and above are the most active and loyal segment, with a significant portion being female. This age group is likely in or nearing retirement, giving them more time and disposable income to spend. They are followed by customers aged 41-50, who are also highly active, likely due to their established careers and financial stability. The third most active group is customers aged 21-30, who are likely early in their careers with fewer financial responsibilities, making them more willing to spend. On the other hand, customers aged 15-20 are the least active, as they are likely financially dependent on their parents or guardians and have limited spending power.
- Revenue by Age Group:
The highest revenue comes from customers aged 51 and above, followed by those aged 21-30. This aligns with the observation that older customers have more disposable income, while younger adults (21-30) are in a phase of life where they are building their lifestyles and are more willing to spend. Customers aged 31-40 contribute the third-highest revenue, likely balancing their spending with growing financial responsibilities such as family and mortgages. The fourth-highest revenue comes from customers aged 41-50, who may be more cautious with their spending due to higher financial obligations. The lowest revenue comes from customers aged 15-20, reinforcing the idea that this group is largely dependent on others for financial support.
- Behavioral Insights:
The purchasing behavior of customers aged 51+ suggests they value convenience and quality, making them ideal candidates for loyalty programs or home delivery services. Meanwhile, customers aged 21-30 are more likely to respond to trendy or lifestyle-oriented marketing campaigns. The low engagement from the 15-20 age group indicates a need for targeted strategies, such as student discounts or promotions, to attract this demographic.

### Product Analysis:
- Total Revenue and Quantity Sold:
The total revenue generated is $456,000, with 51% coming from female customers. Similarly, out of the 2,514 units sold, 52% were purchased by women. This reinforces the finding that female customers are the most valuable segment, contributing significantly to both revenue and sales volume.

- Product Preferences by Gender:

 - Electronics: Men purchase slightly more electronics than women, indicating a stronger interest in this category among male customers. However, women also show considerable interest in electronics, likely due to their role as primary decision-makers for household purchases.

 - Beauty Products: Women are the primary buyers of beauty products, reflecting their stronger engagement with this category. Men also purchase beauty products, though less frequently, possibly for personal use or as gifts for partners.
 - Clothing: Men purchase more clothing than women, suggesting that men are more active in the fashion category. This could be due to a preference for trendy or functional clothing items.
