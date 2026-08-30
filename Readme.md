# Sri Lanka Cost of Living & Inflation Analysis

## 📷 Dashboard Screenshots

![alt text](screenshots/dashboard_1.png)

## 📊 Project Overview

An interactive **Microsoft Power BI** dashboard analyzing Sri Lanka's cost of living and inflation.

The project explores retail prices of essential food and non-food items across Sri Lanka's provinces and districts. It provides insights into average prices, monthly and yearly price changes, price levels, product categories, and regional price differences.

## 🎯 Objectives

- Analyze cost-of-living trends in Sri Lanka
- Compare prices across provinces and districts
- Understand monthly (MoM) and yearly (YoY) price changes
- Identify high-priced items and categories
- Analyze regional differences in price movements
- Present insights through an interactive Power BI dashboard

## 📁 Dataset

The dataset contains item-level price information, including:

- Date
- Year
- Quarter
- Month
- Province
- District
- Market Type
- Category
- Subcategory
- Item
- Unit
- Price (LKR)
- Previous Month Price (LKR)
- MoM Change (%)
- Price 12 Months Ago (LKR)
- YoY Change (%)
- Price Index
- Price Level
- Food / Non-Food
- Data Status
- Source Basis

The data covers essential products such as rice, sugar, coconut, vegetables, pulses, cooking oil, flour, and spices across all **9 provinces** of Sri Lanka.

## 🧹 Data Preparation

Data was prepared using **Power Query / Power BI**:

- Standardized date fields
- Checked province and district values
- Checked missing and non-numeric values
- Reviewed price and price-change fields
- Standardized category and item names
- Classified Food and Non-Food items
- Classified prices into Low, Medium, High, and Very High levels

## 📈 Power BI Dashboard

The dashboard includes:

| Visualization | Purpose |
|---|---|
| **KPI Cards** | Average Price, Total Price, Monthly Change, Yearly Change, Item Count, Province Count |
| **Slicers** | Time Period, Item, Price Level, District |
| **Donut Chart** | Number of Items by Subcategory |
| **Bar Chart** | Average Price Index by Category |
| **Pie Chart** | Average Price by Province |
| **Horizontal Bar Chart** | Number of Items by Price Level |
| **Line Chart** | Average Price by Month |
| **Map Visual** | YoY Price Change by District |

## 🔍 Key Findings

- Average retail price: **LKR 832.03**
- Average MoM price change: **1.64%**
- Average YoY price change: **8.92%**
- Approximately **50,000 item-price records**
- Data covers all **9 provinces** of Sri Lanka
- Vegetables and Staple Food are the largest subcategories
- Price levels differ across provinces and districts
- Districts show different year-on-year price movements

## 💡 Recommendations

- Strengthen monitoring of staple food and vegetable prices
- Provide targeted support to areas experiencing higher price increases
- Continue monitoring both MoM and YoY price changes
- Improve local production and supply-chain information
- Combine price data with income and wage data in future analysis
- Investigate High and Very High price-level items

## 🛠️ Tool Used

**Microsoft Power BI Desktop**
