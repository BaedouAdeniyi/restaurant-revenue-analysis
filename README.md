# Restuarant Revenue Analysis

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

## Exploartory Data Analysis (EDA)
The exploratory data analysis focused on understanding revenue performance, customer ordering behavior, and product preferences across different time periods.

Revenue patterns were examined by product category, time of day, and over time to identify key revenue drivers and trends.
Order behavior was analyzed using order counts and order volume trends to understand customer activity levels.
Average order value was explored across time periods and on a monthly basis to assess customer spending behavior.
Product mix analysis was conducted to understand how customer preferences differ by time of day.
Finally, customer repeat behavior was reviewed to provide context on customer retention.

These analyses informed the selection of KPIs and visuals used in the final dashboard.

## Key Findings
### Key Insight 1:Revenue Performance Over Time
Question we are answering
- How has revenue performed over time, and what factors drive changes in revenue?

Revenue shows noticeable variation over time rather than steady growth. Some months record strong increases, while others experience slowdowns or dips, indicating that revenue is not evenly distributed across the year.

A closer look shows that these changes are mainly driven by fluctuations in the number of orders rather than large changes in average order value. During high-revenue months, order volume increases significantly, while average order value remains relatively stable. In lower-revenue months, fewer orders are placed, which directly reduces total revenue.

This suggests that revenue performance is largely volume-driven. Improving customer acquisition, repeat purchases, or order frequency would likely have a greater impact on revenue growth than focusing only on increasing prices or basket size.

### Key Insight 2: Time-of-Day Performance
Revenue is highest in the morning, followed by the afternoon, evening, and night. Morning revenue is nearly twice that of the afternoon, while afternoon and evening revenues are very similar. Evening revenue is almost 2.5 times higher than night revenue.

To understand what drives this pattern, revenue was broken down into order volume and average revenue per order.

Order count closely mirrors the revenue trend across time periods, indicating that higher morning revenue is primarily driven by a higher number of orders, not higher spend per order.

In contrast, average revenue per order is highest in the afternoon, followed by evening and night, with morning having the lowest average order value. Afternoon average revenue is nearly twice that of the evening, suggesting that although fewer customers visit in the afternoon, each transaction generates more revenue.ther order main dishes or combine starter + main

To explain this difference, a hypothesis was tested on product mix by time of day. The analysis showed that:

- Starters and desserts are ordered more frequently in the morning
- Main meals (often combined with starters) are ordered more frequently in the afternoon

This explains the higher afternoon average order value. Main meals account for the largest share of revenue (≈42%), compared to starters (≈39%) and desserts (≈38%), confirming that meal composition (not customer volume) drives higher afternoon revenue per order.

  - What was observed
  - Why it happened
  - Why it matters





  - What was observed
  - Why it happened
  - Why it matters

## Tools Used
- Microsoft Excel 2019
- PivotTables
- PivotCharts
- Slicers
- Calculated fields
