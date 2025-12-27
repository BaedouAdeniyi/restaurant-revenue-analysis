# Restuarant Revenue Analysis

## Project Overview
This project analyzes sales data from a restaurant to understand revenue trends, customer behavior, and product performance. Using Excel, we explored the dataset, calculated key metrics, and created a dashboard to visualize insights. The goal is to show which products and time periods contribute most to revenue, and how customer orders vary throughout the day.

## Project Description
This project analyzes restaurant sales data to understand revenue performance, customer purchasing patterns, and product demand across different time periods. Using Microsoft Excel, I performed exploratory data analysis (EDA), built PivotTables, and created an interactive dashboard to track key performance indicators such as total revenue, order volume, average order value, product category performance, and customer behavior.

The analysis focuses on identifying what drives revenue over time, how customer activity varies by time of day, and how the product mix changes across different periods. Insights from the project highlight the relationship between order volume and revenue, differences in spending behavior by time of day, and the low rate of returning customers. The final output is a visually structured Excel dashboard designed to support data-driven business decisions.

## Business Questions
- How does revenue vary over time (monthly)?
- Which meal category generates the most revenue?
- Which time of day generates the highest revenue and order volume?
- Are there returning customers and what is their impact on revenue?

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

## Tools Used
- Microsoft Excel 2019
- PivotTables
- PivotCharts
- Slicers
- Calculated fields

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
