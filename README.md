# Exploratory Data Analysis on Retail Sales Data 

## Project Overview:
As a Data Analyst Intern at Oasis Infobytes,  I exploreED retail sales data to uncover patterns, trends, and insights that can help businesses make data-driven decisions. Through exploratory data analysis (EDA), we analyze customer demographics, purchasing behavior, and product performance to provide actionable recommendations.

## Dataset Description:

This dataset is a snapshot of a fictional retail landscape sourced from kaggle, capturing essential attributes that drive retail operations and customer interactions. It includes key details such as Transaction ID, Date, Customer ID, Gender, Age, Product Category, Quantity, Price per Unit, and Total Amount. These attributes enable a multifaceted exploration of sales trends, demographic influences, and purchasing behaviors.

## Goal of Analysis: 
To analyze customer demographics, purchasing behavior, and product performance

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
  ```
- Created an Age Group column to categorize customers into age brackets using the IFS function:

   ```excel
  =IFS(E2<=20, "15-20", E2<=30, "21-30", E2<=40, "31-40", E2<=50, "41-50", E2>=51, "51+")
    ```

   ### Descriptive Analysis
- Calculated the average revenue for May 2023 using the `AVERAGEIFS` function:
  
  ```excel
   =AVERAGEIFS(Table1[Total Amount], Table1[Month], "May", Table1[Year], "2023") ```
  
- Calculated the total revenue generated from the Beauty product category using the SUMIF function

```excel
=SUMIF(Table1[Product Category], "Beauty",Table1[Total Amount])
```

- Determined the number of female customers in November 2023 using the COUNTIFS function:

```excel
=COUNTIFS(Table1[Gender], "Female", Table1[Month], "November", Table1[Year], "2023")
```



### Data Aggregation

- Created pivot tables on two different Sheets to aggregate data for customer insights and product performance:

  - Customer Insights: Aggregated data by gender, age group, and revenue.

  - Product Performance: Aggregated data by product category, gender, and revenue.

### Data Visualization

- Created two dashboards in Excel to visualize insights:

  - Customer Analysis Dashboard: Focused on customer demographics and purchasing behavior.

  - Product Performance Dashboard: Focused on product category performance and sales trends.

- Used charts such as donut charts, bar charts,line charts, KPIs to present insights effectively.

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

- Average Price by Product Category:
The average price for beauty products is __$184.06__, making it the most expensive category. __Electronics__ follow closely at __$184.06__ ,making it the most expensive category. __Electronics__ follow closely at __$181.90__, while clothing is the most affordable at __$174.29__. This pricing structure aligns with the observed purchasing behavior, where higher-priced items like beauty products have lower sales volumes compared to more affordable categories like clothing.

- Quantity Sold by Product Category:
  - Clothing: With __894__ units sold, clothing is the top-performing category in terms of quantity. This is likely due to its lower price point and its status as a necessity.

  - Electronics: **849** units of electronics were sold, reflecting strong demand for this category despite its higher price.

  - Beauty Products: __771__ units of beauty products were sold, the lowest among the three categories. This aligns with the law of demand, as beauty products have the highest average price.

- Revenue Contribution by Product Category:

  - Electronics: Contributed 34% of total revenue, slightly higher than clothing. This highlights the profitability of electronics despite their lower sales volume compared to clothing.
  - Clothing: Contributed 34% of total revenue, driven by its high sales volume.
  - Beauty Products: Contributed 32% of total revenue, demonstrating their high profitability despite lower sales volume.

- Monthly Sales Trends:
The highest revenue and quantity sold were recorded in **May**, with **$53,150** in revenue and 259 units sold. This peak suggests a seasonal trend, possibly driven by holidays or promotional events. October also showed strong sales, further indicating the importance of seasonal strategies.
## Recommendation  

- Our insights show that **female customers are our most active and high-spending segment**, which could be due to their role in household purchases. While the gap between male and female customers is relatively small, **women contribute the highest revenue**. This indicates that we should **prioritize female customers** by continuing to sell home-related products while also **expanding our male-targeted product offerings** to boost overall revenue. Since men are also interested in our products but may have **busier schedules**, we should consider **marketing convenience-focused solutions** tailored to them.  

- Customers aged **51 and above** are not only **our most active shoppers** but also have **the highest purchasing power**. This is likely due to their financial stability, retirement, or reduced working hours, giving them more time to shop. To enhance their experience, we should **introduce home delivery options** to make shopping easier and more convenient for them. Similarly, **customers aged 21-30** also show **high purchasing power**, likely because they are at the **peak of their careers** with fewer financial burdens. This group should be **targeted with more advertising and product promotions**. On the other hand, **customers aged 15-20** contribute the least to our sales, likely due to financial dependence on parents or guardians. However, **we shouldn’t reduce products meant for this age group**, as parents may still make purchases on their behalf.  

- While **women have the highest purchasing power and shop more frequently**, **beauty products remain the least-sold category**, whereas **clothing has the highest sales volume, followed by electronics**. This aligns with the idea that clothing is a **necessity**, and electronics are in high demand as they **enhance convenience and entertainment at home**. To **boost beauty product sales**, we should consider **offering more discounts and promotions**, as this category has the **highest average price but the lowest quantity sold**. At the same time, we should **prioritize clothing and electronics**, as they are **consistently in high demand**.  

- **Men purchase more clothing than any other category**, while **women purchase more electronics and beauty products**. This suggests that **expanding our clothing selection could attract even more male shoppers**, while also **focusing on electronics and beauty products for female customers**, as they have the **strongest purchasing power overall**.  

- Our **highest sales and revenue were recorded in May, followed by October**. This suggests a **seasonal trend**, possibly linked to promotions or holiday-related shopping. To **maximize revenue**, we should **offer targeted discounts and marketing campaigns in May, October, and other peak seasons** to **capitalize on increased consumer spending**.  
