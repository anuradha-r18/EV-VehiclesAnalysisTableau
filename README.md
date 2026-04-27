# ⚡ Electric Vehicle Population Data Analysis

> A comprehensive data analytics and visualization project exploring EV adoption trends, market dynamics, and clean energy eligibility across the United States.

**Prepared by:** Anuradha Raghuwanshi  
**Dataset:** Washington State EV Population Data  
**Records Analyzed:** 150,482 vehicles

---

## 📌 Project Overview

This project performs an end-to-end analysis of registered electric vehicles in the U.S., with a focus on Washington State. It covers market share by manufacturer, year-over-year adoption growth, vehicle type distribution (BEV vs. PHEV), CAFV eligibility, geographic spread, and top model rankings — culminating in an interactive HTML analytics report and a Tableau/Power BI-style dashboard.

---

## 📁 Project Structure

```
ev-data-analysis/
│
├── Electric_Vehicle_Population_Data.csv   # Raw dataset (150,482 records)
├── EV_Data_Analytics_Report.html          # Full interactive analytics report
├── dashboard_screenshot.png               # Dashboard visual (Tableau/Power BI)
└── README.md                              # Project documentation (this file)
```

---

## 📊 Dataset Description

| Column | Description |
|---|---|
| `VIN (1-10)` | First 10 characters of the Vehicle Identification Number |
| `County` | County of registration |
| `City` | City of registration |
| `State` | U.S. State |
| `Postal Code` | ZIP code |
| `Model Year` | Year of vehicle manufacture |
| `Make` | Vehicle manufacturer (e.g., Tesla, Nissan) |
| `Model` | Vehicle model name |
| `Electric Vehicle Type` | BEV (Battery Electric) or PHEV (Plug-in Hybrid) |
| `Clean Alternative Fuel Vehicle (CAFV) Eligibility` | Whether eligible for clean fuel incentives |
| `Electric Range` | All-electric driving range in miles |
| `Base MSRP` | Manufacturer's suggested retail price |
| `Legislative District` | WA state legislative district |
| `DOL Vehicle ID` | Department of Licensing unique ID |
| `Vehicle Location` | GPS coordinates (POINT format) |
| `Electric Utility` | Associated utility provider |
| `2020 Census Tract` | U.S. Census tract ID |

---

## 🔑 Key Findings

- **150,482** total electric vehicles registered in the dataset
- **77.6%** are Battery Electric Vehicles (BEVs); **22.4%** are PHEVs
- **Tesla** dominates with 68,983 vehicles — **48.15%** of the entire fleet
- **Model Year 2023** hit an all-time high of **37,079 registrations**
- **Washington State** accounts for **99.8%** of all registrations (150,141 vehicles)
- **King County** alone holds **52.5%** of all EVs (79,075 vehicles)
- Average electric range across all vehicles: **67.88 miles**
- **46.3%** of vehicles have unknown CAFV eligibility — a significant policy data gap

---

## 📈 Dashboard Highlights

The interactive dashboard (built in Tableau / Power BI) includes:

- **KPI tiles** — Total Vehicles, BEV count, PHEV count, Avg Electric Range
- **Line/area chart** — Vehicle registrations by Model Year (2011–2024)
- **US Choropleth map** — EV distribution by State
- **Horizontal bar chart** — Top 15 manufacturers by count
- **Ring/donut chart** — CAFV eligibility breakdown
- **Detail table** — Vehicles by Model with EV type and % of total
- **Filter panel** — CAFV Eligibility, EV Type, Model, State

---

## 📑 Analytics Report

The `EV_Data_Analytics_Report.html` file is a fully self-contained interactive report featuring:

- Dark-themed cover page with headline stats
- 9 analysis sections with Chart.js visualizations
- BEV vs. PHEV stacked bar chart by model year
- Top 10 brands leaderboard with relative bar indicators
- County-level geographic breakdown (WA State)
- Strategic insights cards summarizing key takeaways
- Fully interactive charts (hover tooltips, responsive layout)

Open the HTML file in any modern browser — no installation required.

---

## 🚀 How to Use

### View the Report
Simply open `EV_Data_Analytics_Report.html` in a browser:
```bash
open EV_Data_Analytics_Report.html       # macOS
start EV_Data_Analytics_Report.html      # Windows
xdg-open EV_Data_Analytics_Report.html  # Linux
```

### Explore the Data
The raw CSV can be loaded in Python, Excel, Tableau, or Power BI:
```python
import pandas as pd
df = pd.read_csv("Electric_Vehicle_Population_Data.csv")
print(df.shape)         # (150482, 17)
print(df['Make'].value_counts().head(5))
```

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Tableau / Power BI** | Interactive dashboard creation |
| **Chart.js** | JavaScript charting library for the HTML report |
| **Python (pandas)** | Data exploration and statistical analysis |
| **HTML / CSS / JS** | Report design and interactivity |

---

## 💡 Strategic Recommendations

1. **Address the CAFV data gap** — 46.3% unknown eligibility means many owners may be missing clean fuel incentives. Policy outreach and data collection efforts are recommended.
2. **Expand beyond King County** — Over 52% of EVs are concentrated in one county. Investment in suburban and rural charging infrastructure could accelerate broader adoption.
3. **Support emerging brands** — Rivian, Volvo, and Mercedes-Benz are entering the space. Tracking these brands in future datasets will paint a more complete picture of market diversification.
4. **Monitor the 2024 dip** — Only 642 vehicles registered under model year 2024 in this snapshot. This likely reflects dataset timing rather than a real slowdown, but warrants monitoring.

---

*Data Source: Washington State Department of Licensing — Electric Vehicle Population Dataset*

Deployed Link : https://public.tableau.com/views/EVVehiclesAnalysis_17772959942160/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
