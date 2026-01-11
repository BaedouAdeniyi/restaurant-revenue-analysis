# Restuarant Revenue Analysis

## Table of Content
- [Project Overview](#project-overview)
- [Project Description](#project-description)
- [Dataset](#dataset)
- [Business Questions](#business-questions)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Key KPIs / Metrics](#key-kpis-/-metrics)
- [Dashbord](#dashboard)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [Summary](#summary)
- [Tools Used](#tools-used)

## Project Overview
This project analyzes sales data from a restaurant to understand revenue trends, customer behavior, and product performance. Using Excel, we explored the dataset, calculated key metrics, and created a dashboard to visualize insights. The goal is to show which products and time periods contribute most to revenue, and how customer orders vary throughout the day.

## Project Description
This project analyzes restaurant sales data to understand revenue performance, customer purchasing patterns, and product demand across different time periods. Using Microsoft Excel, I performed exploratory data analysis (EDA), built PivotTables, and created an interactive dashboard to track key performance indicators such as total revenue, order volume, average order value, product category performance, and customer behavior.

The analysis focuses on identifying what drives revenue over time, how customer activity varies by time of day, and how the product mix changes across different periods. Insights from the project highlight the relationship between order volume and revenue, differences in spending behavior by time of day, and the low rate of returning customers. The final output is a visually structured Excel dashboard designed to support data-driven business decisions.

## Dataset
- Dataset description
  - Order ID: Unique identifier for each order.
  - Customer Name: Name of the customer who placed the order.
  - Food Item: The specific food item ordered (e.g., Pizza, Pasta, Soup, Brownie).
  - Category: Food category of the item (Starter, Main, Dessert).
  - Quantity: Number of units of the food item ordered (1–5).
  - Price: Price of the food item in local currency (2.06 – 24.99).
  - Payment Method: Payment method used (Cash, Debit Card, Credit Card, Online Payment).
  - Order Time: Timestamp when the order was placed.
- Data Source: [Kaggle](https://www.kaggle.com/datasets/haseebindata/restaurant-orders)

## Business Questions
- How has revenue performed over time, and what factors drive changes in revenue?
- Which time of day generates the most revenue, and what drives performance across different periods of the day?
- How does product mix vary by time of day, and how does this influence revenue patterns?
- Do customers return, and what does the data suggest about customer retention behavior?
- Are there identifiable low-performing periods or patterns that indicate opportunities for improvement or data limitations?

## Data Cleaning and Preparation
The dataset was first reviewed for data quality issues, including missing values and duplicate records. No inconsistencies were found.

To support business analysis, new features were created. A revenue column was calculated by multiplying price and quantity for each order. The original order timestamp was split into separate date and time columns, enabling trend and time-based analysis.

Additionally, a time period feature (Morning, Afternoon, Evening, Night) was derived from the order time to analyze customer behavior and sales performance across different periods of the day.

## Exploartory Data Analysis (EDA)
The exploratory data analysis focused on understanding revenue performance, customer ordering behavior, and product preferences across different time periods.

Revenue patterns were examined by product category, time of day, and over time to identify key revenue drivers and trends.
Order behavior was analyzed using order counts and order volume trends to understand customer activity levels.
Average order value was explored across time periods and on a monthly basis to assess customer spending behavior.
Product mix analysis was conducted to understand how customer preferences differ by time of day.
Finally, customer repeat behavior was reviewed to provide context on customer retention.

These analyses informed the selection of KPIs and visuals used in the final dashboard.


## Key KPIs / Metrics
To summarize restaurant performance and support the analysis, the following key metrics were calculated
### 1. Total Revenue
- The total amount generated from all completed orders within the dataset period.
- Calculation:
   - Total Revenue = Price × Quantity (aggregated across all orders)

### 2. Total Orders
- The total number of unique orders placed.
- Calculation:
  - Total Orders = Count of unique Order IDs
 
### 3. Average Order Value (AOV)
- The average amount spent per order.
- Calculation:
  - Average Order Value = Total Revenue ÷ Total Orders

 ### 4. Returning Customer Rate
 - Measures how many customers placed more than one order.
 - Calculation:
   - Returning Customer Rate = (Number of repeat customers ÷ Total customers) × 100
   - Insight: The rate is very low, indicating that most customers are one-time buyers.

### 5. Top Product Category by Revenue
- Identifies the meal category that contributes the highest share of total revenue using pivot tables
- Result: Main Dish category generates the highest revenue.

## Dashboard
<img width="488" height="275" alt="Screenshot 2025-12-27 204658" src="https://github.com/user-attachments/assets/558c4b2b-5bec-43f5-83d1-822ff9a05481" />

## Key Findings
### Key Insight 1: Revenue Performance Over Time
Question we are answering
- How has revenue performed over time, and what factors drive changes in revenue?

Revenue shows noticeable variation over time rather than steady growth. Some months record strong increases, while others experience slowdowns or dips, indicating that revenue is not evenly distributed across the year.

A closer look shows that these changes are mainly driven by fluctuations in the number of orders rather than large changes in average order value. During high-revenue months, order volume increases significantly, while average order value remains relatively stable. In lower-revenue months, fewer orders are placed, which directly reduces total revenue.

This suggests that revenue performance is largely volume-driven. Improving customer acquisition, repeat purchases, or order frequency would likely have a greater impact on revenue growth than focusing only on increasing prices or basket size.

### Key Insight 2: Time-of-Day Performance
Question this insight answers
- Which time of day generates the most revenue, and what drives performance differences across time periods?

Revenue is highest in the morning, followed by the afternoon, evening, and night. Morning revenue is nearly twice that of the afternoon, while afternoon and evening revenues are very similar. Evening revenue is almost 2.5 times higher than night revenue.

To understand what drives this pattern, revenue was broken down into order volume and average revenue per order.

Order count closely mirrors the revenue trend across time periods, indicating that higher morning revenue is primarily driven by a higher number of orders, not higher spend per order.

In contrast, average revenue per order is highest in the afternoon, followed by evening and night, with morning having the lowest average order value. Afternoon average revenue is nearly twice that of the evening, suggesting that although fewer customers visit in the afternoon, each transaction generates more revenue.ther order main dishes or combine starter + main

To explain this difference, a hypothesis was tested on product mix by time of day. The analysis showed that:

- Starters and desserts are ordered more frequently in the morning
- Main meals (often combined with starters) are ordered more frequently in the afternoon

This explains the higher afternoon average order value. Main meals account for the largest share of revenue (≈42%), compared to starters (≈39%) and desserts (≈38%), confirming that meal composition (not customer volume) drives higher afternoon revenue per order.

### Key Insight 3: Product Performance
Question this insight answers
- Which products contribute the most to revenue, and how does product mix differ across time periods?

Overall, main meals contribute the largest share of total revenue, confirming that they are the primary revenue driver, even though starters and desserts also contribute meaningfully.

However, product contribution changes noticeably by time of day.

In the morning, starters and desserts slightly lead over main meals, though main meals are still ordered at a meaningful level. This suggests that customers are more inclined toward lighter or quicker purchases in the morning, rather than full meals.

In the afternoon, starters become the most ordered category, followed by main meals, while desserts are ordered less frequently. This combination indicates that customers are more likely to order fuller meals, often pairing a main meal with a starter, which aligns with the higher average order value observed during this period.

In the evening, main meals take the lead, with desserts also forming a substantial share, while starters decline further. This points to a shift toward more complete dining compared to earlier in the day.

At night, main meals dominate the product mix, with starters and desserts contributing at similar but lower levels. Despite this stronger preference for main meals, overall revenue remains lower due to reduced order volume during this period

### Key Insight 4: Customer Retention Behaviour
Question this insight answers
- Do customers return and what does the data suggest about customer rentention

The dataset shows that customer repeat purchases are extremely low. Out of approximately 500 total records, only three customers appear more than once, resulting in a returning customer rate of about 0.6%. This indicates that almost all customers in the dataset made only a single purchase.

Because the number of returning customers is so small, the data does not support a deeper analysis of repeat purchase behavior or loyalty patterns. As a result, overall revenue and order trends in this dataset are driven almost entirely by one-time customers.

### Key Insight 5: Low-Performing Periods & Data Limitations
Qustion this insight answers
- Are there identifiable low-performing periods or patterns that indicate opportunities for improvement or data limitations?

The night period consistently records the lowest revenue and order volume compared to other times of day. In addition, revenue shows a sharp decline toward the final month (August) in the dataset, which appears inconsistent with earlier trends.

However, further inspection suggests that these patterns are influenced by data coverage limitations rather than confirmed demand drops.

## Recommendations
1. Leverage Morning Traffic to Increase Order Value

The morning period generates the highest order volume and total revenue, but it also records the lowest average order value, driven by a higher proportion of starter and dessert purchases compared to main meals. This suggests that while customer traffic is strong in the morning, individual spending per order is relatively low. Based on this, the business could explore bundle offers or subtle upselling strategies during the morning period, such as combining light items with main meals, to increase the value of each order without relying on additional foot traffic.

2. Sustain and Protect Afternoon Performance

Although the afternoon records fewer orders than the morning, it achieves the highest average order value, largely because customers tend to order main meals alongside starters. This indicates that customers in this period are more likely to sit down for a full meal. To sustain this performance, the business should ensure consistent menu availability, efficient service, and adequate staffing during the afternoon to avoid disruptions that could reduce order value or discourage customers.

3. Approach Night Period Performance with Caution

The night period shows the lowest revenue and order volume, even though the average order value is not the lowest among all time periods. This suggests that lower performance may be driven more by reduced customer traffic than by low spending behavior. Rather than making immediate operational changes, the business should consider collecting more data or testing targeted promotions to determine whether demand can be stimulated during this period.

4. Improve Customer Retention Tracking

The analysis shows that returning customers are almost non-existent, with only a very small percentage of customers appearing more than once in the dataset. This limits the ability to analyze repeat purchase behavior or long-term customer value. To address this, the business should consider implementing a more reliable customer identification system, such as loyalty programs or unique customer IDs, to better track repeat visits and support future retention analysis.

5. Extend Data Collection for Stronger Insights

Some observed trends, particularly toward the end of the dataset, are influenced by incomplete data, which limits the ability to assess seasonality or long-term patterns. Extending data collection over a longer and more complete time period would allow for more reliable trend analysis, clearer identification of seasonal effects, and stronger support for future business decisions. 

## Summary
This project analyzed restaurant sales data to understand how revenue performs over time, how customer behavior varies across different periods of the day, and what factors drive overall performance. Using Excel for data cleaning, exploration, and visualization, the analysis focused on identifying meaningful patterns rather than producing surface-level metrics.

The findings show that revenue trends are primarily driven by changes in order volume rather than fluctuations in average order value. While the morning period generates the highest revenue due to high customer traffic, it also records the lowest average order value, driven by a higher proportion of starter and dessert purchases. In contrast, the afternoon period, despite having fewer orders, achieves the highest average order value as customers tend to order full meals.

Customer retention was found to be extremely low, with very few repeat customers identified in the dataset, limiting deeper analysis of repeat purchase behavior. Additionally, incomplete data for certain periods highlights the importance of longer and more consistent data collection to support stronger conclusions.

Overall, this project demonstrates a structured approach to exploratory data analysis, insight generation, and storytelling using real-world data. It reflects an end-to-end analytical workflow—from data preparation to business-focused insights—while emphasizing critical thinking, hypothesis testing, and clear communication.

## Tools Used
- Microsoft Excel 2019
- PivotTables
- PivotCharts
- Slicers
- Calculated fields
