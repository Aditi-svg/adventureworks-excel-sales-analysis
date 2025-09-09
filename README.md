# AdventureWorks Sales Analysis
![Excel](https://img.shields.io/badge/Excel-Power%20Query%20%7C%20Power%20Pivot-217346)
![DAX](https://img.shields.io/badge/DAX-Time%20Intelligence-blue)
![Status](https://img.shields.io/badge/Project-Active-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

> Excel + Power Query + DAX exploration of the classic **AdventureWorks** sales dataset.

**Quick links:** 
- ▶️ **Open raw workbook:** `raw_file/AdventureWorks Sales.xlsx`
- ▶️ **Open data modelling workbook:** `excel/Adventure_data_modelling.xlsb.xlsx`  
- 📷 **Screenshots:** `images/`  
- 🧮 **Measures file:** `measures/DAX_Measures.txt`  
- 🧰 **Date table M:** `powerquery/DateTable_M.txt`

---

## 👀 Overview
This workbook analyzes AdventureWorks sales using **Power Pivot** in Excel.  
The star schema contains **7 tables**:

- **Fact:** `Sales`  
- **Dimensions:** `Customer`, `Date`, `Product`, `Reseller`, `Sales Order`, `Sales Territory`

Relationships use keys like `SalesOrderLineKey` and the **date keys**, enabling DAX measures and slicers to filter by **customer segments**, **product categories**, **reseller types**, **territories**, and **time**.

---

## 🧭 Table of Contents
- [Overview](#-overview)
- [Get Started](#-get-started)
- [Measures (click to expand)](#-measures-click-to-expand)
- [Reports / Worksheets](#-reports--worksheets)
- [Repo Structure](#-repo-structure)
- [Troubleshooting](#-troubleshooting)
- [Notes](#-notes)

---

## 🚀 Get Started
- [ ] Open `excel/AdventureWorks_Sales_Analysis.xlsx`  
- [ ] Enable **Power Pivot** (File → Options → Add-ins → COM Add-ins)  
- [ ] **Refresh All** to load the model  
- [ ] Use slicers (Year, Country, Channel, Category) to explore

> Tip: Time intelligence requires a proper **Date** table marked as *Date Table* and a **valid relationship** from `Sales[date key]` to `Date[date key]`.

---

## 🧮 Measures (click to expand)
<details>
<summary><b>Core KPIs</b></summary>

- **Total_Sales** – Sum of sales revenue (extended amount).  
- **Profit** – `Total_Sales − Total_Product_Cost`.  
- **Gross_Margin_pct** – `Profit ÷ Total_Sales`.  
- **Units_Sold** – Total quantity ordered.  
- **Order_Lines** & **Distinct_Order** – Distinct counts of lines and orders.  
- **AOV (Average Order Value)** – `Total_Sales ÷ Distinct_Order`.
</details>

<details>
<summary><b>Time Intelligence</b></summary>

- **SalesMTD / SalesQTD / SalesYTD** – Month-/Quarter-/Year-to-date sales.  
- **Sales_LY** – Sales for the **same period last year**.  
- **YOY%** – Year-over-year % growth: `(Total_Sales − Sales_LY) ÷ Sales_LY`.  
- **Rolling 12M Sales** – 12-month rolling total.
</details>

<details>
<summary><b>Pricing & Discount</b></summary>

- **Extended Amount / Discount Amount / Discount %**  
- **Product cost** measures (e.g., `Total_Product_Cost`, `Std Cost × Qty`)  
</details>

> Full DAX snippets live in **`/measures/DAX_Measures.txt`** for easy copy/paste.

---

## 📊 Reports / Worksheets
- **Sheet 1 — Monthly Sales Performance**  
  Compare **Total Sales, Profit, Gross Margin %, Units Sold, Distinct Orders, AOV** by **Month/Year** with a Year slicer.

- **Sheet 2 — YoY Growth by Country**  
  Year-over-year % changes in Total Sales per **Country** to spot accelerating/slowing markets.

- **Sheet 5 — Category / Reseller Breakdown**  
  Total Sales by **Product Category** (Accessories, Bikes, Clothing, Components) and **Reseller/Business Type**, with a Year slicer.

- **Sheet 6 — Product Performance**  
  Rank products using **Units Sold, Gross Margin %, Profit** (identify winners/laggards).

- **Sheet 7 — MTD / YTD Sales Summary**  
  Track **SalesMTD** and **SalesYTD** by Month; slicers for **Reseller** and **Product Category**.

> Optional: Add screenshots to `/images` and embed them here:
>
> `![Monthly Sales vs LY](images/monthly_sales_ly.png)`  
> `![Channel Mix](images/channel_mix.png)`

---

