Adventure Works Sales Analysis
Overview

This workbook explores the Adventure Works sales dataset using Power Pivot in Excel. The underlying data model contains seven related tables—Customer, Date, Product, Reseller, Sales, Sales Order and Sales Territory. The Sales table acts as the fact table, while the other tables are dimensions. Relationships are defined on key fields (for example, SalesOrderLineKey and date keys) so that DAX measures and slicers can filter the data by customer segments, product categories, reseller types, territories and time periods.

Measures

A suite of DAX measures has been created to analyse performance from multiple angles:

Total_sales – Sum of the extended amount (revenue) for each sales line.

Profit – Total sales minus total product cost.

Gross_Margin_pct – Profit divided by total sales.

Units_sold – Total quantity ordered.

Order_lines and Distinct_Order – Count of distinct sales order lines and orders.

AOV (Average Order Value) – Total sales divided by the number of distinct orders.

SalesMTD/SalesQTD/SalesYTD – Month‑to‑date, quarter‑to‑date and year‑to‑date cumulative sales using time‑intelligence functions.

Sales_LY – Sales for the same period last year.

YOY% – Year‑over‑year growth, calculated as (Total_sales − Sales_LY) ÷ Sales_LY.

Additional measures for discount amounts, extended amount, product cost and a rolling 12‑month total provide further insight.

Reporting worksheets

Several pivot tables and charts are provided to visualise these measures:

Monthly Sales Performance (Sheet 1) – Compares total sales, profit, gross margin %, units sold, distinct orders and average order value by month and year, with slicers to filter by year.

YOY Growth by Country (Sheet 2) – Shows year‑over‑year percentage changes in total sales for each country, allowing easy identification of markets with accelerating or slowing growth.

Category/Reseller Breakdown (Sheet 5) – Summarises total sales by product category (Accessories, Bikes, Clothing, Components) and by reseller/business type, with a year slicer.

Product Performance (Sheet 6) – Lists individual products along with units sold, gross margin % and profit, so you can rank products by profitability or sales volume.

MTD/YTD Sales Summary (Sheet 7) – Tracks month‑to‑date and year‑to‑date sales by month, with slicers for reseller and product category.
