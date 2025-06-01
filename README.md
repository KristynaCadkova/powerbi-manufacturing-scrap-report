# Production & Warehouse Scrap Report

## Overview
This report provides a comprehensive analysis of scrap across production lines for the year 2024, focusing on both cost and quantity perspectives. It is divided into two main pages:
1. **Scrap Overview** – high-level KPIs, trends, and distributions.
2. **Defect Drilldown** – detailed breakdown by defect categories and cost centers.

The dataset is based on **anonymized data from a real manufacturing company**, enriched with **synthetic data on produced units** to preserve internal data confidentiality while enabling relevant scrap rate calculations.

---

## Page 1: Scrap Overview
- **Primary KPI Cards**: Total Scrap Value, Quantity, Max Single Scrap, Max Unit Price.
- **Trend Analysis**: Monthly scrap development.
- **Scrap Breakdown**: Donut chart by scrap reason, bar chart by cost center.
- **Reclamation Success**: Ratio of successful credit notes.

**Navigation Features**:
- Tab switch between Scrap Value and Quantity.
- Filters for Month, Defect Category, and Cost Center.

---

##  Page 2: Scrap Analysis by Line & Defect
- **FTY Gauge**: First Time Yield (%) with conditional coloring.
- **Scrap Rate vs. Target**: Trend with monthly values and threshold.
- **Pareto Chart**: By defect type, showing cumulative impact.
- **Top Materials by Scrap**: Quantity-based overview.

**Navigation Features**:
- Line selector tiles (CSA, HEL, MSK, SEW).
- Dynamic filters and explanatory annotations for improved UX.

---

##  Logic & Modeling

- Model built on a **star schema** with clearly defined relationships between fact and lookup tables.
- Measures centralized in a custom `[Metrics]` table.
- **Power Query** used for data transformation and enrichment.
- Simulated production data used to enable calculation of PPM, Scrap Rate, and FTY.
- **DAX measures** created for custom KPIs including conditional formatting.
- Conditional formatting applied to FTY, Scrap Rate, and PPM for intuitive signaling.
- Tooltips and filter interactions fine-tuned for clarity.

---

##  Notes for Reviewers
- Default view shows top 20 items by Scrap Value. Slicers allow detailed filtering.
- Tooltips include contextual insights (e.g. revision change in May).
- All visual states preserved through bookmarks for interactivity without losing filter context.
- Author and contact details are placed unobtrusively in the corner of the dashboard for version control and attribution.


---

## 👤 Author
Created by: **Kristýna čadková**  
Email: kristyna.posingerova@seznam.cz  
Discord: kristyna_90682

---
