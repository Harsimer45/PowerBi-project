# PowerBi-project
# ICC Cricket World Cup 2023 Dashboard 📊🏏

This project presents an **interactive Power BI dashboard** built to analyze the ICC Cricket World Cup 2023 using data visualization and DAX (Data Analysis Expressions). It was completed as part of my **Summer Training** at **TCIL-IT Chandigarh** during **June–July 2025**.

## 🔍 Overview

The primary goal was to convert raw match data into an insightful, dynamic dashboard without using Python or SQL—relying purely on Power BI’s built-in tools. The dashboard offers real-time filtering and analytics for:

- Team performance
- Player statistics
- Match outcomes
- Points and Net Run Rate (NRR)

## 📂 Datasets Used

Three CSV files were used from Kaggle:

1. **matches.csv** – General match details (venue, teams, winner, umpires, etc.)
2. **deliveries.csv** – Ball-by-ball match data (batsman, bowler, runs, wickets)
3. **points_table.csv** – Team standings (matches played, wins, losses, points, NRR)

## 🔧 Data Modeling

- Relationships were created between the three datasets using `match_number` and team names.
- `Power Query Editor` was used for data cleaning and transformation.
- Data types were verified, null values handled, and invalid entries removed.
- One-to-many relationships connected `matches` with `deliveries` using `match_number`.

## 🧮 DAX Measures Created

Custom DAX measures were developed to derive important statistics. Examples include:

- `Total Runs` = `SUM(deliveries[runs_off_bat])`
- `Total Wickets` = COUNT of non-`run out` `wicket_type`
- Measures for each score type: Ones, Twos, Threes, Fours, Sixes
- Dismissal types: LBW, Bowled, Caught, Stumped, etc.
- `Tournament Winner` using a `VAR` + `CALCULATE` formula on the last match

## 🖥️ Dashboard Overview

### 📄 **Page 1: Tournament Overview**
- **KPI Cards**: Winner, Total Runs, Total Matches, Total Wickets
- **Map Visual**: Stadium locations
- **Donut Chart**: Total Sixes vs Fours
- **Tables**: Top 5 Run Scorers, Top 5 Wicket Takers

### 📄 **Page 2: Team Radar**
- **Slicers**: Team and Venue selectors
- **Bar Charts**: Top 3 Run Scorers & Wicket Takers per team
- **Cards**: Runs and Wickets at selected venue
- **Donut Charts**: Run and Wicket Distribution
- **Line Chart**: Net Run Rate (positive = green, negative = red)

## 💡 Observations & Learning Outcomes

- Learned how to model, transform, and visualize large sports datasets
- Built KPIs and visuals entirely using Power BI and DAX
- Gained hands-on experience in ETL processes, filtering, and interactive reporting
- Developed skills relevant to BI, data analytics, and dashboard design

## 📌 Project Highlights

✅ 100% No-Code Approach  
✅ Real-Time Filtering & Slicer Interactions  
✅ Visual Storytelling with Clear Layouts  
✅ Covers Group Stage, Semi-Finals, and Final Matches  





---

> 🔗 Note: Dashboard visuals available in `.pbix` format and screenshots in the `/screenshots` folder (add accordingly).
