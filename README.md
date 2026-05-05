<div align="center">

# ⚡ EV Sales Analytics Dashboard

**A multi-page Power BI report tracking Electric Vehicle market performance across regions, brands, fuel types, charging infrastructure, and sales trends in the Indian market.**

<br/>

[![Power BI](https://img.shields.io/badge/Built_With-Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com)
[![Pages](https://img.shields.io/badge/Report_Pages-4-0078D4?style=for-the-badge)](.)
[![Theme](https://img.shields.io/badge/Theme-Fluent2-5C2D91?style=for-the-badge&logo=microsoft&logoColor=white)](.)
[![Status](https://img.shields.io/badge/Status-Active-2ea44f?style=for-the-badge)](.)

</div>

---

## 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Dashboard Preview](#-dashboard-preview)
3. [KPI Cards](#-kpi-cards)
4. [Report Pages](#-report-pages)
5. [Key Insights](#-key-insights)
6. [Data Model & DAX](#-data-model--dax)
7. [Filters & Slicers](#-filters--slicers)
8. [Setup & Installation](#-setup--installation)
9. [Folder Structure](#-folder-structure)
10. [Contributing](#-contributing)

---

## 🔍 Project Overview

This Power BI dashboard delivers end-to-end visibility into the Indian Electric Vehicle (EV) market. Designed for business analysts, automotive strategists, and policy makers, it enables data-driven decisions through four dedicated report pages covering **sales performance, regional distribution, fuel & charging types, and long-term trends**.

**Data Sources: Kaggle.com**

| Table | Role | Key Columns |
|---|---|---|
| `EV_Sales` | Fact Table | Brand, Region, State, Vehicle_Type, Fuel_Type, Charging_Type, Units_Sold, Total_Revenue_INR |
| `DateTable` | Date Dimension | Date, Month, Quarter, Year |

---

## 🖼 Dashboard Preview

<br/>

**Page 1 — Overview**

<img width="2075" height="1200" alt="ev sales_page-0001" src="https://github.com/user-attachments/assets/fb0a0792-b754-41a7-8864-8ace40ebbdcc" />

---

**Page 2 — Geographics**

<img width="2075" height="1200" alt="ev sales_page-0002" src="https://github.com/user-attachments/assets/2b4e6b42-f306-4ede-8a2d-71c4ef80e6b6" />


---

**Page 3 — Fuel & Charging**

<img width="2075" height="1200" alt="ev sales_page-0003" src="https://github.com/user-attachments/assets/222a32f6-7db6-45ea-9ce5-9c8552fe2d6e" />


---

**Page 4 — Trends**

<img width="2075" height="1200" alt="ev sales_page-0004" src="https://github.com/user-attachments/assets/873af31d-1969-4df1-a2a2-67e18c23c89d" />



---

## 📊 KPI Cards

Ten headline metrics appear persistently across all four pages. Each card dynamically updates when any slicer filter is applied.

<br/>

<div align="center">

| &nbsp; | Metric | Description |
|:---:|---|---|
| 💰 | **Total Revenue** | Sum of all EV sales revenue in INR |
| 🚗 | **Total Units Sold** | Total number of EVs sold across all segments |
| 🏛️ | **Total Subsidy** | Cumulative government subsidies disbursed |
| 💲 | **Avg Vehicle Price** | Average price per EV unit (INR) |
| ⚡ | **BEV Share %** | Battery EVs as a percentage of total units sold |
| 🔋 | **Avg Battery kWh** | Mean battery capacity across vehicle types |
| 🛣️ | **Avg Range km** | Average driving range per full charge |
| 🏆 | **Top Brand** | Highest-revenue EV brand under current filters |
| 📍 | **Top State** | State contributing the highest EV sales volume |
| 📅 | **Top Month** | Peak revenue month under current filters |

</div>

<br/>

> **How these cards work:** Each KPI uses a `cardVisual` in Power BI fed by a DAX measure. Cards respond live to all cross-page slicers — change a Region or Year filter and every card updates instantly.

---

## 📑 Report Pages

### Page 1 — Overview

The executive summary. Designed for leadership and high-level stakeholders who need the full picture at a glance.

| Visual | Chart Type | What It Shows |
|---|---|---|
| Revenue Over Time | Line Chart | Monthly revenue by Year for YoY comparison |
| Sales by Vehicle Type | Donut Chart | Revenue share across 2W / 3W / 4W segments |
| KPI Row | Card Visuals (×6) | Revenue, Units, Subsidy, Avg Price, Top Brand, BEV Share, Top State, Top Month |

---

### Page 2 — Geographics

Regional intelligence — where EVs sell and which brands lead.

| Visual | Chart Type | What It Shows |
|---|---|---|
| Revenue by State | Horizontal Bar | Top states ranked by total EV revenue |
| Revenue by Region | Horizontal Bar | North / South / East / West breakdown |
| Quarterly Revenue by Region | Clustered Column | Q1–Q4 revenue across regions by Year |
| Top 8 Brands | Clustered Bar | Revenue + Units side-by-side per brand |

---

### Page 3 — Fuel & Charging

Technology and policy analysis — how EVs are powered, charged, and subsidised.

| Visual | Chart Type | What It Shows |
|---|---|---|
| Units by Fuel Type | Donut Chart | BEV / PHEV / HEV / FCEV split |
| Units by Charging Type | Donut Chart | Fast / Slow / Swap / Solar infrastructure share |
| Units by Subsidy Scheme | Donut Chart | FAME-II / State Scheme / No Subsidy breakdown |
| Revenue by Customer Segment | Clustered Column | Fleet / Individual / Government / Corporate |

---

### Page 4 — Trends

Longitudinal analysis — how EV adoption and technology evolve over time.

| Visual | Chart Type | What It Shows |
|---|---|---|
| Units Sold by Fuel Type Over Time | Line Chart | YoY adoption trend per fuel technology |
| Avg Battery & Range by Vehicle Type | Clustered Column | Technical benchmark across vehicle categories |
| KPI Row | Card Visuals (×4) | Revenue, Units Sold, Subsidy, Avg Price |

---

## 💡 Key Insights

> These insights are derived from the dashboard's analytical structure. Actual values will depend on your connected dataset.

**1. Revenue Seasonality**
The month-over-month line chart on the Overview page surfaces seasonal peaks. Cross-filtering by Year enables direct YoY revenue comparison for any selected region or brand.

**2. BEV Market Dominance**
The BEV Share % KPI measures how rapidly Battery EVs are displacing HEVs and PHEVs. Rising BEV share signals accelerating consumer preference for pure electric over hybrid powertrains.

**3. Regional Concentration**
The Geographics page typically reveals that a small number of states (likely metro-adjacent) drive a disproportionate share of total EV revenue, signalling where infrastructure and marketing investment is paying off.

**4. Brand Concentration**
The Top 8 Brands bar chart highlights how concentrated the competitive landscape is — a handful of brands tend to capture the majority of both volume and revenue.

**5. Subsidy Dependency**
The Subsidy Scheme donut shows what proportion of the market is driven by FAME-II and state-level incentives versus unsubsidised organic demand. High subsidy dependency is a policy risk indicator.

**6. Charging Infrastructure Gap**
The Charging Type donut exposes over-reliance on slow charging, which points to fast-charge and battery-swap infrastructure as priority investment areas.

**7. B2B vs B2C Revenue**
The Customer Segment column chart reveals whether fleet and corporate buyers or individual consumers are the primary revenue contributors — critical for sales and marketing strategy.

**8. Technology Improvement Trend**
Avg Battery kWh and Avg Range km tracked by vehicle type on the Trends page demonstrate measurable YoY improvements in EV technical specifications.

---

## 🗂 Data Model & DAX

### Entity Relationship

```
EV_Sales (Fact)
    │
    │  Many-to-one on Date
    │
DateTable (Dimension)
```

### EV_Sales — Column Reference

```
EV_Sales
├── Date               → FK to DateTable
├── Brand              → EV manufacturer
├── Region             → Geographic region (North/South/East/West)
├── State              → Indian state
├── Vehicle_Type       → 2W / 3W / 4W
├── Fuel_Type          → BEV / PHEV / HEV / FCEV
├── Charging_Type      → Fast / Slow / Swap / Solar
├── Customer_Segment   → Individual / Fleet / Corporate / Government
├── Subsidy_Scheme     → FAME-II / State / None
├── Units_Sold         → Transaction unit count
└── Total_Revenue_INR  → Revenue in Indian Rupees
```

### Key DAX Measures

```dax
-- Volume & Revenue
Total Units Sold  = SUM ( EV_Sales[Units_Sold] )
Total Revenue     = SUM ( EV_Sales[Total_Revenue_INR] )
Avg Vehicle Price = DIVIDE ( [Total Revenue], [Total Units Sold] )

-- Subsidy
Total Subsidy = SUM ( EV_Sales[Subsidy_Amount] )

-- Technology KPIs
Avg Battery kWh = AVERAGE ( EV_Sales[Battery_kWh] )
Avg Range km    = AVERAGE ( EV_Sales[Range_km] )

-- Market Mix
BEV Share =
DIVIDE (
    CALCULATE ( [Total Units Sold], EV_Sales[Fuel_Type] = "BEV" ),
    [Total Units Sold]
)

-- Dynamic Top-N Labels
Top Brand =
MAXX (
    TOPN ( 1, VALUES ( EV_Sales[Brand] ), [Total Revenue], DESC ),
    EV_Sales[Brand]
)

Top State =
MAXX (
    TOPN ( 1, VALUES ( EV_Sales[State] ), [Total Units Sold], DESC ),
    EV_Sales[State]
)

Top Month =
MAXX (
    TOPN ( 1, VALUES ( DateTable[Month] ), [Total Revenue], DESC ),
    DateTable[Month]
)

-- Top 8 Brands Flag (filters the brand bar chart)
Top 8 Flag =
IF (
    RANKX ( ALL ( EV_Sales[Brand] ), [Total Revenue],, DESC ) <= 8,
    "Top 8",
    "Other"
)
```

---

## 🎛 Filters & Slicers

All slicers cross-filter every visual on their respective page. Slicers on the navigation bar apply globally.

| Slicer | Page Scope | Field |
|---|---|---|
| Year | All Pages | `DateTable[Year]` |
| Quarter | All Pages | `DateTable[Quarter]` |
| Region | All Pages | `EV_Sales[Region]` |
| Brand | All Pages | `EV_Sales[Brand]` |
| Vehicle Type | All Pages | `EV_Sales[Vehicle_Type]` |
| State | Geographics | `EV_Sales[State]` |
| Fuel Type | Fuel & Charging, Trends | `EV_Sales[Fuel_Type]` |
| Charging Type | Fuel & Charging | `EV_Sales[Charging_Type]` |
| Subsidy Scheme | Fuel & Charging | `EV_Sales[Subsidy_Scheme]` |
| Customer Segment | Fuel & Charging | `EV_Sales[Customer_Segment]` |

---

## 🚀 Setup & Installation

### Requirements

- Power BI Desktop **2.8.0 or later**
- Access to source EV sales data (CSV or database)

### Step 1 — Clone the Repository

```bash
git clone https://github.com/your-username/ev-sales-dashboard.git
cd ev-sales-dashboard
```

### Step 2 — Open in Power BI Desktop

```
File → Open → ev_sales.pbix
```

### Step 3 — Connect Your Data

If the report opens with a data source error:

```
Home → Transform Data → Data Source Settings → Change Source
```

Point Power BI to your local CSV file or database connection.

### Step 4 — Refresh

```
Home → Refresh
```

All visuals and KPI cards will populate once the data loads.

### Step 5 — Publish to Power BI Service (optional)

```
Home → Publish → Select Workspace → Publish
```

Then configure a scheduled refresh in [Power BI Service](https://app.powerbi.com) under:

```
Dataset Settings → Scheduled Refresh
```

---

## 📁 Folder Structure

```
ev-sales-dashboard/
│
├── ev_sales.pbix              ← Power BI report file
├── README.md                  ← This file
│
├── data/
│   └── ev_sales_data.csv      ← Source dataset (add your own)
│
└── screenshots/
    ├── overview.jpg            ← Page 1 screenshot
    ├── geographics.jpg         ← Page 2 screenshot
    ├── fuel_charging.jpg       ← Page 3 screenshot
    └── trends.jpg              ← Page 4 screenshot
```
---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

```bash
# 1. Fork the repo
# 2. Create your feature branch
git checkout -b feature/add-state-drillthrough

# 3. Commit your changes
git commit -m "feat: add state-level drill-through on Geographics page"

# 4. Push and open a Pull Request
git push origin feature/add-state-drillthrough
```

---


<div align="center">

Made with ⚡ for EV market analytics

*If this helped you, drop a ⭐ — it keeps the project alive!*

</div>
