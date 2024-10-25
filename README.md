# Project Title: Automotive Sales Database System

## Overview
This project involves the creation and management of an automotive sales database system designed to track vehicle sales, classifications, orders, pricing, and analytics. The database is structured to provide insights into the sales performance and inventory status of vehicles across various regions.

## Main Subquery: Sales Data Analysis
The main subquery, `sales_data`, plays a crucial role in aggregating and filtering essential information about vehicle sales. Here’s a breakdown of what this subquery does, how it is structured, and why it is important:

### Purpose
The `sales_data` subquery aims to provide a comprehensive view of vehicle sales, including key details such as sales region, import dates, delivery and sales-ready dates, pricing, and classifications. This data is vital for understanding the performance of the automotive inventory and guiding strategic decisions regarding sales and marketing.

### Structure
1. **Selection of Columns**: The subquery selects various columns from the `vehicle_data` table and joins them with relevant data from other tables, such as `classification`, `order_data`, `lead_data`, `price_data`, and `market_margins`. This ensures that the resulting dataset contains a holistic view of each vehicle's sales status.
  
2. **Left Joins**: By using left joins, the query ensures that all vehicles are included in the analysis, even if some do not have associated records in the other tables. This is important for maintaining a complete inventory view, as it captures vehicles that might not have been sold yet.

3. **Conditional Logic**: The subquery uses `COALESCE` functions to provide default values for certain fields, ensuring that there are no null entries that could hinder analysis. For example, it replaces missing delivery dates or sales-ready dates with a fallback future date (`'2999-12-31'`), which helps in creating a comprehensive timeline for each vehicle.

4. **Filtering Criteria**: The subquery filters for vehicles that have been imported after a specific date (`'2020-01-01'`) and excludes test vehicles by checking the `test_flag`. This allows for a more focused analysis on actual sales-ready vehicles.

### Importance
The results generated from the `sales_data` subquery serve as the foundation for subsequent analysis in the `inventory_timeline` subquery, which evaluates the inventory's status over time. By understanding the sales performance, stakeholders can make informed decisions regarding marketing strategies, pricing adjustments, and inventory management.

## Conclusion
This database system is designed to enhance the efficiency of automotive sales tracking and analysis. By utilizing structured queries and comprehensive data modeling, it provides valuable insights that can lead to improved sales strategies and customer satisfaction.
