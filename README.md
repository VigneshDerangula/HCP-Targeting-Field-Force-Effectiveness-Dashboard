# 🏥 HCP Targeting & Field Force Effectiveness Dashboard

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

**End-to-end pharma commercial analytics solution — SQL · Python · Power BI · Excel · HTML**

[📊 View Dashboard](#-dashboard-preview) · [🚀 Quick Start](#-quick-start) · [📁 File Structure](#-file-structure) · [📈 Key Insights](#-key-findings)

</div>

---

## 📌 Project Summary

A full-stack pharma **commercial analytics pipeline** built to answer the question:

> *"Is our field force calling the right doctors, at the right frequency, for the right products — and is it translating to revenue?"*

Built across **5 layers** — SQL data model, Python analysis notebook, Power BI interactive dashboard, Excel KPI report, and an HTML prototype — all powered by a **single master dataset** so every KPI is identical across all files.

---

## 🎯 Business Problem

A pharma commercial team had **60 HCPs (Healthcare Professionals)** spread across **5 territories**, served by **7 field reps** making thousands of calls per year. Despite all this activity, leadership had **no visibility** into:

- Which doctors were actually worth visiting (Tier A vs B vs C)?
- Were reps spending time on high-value or low-value HCPs?
- Was call frequency translating to sales lift?
- Which territories were underperforming and why?

---

## 📊 Master KPI Summary

> ✅ All values below are **identical** across Python notebook, SQL queries, HTML dashboard, and Excel file (seed = 2025)

| KPI | Value |
|-----|-------|
| 💰 **Total Net Sales** | ₹3.512M |
| 🎯 **Target Achievement** | 90.6% |
| 📞 **Total Calls Made** | 5,225 |
| ✅ **Call Reach Rate** | 72.0% |
| 🔁 **Call Frequency** | 7.26x / HCP / month |
| 💊 **Adoption Rate** | 100% |
| 💵 **Sales per Call** | ₹672 |
| 👥 **Total HCPs** | 60 (Tier A: 23 · B: 20 · C: 17) |
| 🏆 **Tier A Revenue Share** | 56.1% of total |
| 📈 **Tier A vs C Efficiency** | 1.9x more sales per call |
| 📊 **Pareto Cutoff** | 65% of HCPs → 80% of revenue |

---

## 🔑 Key Findings

### 1. 🎯 Tier A HCPs Are 1.9× More Efficient Per Call
Tier A HCPs (top prescribers) generate **₹769 per call** vs **₹407 for Tier C** — yet call distribution was roughly equal across tiers. Rebalancing just 20% of Tier C call time to high-decile under-served HCPs would meaningfully improve revenue per rep day.

### 2. ⭐ Pareto Principle Confirmed
**65% of HCPs drive 80% of net revenue.** The scatter quadrant analysis revealed a significant "Opportunity" cohort — high-sales-potential doctors receiving below-average call frequency. These are the highest-ROI targets for reallocation.

### 3. 🗺️ Territory Performance Gap
| Territory | Net Sales | Reach % | Growth % |
|-----------|-----------|---------|----------|
| Mumbai | ₹0.88M | 71.4% | +6.3% |
| Delhi | ₹0.87M | 72.2% | +21.4% |
| Kolkata | ₹0.74M | 71.7% | +9.1% |
| Chennai | ₹0.63M | 73.7% | +13.8% |
| Bengaluru | ₹0.39M | 71.0% | +18.2% |

Delhi shows the highest growth momentum (+21.4%). Bengaluru has the lowest sales base but strongest growth trajectory — a signal for investment, not reduction.

### 4. 🌟 Rep Sales Lift Distribution
| Rep | Sales Lift vs Avg |
|-----|-------------------|
| K. Sharma | +25.1% 🌟 |
| P. Iyer | +24.4% 🌟 |
| S. Gupta | +5.0% ✅ |
| R. Nair | -9.9% ⚠️ |
| M. Patel | -44.7% 🔴 |

K. Sharma and P. Iyer are clear outliers — their call patterns and HCP targeting strategy should be replicated across underperforming reps.

---

## 📁 File Structure

```
hcp-targeting-dashboard/
│
├── 📓 HCP_Analysis_SYNCED.ipynb       # Python analysis notebook (Jupyter)
│   ├── Section 1 — Setup & Theme
│   ├── Section 2 — Data Load + KPI Verification (auto-checks vs master)
│   ├── Section 3 — Executive Overview Dashboard (6 KPI cards + 5 charts)
│   ├── Section 4 — HCP Deep Dive (scatter quadrant, Pareto, decile)
│   ├── Section 5 — Territory & Field Force Performance
│   ├── Section 6 — Statistical Analysis (correlation, violin, cohort)
│   └── Section 7 — Insights & Recommendations
│
├── 🗄️ HCP_SQL_Analysis_SYNCED.sql     # SQL analysis file (24 use cases)
│   ├── Section 1 — Star Schema DDL
│   ├── Section 2 — Core KPI Calculations (UC-01 to 03)
│   ├── Section 3 — HCP Targeting Analysis (UC-04 to 09)
│   ├── Section 4 — Territory Performance (UC-10 to 12)
│   ├── Section 5 — Field Force & Rep Performance (UC-13 to 16)
│   ├── Section 6 — Product Analysis (UC-17 to 18)
│   ├── Section 7 — Advanced Analytics & Window Functions (UC-19 to 22)
│   └── Section 8 — Reusable Views (UC-23 to 24)
│
├── 📊 HCP_Dashboard_SYNCED.xlsx       # Excel KPI report (4 sheets)
│   ├── 📊 KPI Dashboard — 18 master KPIs with colour coding
│   ├── 🗺️ Territory KPIs — Full breakdown with totals row
│   ├── 👤 Rep KPIs — Sales lift, reach %, performance bands
│   └── 📅 Monthly Trend — 12 months of sales, calls & reach
│
├── 🌐 HCP_Dashboard_SYNCED.html       # Interactive HTML dashboard prototype
│   ├── 5 KPI cards (live computed values)
│   ├── Sales vs Calls combo chart
│   ├── Tier distribution bar
│   ├── Territory sales breakdown
│   ├── Rep lift bars
│   ├── Territory KPI heatmap
│   ├── Scatter plot (5 territories)
│   └── HCP drilldown table (searchable)
│
└── 📋 HCP_PowerBI_Walkthrough.docx    # 19-step Power BI build guide
    ├── Phase 1 — Import & Model (Steps 1–3)
    ├── Phase 2 — DAX Measures (Steps 4–5)
    ├── Phase 3 — Build Visuals (Steps 6–13)
    ├── Phase 4 — Slicers & Polish (Steps 14–17)
    └── Phase 5 — Publish & Test (Steps 18–19)
```

---

## 🏗️ Data Architecture

```
                    ┌─────────────────┐
                    │   Dim_Date      │
                    │  Date_ID (PK)   │
                    │  Year, Quarter  │
                    │  Month_Name     │
                    └────────┬────────┘
                             │
┌──────────────┐    ┌────────▼────────┐    ┌──────────────────┐
│  Dim_Rep     │    │  Fact_Sales     │    │  Dim_HCP         │
│  Rep_ID (PK) ├────►  Net_Sales      ◄────┤  HCP_ID (PK)     │
│  Rep_Name    │    │  Sales_Target   │    │  Tier (A/B/C)    │
│  Territory   │    │  Product        │    │  Decile (1–10)   │
│  Manager     │    │  Units_Sold     │    │  Specialty       │
│  Therapy     │    │  Gross_Sales    │    │  Decile_Delta    │
└──────────────┘    │  Discount       │    └──────────────────┘
                    └────────┬────────┘
                             │
┌──────────────────┐  ┌──────▼────────┐
│  Dim_Territory   │  │  Fact_Calls   │
│  Territory (PK) ◄───┤  Call_Type    │
│  Region          │  │  Reached Y/N  │
│  Zone, State     │  │  Duration     │
└──────────────────┘  └───────────────┘

Facts  : 720 sales rows · 5,225 call rows
Dims   : 60 HCPs · 7 Reps · 5 Territories · 12 Months
Seed   : 2025 (reproducible — same data across all files)
```

---

## 🚀 Quick Start

### Run the Python Notebook

```bash
# Clone the repository
git clone https://github.com/yourusername/hcp-targeting-dashboard.git
cd hcp-targeting-dashboard

# Install dependencies
pip install pandas numpy matplotlib seaborn openpyxl jupyter

# Launch notebook
jupyter notebook HCP_Analysis_SYNCED.ipynb
```

> **Note:** The notebook regenerates the master dataset using `np.random.seed(2025)` — Cell 2 includes a built-in KPI verification table that auto-confirms all values match the master.

### Run the SQL Queries

```bash
# Using SQLite CLI
sqlite3 hcp_synced.db < HCP_SQL_Analysis_SYNCED.sql

# Or open in any SQL editor (DBeaver, DataGrip, VS Code SQLite extension)
# The file is also compatible with PostgreSQL and MySQL with minor syntax changes
```

### View the HTML Dashboard

```bash
# Simply open in any browser
open HCP_Dashboard_SYNCED.html
# or
double-click HCP_Dashboard_SYNCED.html
```

---

## 🛠️ Tech Stack

| Layer | Tool | Purpose |
|-------|------|---------|
| **Data Model** | SQLite (SQL) | Star schema DDL, 24 analytical use cases |
| **Analysis** | Python + Pandas | Data generation, KPI computation, aggregations |
| **Visualisation** | Matplotlib + Seaborn | 4 full dashboard figures, dark theme |
| **BI Dashboard** | Power BI Desktop | Interactive exec dashboard, 9 DAX measures |
| **Reporting** | Excel (openpyxl) | 4-sheet KPI workbook with colour coding |
| **Prototype** | Vanilla HTML/CSS/JS | Interactive dashboard, no dependencies |
| **Notebook** | Jupyter | Reproducible analysis with built-in verification |

---

## 📐 SQL Use Cases (24 Total)

| # | Use Case | Concept |
|---|----------|---------|
| UC-01 | Executive KPI Summary | Aggregation + JOINs |
| UC-02 | Monthly KPI Trend | GROUP BY date |
| UC-03 | MoM Sales Growth % | Self-JOIN / LAG equivalent |
| UC-04 | HCP Performance Scorecard | Multi-table JOIN + ROW_NUMBER() |
| UC-05 | Tier-wise KPI Comparison | Conditional aggregation |
| UC-06 | Pareto Analysis (80/20) | Running totals + CTE |
| UC-07 | Under-served HCP Identification | Subquery + gap analysis |
| UC-08 | Specialty Sales Mix | GROUP BY + revenue share |
| UC-09 | Decile Movement Breakdown | CASE WHEN segmentation |
| UC-10 | Territory KPI Heatmap | Multi-metric aggregation |
| UC-11 | Territory Ranking | DENSE_RANK() window function |
| UC-12 | 3-Month Rolling Average | ROWS BETWEEN window frame |
| UC-13 | Rep Performance Scorecard | Multi-dimension JOIN |
| UC-14 | Sales Lift % by Rep | CTE + deviation from average |
| UC-15 | Call Type Effectiveness | DENSE_RANK() on efficiency |
| UC-16 | Rep Monthly Gap Analysis | CASE WHEN + gap flagging |
| UC-17 | Product Revenue & Discount | Discount rate calculation |
| UC-18 | Product × Territory Pivot | CASE WHEN pivot |
| UC-19 | YTD Cumulative Sales | SUM() OVER (UNBOUNDED PRECEDING) |
| UC-20 | HCP Percentile & NTILE | PERCENT_RANK() + NTILE(4) |
| UC-21 | Scatter Quadrant (SQL) | Median-based quadrant logic |
| UC-22 | HCP Cohort Segmentation | Activity pattern classification |
| UC-23 | Executive KPI View | CREATE VIEW |
| UC-24 | HCP Master View | Denormalised reporting view |

---

## 📈 Python Analysis Figures

| Figure | Title | Charts Inside |
|--------|-------|--------------|
| **Fig 1** | Executive Overview | 6 KPI cards · Sales vs Calls combo · MoM growth · Tier donut · Territory bars · Rep lift |
| **Fig 2** | HCP Deep Dive | 4-quadrant scatter · Tier×Territory heatmap · Specialty bars · Pareto curve · Decile movement |
| **Fig 3** | Territory & Field Force | KPI heatmap · Rep efficiency scatter · Product donut · Reach by tier · Sales vs target |
| **Fig 4** | Statistical Analysis | Correlation matrix · Violin plots · Pareto II · Stacked cohort · SPC histogram |

---

## 🔁 Data Consistency Guarantee

All 5 deliverables are powered by **one master dataset** (Python seed = 2025). The notebook includes a live verification cell:

```
═══════════════════════════════════════════════════
  KPI VERIFICATION — Python Notebook vs Master
═══════════════════════════════════════════════════
  KPI                          MASTER     NOTEBOOK   OK?
  ─────────────────────────────────────────────────
  Total Net Sales            3512100.0  3512100.0    ✅
  Total Calls                     5225       5225    ✅
  Call Reach %                    72.0       72.0    ✅
  Target Achievement %            90.6       90.6    ✅
  Tier A SPC                     769.0      769.0    ✅
  Tier C SPC                     407.0      407.0    ✅
  SPC Ratio (A/C)                  1.9        1.9    ✅
═══════════════════════════════════════════════════
```

Every SQL query also includes an `-- Expected result:` comment with the pre-verified answer so you can confirm consistency without running anything.


## 🤝 Connect

Feel free to ⭐ star this repo if you found it useful, or reach out via [LinkedIn](https://linkedin.com/in/yourprofile) for questions, collaboration, or feedback.

---

<div align="center">

*Built with Python · SQL · Power BI · Excel · HTML*

</div>
