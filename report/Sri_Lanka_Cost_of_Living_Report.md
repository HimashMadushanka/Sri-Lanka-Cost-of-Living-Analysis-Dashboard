# Sabaragamuwa University of Sri Lanka

## Sri Lanka Cost of Living & Inflation Analysis
### Understanding and Visualizing a Common Sri Lankan Problem Using Power BI

**Individual Assignment Report**

- **Student Name**: K. Himash Madushanka
- **Registration Number**: `22CDS0420`
- **Module Name**: Business Intelligence (`DS4108`)
- **Submission Date**: 20th August 2026
- **Tool Used**: Microsoft Power BI Desktop
- **Video Presentation**: [YouTube Link](https://youtu.be/M14qdr2MkP0)

---

## Table of Contents

1. [Introduction to the Selected Sri Lankan Problem](#1-introduction-to-the-selected-sri-lankan-problem)
2. [Reason for Selecting the Problem](#2-reason-for-selecting-the-problem)
3. [Data Sources Used](#3-data-sources-used)
4. [Data Cleaning and Preparation](#4-data-cleaning-and-preparation)
5. [Power BI Dashboard](#5-power-bi-dashboard)
6. [Key Findings and Insights](#6-key-findings-and-insights)
7. [Recommendations](#7-recommendations)
8. [Conclusion](#8-conclusion)
9. [References](#9-references)
10. [Video Presentation](#10-video-presentation)

---

## 1. Introduction to the Selected Sri Lankan Problem

Sri Lanka has experienced significant economic volatility over the past several years, driven largely by the 2022 debt and foreign-exchange crisis. A direct consequence of this volatility has been persistent, and at times extreme, inflation in the cost of essential goods. Households across the country have faced sharp increases in the prices of food staples such as rice, pulses, vegetables, sugar, and cooking oil, alongside rising costs for non-food essentials. 

These price movements have not been uniform: they vary by province, district, market type, and item category, making the true scale and distribution of the problem difficult to grasp from headline inflation figures alone.

This assignment analyses retail price data for a basket of essential food and non-food items across Sri Lanka's provinces and districts, using Microsoft Power BI to build an interactive dashboard titled **"Sri Lanka Cost of Living & Inflation Analysis."** The dashboard tracks average prices, month-on-month (MoM) and year-on-year (YoY) price changes, and a computed Price Index across categories, subcategories, and regions, so that a viewer can quickly see where cost-of-living pressure is greatest and how it has evolved over time.

---

## 2. Reason for Selecting the Problem

Cost of living and inflation were selected because they are among the most immediate and universally felt economic problems in Sri Lanka today, affecting virtually every household regardless of income level or location. 

As a data professional with experience across analyst and data engineering roles, I wanted to apply data visualization techniques to a problem with genuine social relevance rather than a purely academic dataset. 

The availability of structured, item-level price data with province, district, category, and time dimensions also made this problem particularly well suited to a multi-dimensional Power BI dashboard, allowing comparisons across geography, product category, and time that are difficult to convey through text or static reports alone.

---

## 3. Data Sources Used

The dataset used in this analysis is structured at the item-price level, with the following fields:
- `Date`
- `Year`, `Quarter`, `Month`
- `Province`, `District`
- `Market_Type`
- `Category`, `Subcategory`
- `Item`, `Unit`
- `Price_LKR`
- `Previous_Month_Price_LKR`
- `MoM_Change_%`
- `Price_12_Months_Ago_LKR`
- `YoY_Change_%`
- `Price_Index`
- `Price_Level`
- `Food_NonFood`
- `Data_Status`
- `Source_Basis`

Together these fields allow price tracking for individual items (e.g. rice, sugar, coconut, vegetables, pulses, cooking oil, flour, spices) across nine provinces and their districts, over multiple months and quarters.

---

## 4. Data Cleaning and Preparation

Before building the dashboard, the raw dataset was reviewed and prepared in Power Query / Power BI as follows:

1. **Date Field Standardization**: Verified and standardised the `Date` field and derived `Year`, `Quarter`, and `Month` attributes for time-based analysis.
2. **Geographical Validation**: Checked `Province` and `District` values for consistent spelling and mapped them to a common geography hierarchy used across all visuals.
3. **Data Integrity Checks**: Reviewed `Price_LKR`, `Previous_Month_Price_LKR`, and `Price_12_Months_Ago_LKR` for missing or non-numeric values and removed or flagged incomplete records via the `Data_Status` field.
4. **Metric Validation**: Confirmed `MoM_Change_%`, `YoY_Change_%`, and `Price_Index` were calculated consistently across items, and used these as the basis for trend and comparison visuals.
5. **Categorical Standardisation**: Standardised `Category`, `Subcategory`, and `Item` naming so that visuals such as *"Average Price Index by Category"* and *"Number of Items by Subcategory"* group correctly without duplicate categories.
6. **Segmentation**: Classified each row under `Food_NonFood` and `Price_Level` (Low / Medium / High / Very High) to support the price-level slicer and related visuals.

These steps ensured the dashboard's KPI cards, trend lines, and comparison charts reflect a clean, consistently structured dataset.

---

## 5. Power BI Dashboard

### Dashboard Overview
The dashboard, titled **"Sri Lanka Cost of Living & Inflation Analysis,"** combines KPI cards, slicers, and multiple chart types on a single page so a viewer can move from a national overview to specific provinces, districts, categories, and price levels.

### Dashboard Components
- **KPI Cards**: Average of `Price_LKR`, Sum of `Price_LKR`, Average Monthly Change, Average Yearly Change, Count of Item, and Count of Province, giving an at-a-glance national summary.
- **Slicers**: Time Period, Item, `Price_Level`, and District, allowing the viewer to filter the entire dashboard interactively.
- **Donut Chart**: Number of Items by Subcategory (Vegetables, Staple Food, Cooking Essentials).
- **Bar Chart**: Average Price Index by Category, comparing Spices, Sugar, Oil, Coconut, Vegetables, Rice, Pulses, and Flour.
- **Pie Chart**: Average Price by Province, showing each province's share of total average price.
- **Horizontal Bar Chart**: Number of Items by Price Level (Low, Medium, High, Very High).
- **Line Chart**: Average of `Price_LKR` by Month, showing the overall price trend over the period covered.
- **Map Visual**: YoY Price Change by District, geographically highlighting where year-on-year price increases are concentrated.

---

## 6. Key Findings and Insights

- **General Price Baseline**: The average retail price across the tracked items is approximately **LKR 832.03**, indicating the general price level of the products included in the dataset.
- **Inflation Rates**: The average month-on-month (MoM) price change is **1.64%**, while the average year-on-year (YoY) price change is **8.92%**. This shows that prices experienced noticeable increases over the longer 12-month period.
- **Dataset Coverage**: The dataset contains approximately **50,000 item-price records** covering **all 9 provinces of Sri Lanka**, providing broad geographical coverage for the analysis.
- **Dominant Product Subcategories**: Vegetables and Staple Food are the largest subcategories in the dataset, representing approximately **45% and 40%** of the tracked records respectively. Cooking Essentials account for the remaining approximately **15%**.
- **Provincial Disparity**: The provincial analysis shows differences in the average prices recorded across provinces. This indicates that price levels are not exactly the same across all regions of Sri Lanka.
- **Price Trajectory**: The monthly average price trend shows a general decline from approximately LKR 900 to the low LKR 800 range during the period shown. This suggests that the tracked prices decreased during the observed period, although the positive YoY change indicates that prices may still be higher compared with the corresponding period of the previous year.
- **Price Level Distribution**: The **Medium** price level contains the largest number of tracked items, followed by **High**, **Low**, and **Very High** price levels. This indicates that most items in the dataset are classified within the medium price category.
- **District Variance**: The YoY Price Change by District visualization highlights differences in price movements between districts. Districts such as **Trincomalee and Vavuniya** appear in the visualization and can be examined further to identify areas experiencing notable year-on-year price changes.

---

## 7. Recommendations

1. **Strengthen Price Monitoring of Staple Food and Vegetables**: These are the largest subcategories in the dataset and include many essential household products. Regular monitoring can help identify unusual price increases early.
2. **Provide Targeted Support to Areas Experiencing Higher Price Increases**: Provincial and district-level price data can be used to identify areas with significant YoY price changes and provide appropriate assistance or interventions where necessary.
3. **Continue Monitoring Both MoM and YoY Price Changes**: A positive YoY change together with a lower or declining monthly trend may indicate that prices are stabilising but remain at a relatively high level.
4. **Improve the Availability of Local Production and Supply-Chain Information**: Better understanding of production, transportation, and distribution can help identify the causes of price increases and reduce unnecessary supply-chain costs.
5. **Combine Price Data with Income and Wage Data in Future Analysis**: This would provide a better understanding of whether household purchasing power is keeping pace with rising prices.
6. **Use the Price Level Classification to Identify High-Priced Items**: Items classified as High or Very High can be examined further to identify possible supply, transportation, production, or import-related factors contributing to their higher prices.

---

## 8. Conclusion

The Power BI dashboard developed for this assignment demonstrates that cost of living and inflation remain significant and unevenly distributed problems across Sri Lanka. 

While the average year-on-year price increase of **8.92%** confirms that inflationary pressure is real and sustained, the data also shows that this pressure is concentrated in specific categories — principally staple food and vegetables — and specific provinces and districts. 

Interactive filtering by time period, item, price level, and district allows policymakers, researchers, or ordinary citizens to move beyond national averages and understand exactly where cost-of-living pressure is most acute. Addressing the problem effectively will likely require category- and region-specific interventions rather than a single uniform national policy.

---

## 9. References

- Department of Census and Statistics Sri Lanka (2026) *Retail Prices*. Available at: Department of Census and Statistics – Retail Prices.
- Department of Census and Statistics Sri Lanka (2026) *National Consumer Price Index (NCPI)*. Available at: Department of Census and Statistics – NCPI.
- Central Bank of Sri Lanka (2026) *Measures of Consumer Price Inflation*. Available at: Central Bank of Sri Lanka – Consumer Price Inflation.
- Central Bank of Sri Lanka (2026) *CCPI-based headline inflation*. Available at: Central Bank of Sri Lanka – Inflation in May 2026.
- Microsoft (2026) *Power BI Documentation*. Microsoft Learn. Available at: Microsoft Power BI Documentation.
- Microsoft (2026) *Get started with Power BI Desktop*. Microsoft Learn. Available at: Get started with Power BI Desktop.

---

## 10. Video Presentation

- **YouTube Link**: [https://youtu.be/M14qdr2MkP0](https://youtu.be/M14qdr2MkP0)
