# 🏈 2023 NFL Player Performance Dashboard

An interactive Power BI dashboard that transforms raw 2023 NFL statistics into a decision-support tool for fantasy football analysis and player evaluation. Combines advanced DAX measures, dynamic quadrant analysis, and a dark-mode UI to surface player efficiency trends at a glance.

![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi)
![DAX](https://img.shields.io/badge/DAX-Custom%20Measures-yellow)
![Power Query](https://img.shields.io/badge/Power%20Query-M-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Overview

This project analyzes performance metrics for NFL players across four positions — QB, RB, WR, and TE — using the 2023 season dataset. The goal was to build a reusable analytics template that goes beyond standard box scores to identify efficiency trends and outlier performers.

---

## ✨ Features

- **Unified Yardage Metric** — Custom DAX measure combines passing and rushing yards to handle dual-threat players without double-counting
- **Dynamic Quadrant Analysis** — Scatter plots with average lines that recalculate automatically based on the selected position filter
- **Position Slicers** — Toggle between QB, RB, WR, and TE to instantly update all visuals and rankings
- **Dark Mode UI** — High-contrast interface with rounded visuals, clean KPI cards, and consistent color language
- **PDF Exports** — Pre-generated position-specific reports included in the repo

---

## 🗂️ Repository Contents

| File | Description |
|------|-------------|
| `2023_NFL_STATS_PROJECT.pbix` | Main Power BI dashboard file |
| `QB_Stats.pdf` | Exported quarterback analysis |
| `RB_Stats.pdf` | Exported running back analysis |
| `WR_Stats.pdf` | Exported wide receiver analysis |
| `TE_Stats.pdf` | Exported tight end analysis |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Data visualization and report building |
| **DAX** | Custom measures and KPI calculations |
| **Power Query (M)** | Data extraction, cleaning, and transformation |
| **Data Modeling** | Relationships between player, team, and seasonal tables |

---

## 🧠 Key DAX Measures

**Total Yards** — aggregates offensive output regardless of source, correctly handling dual-threat players:

```dax
Total Yards =
SUM('Stats'[passing_yards]) + SUM('Stats'[rushing_yards])
```

**Yards per Attempt (Y/A)** — efficiency metric beyond raw volume:

```dax
YPA =
DIVIDE(SUM('Stats'[passing_yards]), SUM('Stats'[pass_attempts]), 0)
```

---

## 📊 Analyses Covered

- **Passing:** Yards, TDs, interceptions, passer rating, Y/A
- **Rushing/Receiving:** Volume (attempts/targets) vs. efficiency (yards per carry/catch)
- **Team Performance:** Scoring trends, offensive and defensive output
- **Quadrant Analysis:** Elite vs. average separation by position
- **Fantasy Value:** Identifying sleeper candidates based on target share and touch volume

---

## 🚀 Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)

### Opening the Dashboard

1. Clone or download this repository
2. Open `2023_NFL_STATS_PROJECT.pbix` in Power BI Desktop
3. If prompted with a **Data Source Error**, go to:
   - **Transform Data** → **Data Source Settings** → **Change Source**
   - Point the path to the data files on your local machine

### Refreshing with New Data

1. Download updated CSV/Excel stats files
2. Replace the files in the data source location
3. Click **Refresh** in Power BI Desktop

---

## 📝 License

MIT — free to use, fork, and build on.

---

## 🤝 Contact

**Sky Moon** — [sky.moon7567@gmail.com](mailto:sky.moon7567@gmail.com) | [LinkedIn](https://linkedin.com/in/sky-moon/)
