# Sri Lanka Cost of Living & Inflation Analysis Dashboard


## 📊 Project Overview

Sri Lanka has experienced unprecedented economic volatility following the 2022 debt and foreign-exchange crisis. A direct consequence of this volatility has been persistent and elevated inflation in the cost of essential goods. Households nationwide face steep price increases for staples like rice, pulses, fresh vegetables, sugar, flour, and cooking oils.

While headline inflation figures offer broad national indicators, they mask **significant regional variations, seasonal supply shocks, and commodity-specific spikes**.

This project delivers an interactive **Power BI analytical dashboard** that transforms over **50,000+ granular retail price observations** into actionable intelligence across **all 9 provinces and 25 districts of Sri Lanka**.

---


## 📷 Dashboard Screenshots & Visual Tour

### 1. Executive Overview — National Level
*Full macro analysis covering all 9 Provinces, 25 Districts, 20 Essential Food Items, and over 37.97M aggregated price observations.*

<p align="center">
  <img src="screenshots/dashboard_1.png" alt="Executive Overview - National Level Dashboard" width="100%">
</p>

#### Key Insights from this View:
- **Macro KPI Indicators**:
  - **Total Price Records**: 37.97M (aggregated observations)
  - **Average Retail Price**: **LKR 863.02**
  - **Tracked Commodity Items**: 20 essential products
  - **Geographic Coverage**: 25 Districts across 9 Provinces
- **Price Distribution by Category**: Donut chart detailing item share by category (Vegetables **45%**, Rice **20%**, Spices **10%**, Coconut **5%**, Flour **5%**, Cooking Oil **5%**).
- **Price Records by Category**: Column chart highlighting volume observations across key goods.
- **Time-Series Inflation Curve (2018–2025)**: Multi-year trend line showing price stability pre-2021, rapid inflation surges during 2022–2024, and subsequent consolidation in 2025.
- **Geospatial Map Visual**: Interactive district-level price heat points across Sri Lanka.
- **Cross-Province Commodity Matrix**: Granular comparative matrix evaluating commodity costs (Beans, Cabbage, Carrot, Chilli Powder, Coconut) side-by-side across all provinces.

---

### 2. Regional Deep-Dive — Southern Province & Matara District
Sub-regional drill-down focusing on Southern Province retail dynamics and district-specific market trends

<p align="center">
  <img src="screenshots/dashboard_2.png" alt="Regional Deep-Dive - Southern Province Matara District" width="100%">
</p>

#### Key Insights from this View:
- **District Isolation**: Instant filtering of **1.52M records** specific to the Matara district, revealing an average price of **LKR 864.29**.
- **Localized Map Zoom**: Automatically centers on Southern coastal supply corridors (Matara, Weligama, Hittetiya, Pamburana).
- **Localized Historical Trajectory**: Displays month-over-month price shifts reflecting regional harvest cycles and transportation logistics.
- **Price Matrix Filtering**: Shows exact district pricing for individual vegetable and grocery items.

---

### 3. High Price Level Segmentation — Hambantota District
*Targeted sensitivity analysis isolating "High" price-tier goods within Hambantota District between 2018 and 2022.*

<p align="center">
  <img src="screenshots/dashboard_3.png" alt="High Price Level Segmentation - Hambantota District" width="100%">
</p>

#### Key Insights from this View:
- **Price-Tier Classification**: Isolates commodities classified as **High Price Level**, exhibiting an elevated average price of **LKR 948.66**.
- **Category Composition Shift**: Shows vegetable categories surging to **73.44%** of the high-price basket, alongside edible cooking oils (**26.56%**).
- **Localized Volatility**: Captures sharp upward movements leading into the 2022 economic inflection point.
- **Specific Commodity Benchmarks**: Benchmarks unit prices for Green Chilli (**LKR 1,007.68**), Coconut Oil (**LKR 909.49**), Carrot (**LKR 862.41**), and Red Onion (**LKR 833.37**).

---

## 📈 Power BI Visualizations & Features

| Visual Element | Chart Type | Analytical Purpose |
| :--- | :--- | :--- |
| **KPI Cards** | Multi-card / Single Cards | Displays at-a-glance summary metrics: Total Records, Average Price (LKR), Number of Items, Number of Districts, and Number of Provinces. |
| **Price Distribution by Category** | Donut Chart | Visualizes proportional market basket share across food categories (Vegetables, Rice, Spices, Coconut, Flour, Oil, Pulses, Sugar). |
| **Price Records by Category** | Clustered Column Chart | Quantifies observation frequency per category to identify sampling density. |
| **District-Level Price Comparison** | Filled & Bubble Map | Geospatial visualization highlighting geographic price concentrations across 25 administrative districts. |
| **Price Trends Over Time** | Line Chart | Multi-year time-series tracking historical price escalation, seasonal cycles, and macroeconomic shocks from 2018 to 2025. |
| **Price Comparison by Province & Item** | Matrix Table | Drill-down enabled matrix comparing item-level retail prices across all 9 provinces. |
| **Interactive Slicers** | Hierarchy & Dropdowns | Synchronized slicers for **Year Range**, **Month**, **Item Basket**, **Price Level (Low, Medium, High, Very High)**, and **Province & District tree**. |

---


## 🧹 Data Preparation & ETL Pipeline

Data cleaning and transformations were performed using **Power Query** in Microsoft Power BI Desktop:

1. **Date & Time Dimension Engineering**:
   - Converted date strings to strict datetime format.
   - Derived `Year`, `Quarter`, and `Month` hierarchies for multi-level temporal analysis.
2. **Geographical Cleansing & Standardization**:
   - Standardized provincial and district nomenclature to eliminate typographical duplicates.
   - Linked district names with TomTom / OpenStreetMap geolocation coordinates.
3. **Data Quality & Validation**:
   - Screened price attributes for non-numeric, null, or out-of-range values.
   - Flagged and handled anomalies via the `Data_Status` field.
4. **Calculated Inflation Metrics**:
   - Validated consistency of Month-on-Month (`MoM_Change_%`) and Year-on-Year (`YoY_Change_%`) rate formulations.
   - Standardized the `Price_Index` baseline for fair comparisons across different units of measurement (`kg`, `liter`, `nut`).
5. **Categorical Segmentation**:
   - Created four distinct `Price_Level` tiers: **Low**, **Medium**, **High**, and **Very High** to support rapid outlier discovery.

---

## 💡 Key Findings & Analytical Insights

- **Baseline Retail Level**: The nationwide average retail price across tracked essential commodities is approximately **LKR 832.03 – LKR 863.02**.
- **Persistent Long-Term Inflation**: While the average month-on-month (MoM) increase stands at **1.64%**, the average year-on-year (YoY) increase is **8.92%**, demonstrating sustained price pressure over annual cycles.
- **Dominant Household Expenditure Drivers**: **Vegetables (45%)** and **Staple Foods / Rice (40%)** account for 85% of tracked observations. Supply disruptions in these two categories drive the largest shocks to household cost of living.
- **Regional Disparities**: Coastal and isolated districts (e.g., Hambantota, Trincomalee, Vavuniya) record higher average price points for transported commodities compared to central agricultural production hubs.
- **Macroeconomic Inflection**: The multi-year time trend shows noticeable price escalation beginning in 2021, peaking during the 2022–2024 economic crisis, with structural price plateaus remaining in 2025.

---

## 🎯 Strategic Recommendations

-  **Strengthen Monitoring of Staple Food and Vegetables**: Implement high-frequency price tracking at major Dedicated Economic Centers (e.g., Dambulla, Keppetipola, Peliyagoda) to identify price inflation early.
-  **Optimize Regional Supply Chains & Cold Storage**: Reduce transport and spoilage costs between agrarian production regions and high-cost consumer districts.
-  **Targeted Welfare Support**: Leverage district-level price index data to adjust social safety net transfers (e.g., *Aswesuma*) in regions facing above-average inflation.
-  **Incorporate Wage & Purchasing Power Data**: Integrate household wage data into future dashboards to evaluate real purchasing power rather than nominal price changes alone.
-  **Prioritize High and Very High Tier Items**: Investigate import tariffs, transport margins, and middleman markups on items categorized in the High and Very High price brackets.

---

## 🚀 How to Run the Project

### Execution Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/HimashMadushanka/Sri-Lanka-Cost-of-Living-Analysis-Dashboard.git

   cd Sri-Lanka-Cost-of-Living-Analysis-Dashboard
   ```

2. **Open the Dashboard**:
   - Double-click `dashboard/Sri_Lanka_Cost_of_Living PowerBI.pbix`.
   - Or open **Power BI Desktop**, click **File** > **Open report**, and select the `.pbix` file.

3. **(Optional) Reconnect Dataset**:
   - If Power BI prompts for a data source refresh, go to **Home** > **Transform Data** > **Data source settings**.
   - Update the file path to point to your local `data/Sri_Lanka_Cost_of_Living_50000_PowerBI_Practice.csv`.
   - Click **Apply Changes** and **Refresh**.

---

## 👨‍💻 Author & Academic Credits

- **Author**: **K. Himash Madushanka**
- **Student ID**: `22CDS0420`
- **Institution**: **Sabaragamuwa University of Sri Lanka**
- **Course Module**: Business Intelligence (`DS4108`)
- **Tool**: Microsoft Power BI Desktop

---

