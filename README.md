# 🏈 2023 NFL Player Performance Dashboard


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
```
## 📊 Frequently Asked Questions (FAQ)

Explore the details of the NFL Stats Power BI project through these common questions and answers.

---

### 🏈 Project Overview

**Q: What is the primary goal of this dashboard?** **A:** This project provides a comprehensive, interactive visualization of NFL player and team performance. It transforms raw seasonal data into actionable insights for fantasy football, team scouting, and general sports analytics.

**Q: What tools were used to build this?** **A:** The project is built entirely within the **Microsoft Power BI** ecosystem, utilizing:
* **Power Query (M):** For data extraction and cleaning.
* **DAX:** For complex calculations and custom KPIs.
* **Data Modeling:** To create relationships between player, team, and seasonal tables.

---

### 📈 Data & Insights

**Q: What specific stats can I analyze?** **A:** The dashboard covers three main pillars of NFL data:
* **Passing:** Yards, TDs, Interceptions, and Passer Rating.
* **Rushing/Receiving:** Volume stats (Attempts/Targets) vs. Efficiency (Yards per Carry/Catch).
* **Team Performance:** Scoring trends and offensive/defensive output.

**Q: Can I compare players side-by-side?** **A:** Yes! Using the built-in **Slicers**, you can filter for specific players or positions to see how they stack up against each other in real-time.

**Q: How is the "Efficiency" calculated?** **A:** We use custom DAX measures to calculate "true" performance metrics that go beyond box scores, such as **Yards per Attempt ($Y/A$)** and **Touchdown-to-Interception ratios**.

---

### ⚙️ Technical Setup

**Q: How do I refresh the data with the latest stats?** **A:** 1. Download the latest CSV/Excel data files.
2. Replace the files in the `/Data` folder of this repository.
3. Open the `.pbix` file in Power BI Desktop and click **Refresh**.

**Q: Can I use this for my own Fantasy Football league?** **A:** Absolutely. This tool is designed to help identify "sleeper" players by looking at volume metrics (targets and touches) that aren't always visible in standard league apps.

---

### 🚀 Getting Started

**Q: I see a "Data Source Error"—how do I fix it?** **A:** Because file paths change between computers, you may need to:
1. Go to **Transform Data** > **Data Source Settings**.
2. Click **Change Source**.
3. Point the file path to the location of the data files on your local machine.
