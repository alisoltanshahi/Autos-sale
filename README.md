# Vehicle Inventory Analysis SQL Script

This repository contains a SQL script designed to analyze vehicle inventory data. The script calculates inventory timelines, tracks vehicle status changes, and aggregates inventory metrics by specific intervals. These calculations support reporting on inventory performance and conversion metrics, potentially aiding in A/B testing setups for evaluating how inventory timelines impact sales performance.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Overview
The SQL script is structured around two main parts:
1. **Sales Data Consolidation**: Collects detailed information about vehicles, including sales data, classification attributes, and key dates. This data is gathered from multiple tables and joins, with fallbacks for missing information.
2. **Inventory Timeline Analysis**: Tracks each vehicle's daily inventory status, flags statuses (e.g., reserved, ready for sale), and categorizes inventory days into specific intervals. The final query aggregates this information by sales region and weekly intervals, enabling a time-segmented analysis of inventory.

## Features
- **Detailed Inventory Status**: Tracks each vehicle’s status daily across various inventory categories (e.g., coming soon, available online).
- **Aggregated Weekly Metrics**: Summarizes inventory duration across customizable time intervals.
- **Support for Conversion Analysis**: Provides a data structure that can support A/B testing setups for inventory-related conversion metrics.
- **Customizable Intervals**: Day-based intervals (0-7 days, 8-14 days, etc.) make it easy to segment inventory for further analysis.

## Usage
Load the SQL script into your preferred SQL environment or editor.
Run the script to generate a timeline of inventory data for each vehicle.
Use the final aggregated data for weekly reporting, conversion analysis, or as part of an A/B testing framework.
## SQL Breakdown
sales_data CTE: Consolidates vehicle data from various tables (e.g., vehicle data, classifications, orders) and fills missing dates using fallback values.
inventory_timeline CTE: Calculates inventory days and status flags for each vehicle daily, providing an in-depth view of the inventory life cycle.
Final Query: Aggregates weekly counts of vehicles in each inventory category by region.
## Dependencies
SQL environment (e.g., MySQL, PostgreSQL, etc.) with access to the required tables:
vehicle_data, classification, order_data, lead_data, price_data, market_margins, calendar_dates.
## Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss any improvements or modifications.

License
This project is licensed under the MIT License.
