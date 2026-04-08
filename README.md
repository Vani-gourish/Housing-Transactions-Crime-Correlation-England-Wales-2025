# Housing-Transactions&Crime-Correlation-England&Wales-2025

**An end-to-end Power BI dashboard analyzing the correlation between UK housing valuations and localized crime rates (2025)**

<!-- 
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Data Modeling](https://img.shields.io/badge/Data_Modeling-005C8A?style=for-the-badge) 
-->

---

## 📌 Executive Summary
This project bridges the gap between macro-economic real estate trends and micro-level neighborhood safety. By ingesting, modeling, and visualizing public records from HM Land Registry and the UK Home Office, this application provides a dual-lens view of the UK property market: **Financial Valuation** and **Geospatial Risk Assessment**.

### 📸 Dashboard Previews
* **Page 1:** ![Housing Prices](Images/Housing%20Prices.png) 
* **Page 2:** ![Crime Rates](Images/Crime%20Rates.png)

---

## 💡 Key Business Insights
* **Geospatial Correlation:** Demonstrated the statistical relationship between higher-than-average property valuations and incident risk indexes at the city and neighborhood (LSOA) levels.
* **Market Segmentation:** Visualized the disparity in sales volume and market share between new builds and established properties across major metropolitan zones.
* **Proportional Risk Profiling:** Uncovered severe vs. minor crime typologies to identify localized risk hotspots, empowering potential stakeholders (insurance actuaries, real estate investors) with actionable intelligence.

---

## 🛠️ Technical Architecture & Skills Demonstrated

### 1. Advanced Data Modeling
* Engineered a robust **Star Schema** to handle disparate granularity between housing transactions (individual sales) and crime data (aggregated by LSOA).
* Successfully resolved Many-to-Many geographic filtering challenges by building a dedicated `Dim_GeographyBridge` table.

### 2. DAX & Analytical Engineering
* Authored custom DAX measures utilizing `CROSSFILTER` to force bi-directional filtering across complex table relationships.
* Developed dynamic, variable-driven (`VAR`) DAX measures using `ALL()` and `MAXX()` to manipulate filter context and drive custom conditional formatting algorithms.

### 3. Enterprise UI/UX Design
* **Custom Navigation:** Implemented a seamless Page Navigator with dynamic hover and selected states for a web-app feel.
* **State Management:** Utilized Bookmarks to create a 1-click "Reset Filters" global escape hatch.
* **Progressive Disclosure:** Built hidden Report Page Tooltips triggered by invisible card hacks to keep the primary interface clean while offering deep-dive metadata.
* **Strategic Highlighting:** Applied a cohesive "Corporate Fintech" Tailwind color palette (Midnight Blue & Soft Ice Blue), using color deliberately to highlight extreme values (Heatmaps) and guide user attention.

---

## 🔗 Data Lineage & Compliance
All datasets utilized in this report are provided under the Open Government Licence v3.0.
* **Housing Market Data:** [HM Land Registry](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads)
* **Crime & Policing Data:** [Crime & Policing Data](https://data.police.uk/)
* **Geospatial Boundaries:** [ONS Open Geography Portal](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads)

*(Contains HM Land Registry data © Crown copyright and database right 2021).*
