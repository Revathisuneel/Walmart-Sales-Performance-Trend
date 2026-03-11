# Walmart-Sales-Performance-Trend
Walmart Sales Performance Dashboard
Project Overview
This project focuses on building an interactive Walmart Sales Performance Dashboard to analyze store sales trends, compare holiday vs non-holiday performance, and identify high-performing stores.
The dashboard was built using Tableau and helps visualize key retail performance metrics such as Total Sales, Average Sales, Holiday Sales Percentage, and Store-level performance.
The goal of this project is to transform raw sales data into meaningful insights that help understand how seasonal events, holidays, and store performance impact overall revenue.

Business Problem
Retail companies like Walmart generate huge volumes of transaction data across multiple stores and dates. Business teams need quick insights into:
Which stores generate the highest revenue
How sales fluctuate during holidays
Whether holidays significantly impact sales
Average sales performance across stores
This dashboard answers these questions through visual analytics.

Dataset Description
The dataset contains Walmart store sales data with the following fields:
1. Column	Description
2. Store	Store ID
3. Date	Transaction date
4. Weekly_Sales	Total weekly sales
5. Holiday_Flag	Indicates whether the week includes a holiday (1 = Holiday, 0 = Non-Holiday)
6. Temperature	Temperature during the week
7. Fuel_Price	Fuel price during the week
8. CPI	Consumer Price Index
9. Unemployment	Unemployment rate
10. Tools & Technologies

Tableau – Data visualization
Excel / CSV Dataset
Calculated Fields in Tableau
KPI Cards
Scatter Plots
Bar Charts
Filters
Key KPIs Implemented
1 Total Sales

This KPI shows the overall revenue generated across all stores.

Tableau Calculation
SUM([Weekly_Sales])
2 Average Sales
This metric represents the average weekly sales across the dataset.

Tableau Calculation
AVG([Weekly_Sales])

This helps identify the typical store performance over time.

3 Holiday Sales Percentage

This KPI shows what percentage of total sales occur during holiday weeks.

Step 1 – Holiday Sales
SUM(
IF [Holiday_Flag] = 1 THEN [Weekly_Sales]
END
)
Step 2 – Total Sales
SUM([Weekly_Sales])
Step 3 – Holiday Percentage
SUM(
IF [Holiday_Flag] = 1 THEN [Weekly_Sales]
END
)
/
SUM([Weekly_Sales])
Format this value as Percentage in Tableau.

This metric helps determine how much holidays contribute to overall sales.

Dashboard Components
KPI Cards
The top section of the dashboard contains KPI cards showing:
Total Sales
Average Sales
Holiday Sales Percentage
Total Stores
These KPIs provide a quick snapshot of business performance.
Top 10 Stores by Sales
A bar chart showing the highest revenue-generating stores.

Steps:
Drag Store to Rows
Drag Weekly Sales to Columns
Sort descending
Apply Top 10 Filter
This helps identify best performing Walmart locations.
Holiday vs Non-Holiday Sales
A comparison visualization showing how sales change during holidays.
Scatter Plot
Used to visualize:
Holiday sales
Non-holiday sales
Sales distribution across stores
Fields used:
X Axis → Holiday Sales
Y Axis → Non Holiday Sales
Marks → Store
This helps determine whether holidays significantly boost sales.

Dashboard Layout

The dashboard layout includes:
1️⃣ KPI Section (Top)
Total Sales
Average Sales
Holiday Sales %
2️⃣ Sales Analysis
Top 10 Stores by Sales
3️⃣ Holiday Analysis
Holiday vs Non-Holiday Scatter Plot
4️⃣ Filters
Store
Date
This layout ensures clear storytelling and easy navigation for users.

Key Insights

From the dashboard analysis we can observe:
Certain Walmart stores consistently outperform others.
Holiday weeks tend to generate higher sales compared to regular weeks.
Sales distribution varies significantly between stores.
Seasonal trends influence retail performance.
Key Skills Learned
During this project I practiced several important data analytics and visualization skills:
Tableau Dashboard Design
Creating KPI Cards
Writing Calculated Fields
Data aggregation using SUM and AVG
Conditional calculations using IF statements
Creating Top N Filters
Building Scatter Plots
Dashboard storytelling and layout design
