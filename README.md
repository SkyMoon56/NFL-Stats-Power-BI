# 🏈 2023 NFL Player Performance Dashboard

![Dashboard Preview](assets/dashboard-main.png)

## 📄 Project Overview
This interactive Power BI dashboard analyzes performance metrics for NFL players across multiple positions (QB, RB, WR, TE). The goal was to transform raw statistical data into a decision-support tool for fantasy football analysis, identifying high-performing outliers and efficiency trends.

## 🛠 Tools Used
- **Microsoft Power BI** (Data Visualization & UI)
- **DAX** (Custom Measures & Complex Calculations)
- **Power Query** (Data Cleaning & Transformation)

## 📊 Key Features
- **Unified Metrics:** Used DAX to create a `Total Yards` measure that combines Passing and Rushing stats, solving data silo issues for dual-threat players.
- **Dynamic Quadrant Analysis:** Scatter plots feature dynamic average lines that recalculate based on the selected position, separating elite performers from the average.
- **Dark Mode UI:** Designed a high-contrast, accessible interface with rounded visuals and clean KPI cards.
- **Position Filtering:** Custom slicers allow users to toggle between positions (QB vs. RB) to instantly update all visuals and rankings.

## 🧠 Technical Highlights
**1. Custom DAX Measure:**
To capture total offensive output, I created a flexible measure that aggregates yards regardless of source:
```dax
Total Yards = SUM('Stats'[passing_yards]) + SUM('Stats'[rushing_yards])
