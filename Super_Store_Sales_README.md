# Super_Store_Sales_Dashboard

# Dashboard link: https://app.powerbi.com/links/uv93QBG_Pi?ctid=4665b27a-3ddb-4591-bc0a-775b49a891bd&pbi_source=linkShare

# Objective
Analyze and improve sales performance of a superstore by creating an interactive Power BI dashboard.

# Key Insights
Sales Trends: Identify peak sales periods and seasonal trends.
Product Performance: Determine which products are top sellers and which are underperforming.
Customer Segmentation: Analyze customer demographics and purchasing behavior.
Geographical Insights: Understand sales distribution across different regions.
Profit Margins: Evaluate profitability by product category and region.

# Key DAX Formulas
Total Sales
Formula: Total Sales = SUM(Sales[Sales Amount])
Explanation: This formula calculates the total sales amount by summing up the values in the Sales Amount column of the Sales table.
Total Profit
Formula: Total Profit = SUM(Sales[Profit])
Explanation: This formula sums up the profit values from the Profit column in the Sales table to get the total profit.
Sales by Region
Formula: Sales by Region = CALCULATE([Total Sales], ALLEXCEPT(Sales, Sales[Region]))
Explanation: This formula calculates the total sales for each region by removing all filters except the Region column.
Top Products by Sales
Formula: Top Products = TOPN(10, SUMMARIZE(Sales, Products[Product Name], "Total Sales", [Total Sales]), [Total Sales], DESC)
Explanation: This formula returns the top 10 products based on total sales. It uses the SUMMARIZE function to group by product name and calculate total sales, then TOPN to get the top 10.
Year-to-Date Sales
Formula: YTD Sales = TOTALYTD([Total Sales], 'Date'[Date])
Explanation: This formula calculates the year-to-date sales by summing the total sales from the beginning of the year to the current date.
Brief Explanation
Total Sales and Total Profit are basic aggregations to get overall performance metrics.
Sales by Region helps in understanding geographical performance by isolating sales data for each region.
Top Products by Sales identifies the best-performing products, aiding in inventory and marketing decisions.
Year-to-Date Sales provides a cumulative sales figure for the current year, useful for tracking progress against annual targets.

# Learning Journey
Data Import and Cleaning: Import sales data and clean it using Power Query Editor.
Data Modeling: Create relationships between tables and define hierarchies.
DAX Functions: Use DAX to create calculated columns, measures, and tables for deeper analysis.
Dashboard Design: Design the dashboard with advanced charts, maps, filters, and slicers.
Sales Forecasting: Implement sales forecasting using Power BI’s built-in features.
Export and Share: Export the dashboard as a PDF and share insights.
# What I Learned
Data Preparation: Importance of clean and well-structured data for accurate analysis.
DAX Proficiency: How to leverage DAX for complex calculations and data manipulation.
Visualization Techniques: Effective use of visual elements to convey insights clearly.
Interactivity: Enhancing user experience with interactive elements like slicers and filters.
Forecasting: Basics of implementing forecasting models in Power BI.

# Final Conclusion to Improve Sales
Focus on High-Performing Products: Allocate more resources to top-selling products.
Targeted Marketing: Use customer segmentation data to tailor marketing campaigns.
Optimize Inventory: Adjust inventory levels based on sales trends and forecasts.
Expand in High-Growth Regions: Invest in regions showing strong sales growth.
Monitor and Adjust: Continuously monitor sales performance and adjust strategies accordingly.
