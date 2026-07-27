# Bluestock Fintech — Mutual Fund Analytics Capstone

**Internship:** Bluestock Fintech | Cohort MJ28
**Role:** Data Analyst Intern
**Author:** Aminu Momodu Audu
**Duration:** June 3 – June 12, 2026

---

## Project Overview

A full-stack Mutual Fund Analytics Platform built on 10 official
datasets covering 40 real AMFI mutual fund schemes across 10 fund
houses. The project covers ETL, SQL database design, EDA, performance
analytics, interactive dashboards, advanced risk analytics and a
Flask REST API.

---

## Official Datasets — 10 files, 87,533 rows

| # | File | Description | Rows |
|---|------|-------------|------|
| 1 | 01_fund_master.csv | 40 real AMFI fund schemes | 40 |
| 2 | 02_nav_history.csv | Daily NAV Jan 2022 to May 2026 | 46,000 |
| 3 | 03_aum_by_fund_house.csv | Quarterly AUM 10 fund houses | 90 |
| 4 | 04_monthly_sip_inflows.csv | Monthly SIP inflows | 48 |
| 5 | 05_category_inflows.csv | Net inflows by category | 144 |
| 6 | 06_industry_folio_count.csv | Investor folios by type | 21 |
| 7 | 07_scheme_performance.csv | Sharpe Beta Alpha per scheme | 40 |
| 8 | 08_investor_transactions.csv | 32K investor transactions | 32,778 |
| 9 | 09_portfolio_holdings.csv | Stock holdings per fund | 322 |
| 10 | 10_benchmark_indices.csv | Nifty 50 Nifty 100 BSE daily | 8,050 |

---

## Deliverables

| ID | Deliverable | Format | Weight | Status |
|----|-------------|--------|--------|--------|
| D1 | ETL Pipeline | .ipynb + .py | 15% | Done Day 1 |
| D2 | SQLite Database | .db | 10% | Done Day 2 |
| D3 | EDA Notebook | .ipynb | 15% | Done Day 3 |
| D4 | Performance Metrics | .ipynb + CSV | 15% | Done Day 4 |
| D5 | Interactive Dashboard | .pbix | 20% | Done Day 5 |
| D6 | Advanced Analytics | .ipynb | 10% | Done Day 6 |
| D7 | Final Report + Slides | .pdf + .pptx | 15% | Done Day 7 |
| BONUS | Flask REST API | .py | Extra | Done |

---

## Day 1 Results

- Loaded 10 official datasets — 87,533 rows total
- Explored 40 AMFI fund schemes across 10 fund houses
- Validated 40 AMFI codes — 100% match across all datasets
- Fetched live NAV from mfapi.in for 5 key schemes
- Generated official Data Quality Report
- Committed and pushed to GitHub

---

## Day 2 Results

- Cleaned all 10 datasets successfully
- NAV history forward-filled to 64,320 rows
- Designed 9-table SQLite star schema
- Loaded 105,832 rows into bluestock_mf.db
- Wrote and executed 10 SQL analytical queries
- Created official data dictionary
- Pushed all work to GitHub

---

## Day 3 Results

- Created 15 publication-quality charts
- NAV trends, AUM growth, SIP inflows analysed
- Investor demographics and geographic distribution mapped
- Correlation matrix and sector allocation computed
- Benchmark comparison — Nifty Midcap 150 best at +237%
- Documented 10 key EDA findings
- Pushed all charts and notebook to GitHub

---

## Day 4 Results

- Computed daily returns for 40 funds over 1,607 trading days
- Calculated CAGR for 1yr, 3yr and 5yr periods
- Computed Sharpe ratio and Sortino ratio for all 40 funds
- Computed Alpha and Beta vs Nifty 100 benchmark
- Computed Maximum Drawdown — worst: SBI Small Cap -52.57%
- Built composite Fund Scorecard — SBI Small Cap Direct ranked 1st
- Created official etl_pipeline.py — runs without errors
- Pushed all files to GitHub

---

## Day 5 Results

- Built 4-page interactive Power BI dashboard
- Page 1: Industry Overview — 4 KPI cards, AUM growth chart
- Page 2: Fund Performance — Scorecard table, Top 10 bar chart
- Page 3: Investor Analytics — Demographics, Geography charts
- Page 4: SIP and Market Trends — SIP inflows, Benchmarks
- Added interactive slicers to all 4 pages
- Exported dashboard to PDF
- Pushed bluestock_mf_dashboard.pbix to GitHub

---

## Day 6 Results

- Computed Historical VaR 95% and CVaR for all 40 funds
- ABSL Small Cap has worst VaR at -2.39% daily
- Computed Rolling 90-day Sharpe — SBI Bluechip leads at 3.37
- Investor Cohort Analysis — 4,803 in 2024 cohort vs 197 in 2025
- SIP Continuity Analysis — 99.9% investors have irregular SIPs
- Built Fund Recommender System for Low, Moderate, High risk
- Sector HHI Analysis — all funds show Low to Moderate concentration
- Pushed all analytics to GitHub

---

## Day 7 Results

- Wrote 15-page professional Final Report PDF
- Created 12-slide Presentation with Midnight Executive theme
- Report covers ETL, EDA, Performance, Dashboard, Advanced Analytics
- Presentation includes fund scorecard, recommendations and key findings
- Pushed Final_Report.pdf and Presentation.pptx to GitHub
- All 7 capstone deliverables completed before June 12 deadline

---

## Bonus — Flask REST API

A REST API built with Flask serving mutual fund analytics insights
as live JSON data.

| Endpoint | Description |
|----------|-------------|
| GET / | API home and available endpoints |
| GET /api/top-funds | Top 5 funds by composite score |
| GET /api/market-insights | Key market findings |
| GET /api/fund-recommender/low | Low risk recommendation |
| GET /api/fund-recommender/moderate | Moderate risk recommendation |
| GET /api/fund-recommender/high | High risk recommendation |

Run with: `python scripts/app.py`
Then visit: http://localhost:5000

---

## Folder Structure

```
bluestock_mf_capstone/
├── data/
│   ├── raw/           original CSV files (excluded via .gitignore)
│   ├── processed/     cleaned CSVs (excluded via .gitignore)
│   └── db/            SQLite database (excluded via .gitignore)
├── notebooks/
│   ├── Day1_Official_Data_Ingestion.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_eda_analysis.ipynb
│   ├── 04_performance_analytics.ipynb
│   ├── 05_powerbi_prep.ipynb
│   └── 06_advanced_analytics.ipynb
├── scripts/
│   ├── etl_pipeline.py
│   ├── recommender.py
│   └── app.py
├── sql/
│   ├── schema.sql
│   └── queries.sql
├── dashboard/
│   └── bluestock_mf_dashboard.pbix
├── reports/
│   ├── Final_Report.pdf
│   ├── Presentation.pptx
│   ├── bluestock_mf_dashboard.pdf
│   ├── Day4_Performance_Summary.txt
│   ├── Day6_Advanced_Analytics_Summary.txt
│   ├── EDA_Findings.txt
│   ├── data_dictionary.md
│   └── charts/
└── README.md
```

---

## Quick Start

```bash
pip install -r requirements.txt
jupyter notebook notebooks/
```

---

## Tech Stack

Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly,
SQLite, SQLAlchemy, Requests, SciPy, Flask,
Power BI, Jupyter Notebook, Git

---

*Bluestock Fintech Internship | Cohort MJ28 | June 2026*
*Author: Aminu Momodu Audu*
