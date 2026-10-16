## 🚦 Smart City Traffic Analytics: Smart Mobility & Indian Road Safety Dashboard
_2 dataset analytics project that combines two real-world datasets, 20,000 Indian road accident records and 5,000 smart-mobility sensor readings, into a single interactive Excel dashboard. It covers raw data cleaning, data quality reports, KPI design, PivotTables, Pivot Charts and slicers, so city authorities can see road safety and traffic flow in one place._

---
## 📌 Table of Contents
- <a href="#overview">Project Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>
---
## 📌 Project Overview
- Road safety and traffic management are usually handled as separate silos inside a city administration. This project analyzes accident history (2022–2025) alongside high-frequency traffic sensor data (speed, occupancy, emissions, ride-sharing demand) to build a data-driven decision framework.

- Objective: Turn two raw datasets into a decision-ready, self-service dashboard that answers where and when accidents happen, how traffic flows, and what congestion costs in emissions and energy.

## ❓ Business Problem
- Accident side:- 20,000 accident records exist, but actionable patterns (riskiest cities, causes, times, road types) have not been extracted, so patrolling and safety policy stay reactive.

- Traffic sensor side:- Real-time IoT readings sit as raw data without analysis of how congestion and pollution change by hour or weather.

- Combined problem:- Operational traffic data and historical accident data are locked in separate silos, so a single risk-and-flow view for decision-making is not possible.

---

## 🗄️ Dataset
| Dataset	| Rows | Grain | Key fields |
|---|---|---|---|
|`Indian Roads Accident` | 20,000 |	One row per accident |	city, state, date/time, road type, lanes, traffic signal, weather, visibility, cause, severity, vehicles involved, casualties, peak-hour flag, festival, risk score |
| `Smart Mobility` | 5,000 | One reading every 5 minutes (1–9 March 2024) |	vehicle count, traffic speed, road occupancy, traffic light state, weather, accident report, sentiment score, ride-sharing demand, parking availability, emissions, energy consumption, traffic condition | 

**Coverage:** 8 cities (Mumbai, Delhi, Pune, Chennai, Kolkata, Bangalore, Hyderabad, Chandigarh), 7 states, **34,529 total casualties.** 

**Data cleaning steps:**

- Removed blank padding rows from the Smart Mobility sheet (only 5,000 rows held real data)
- Added derived columns (Year, Month, Day, Day Name, Day Type, Casualty Category, Risk Category)
- Produced data quality report workbooks: Missing Values, Duplicates, Data Types, Validation, Data Quality, Formula Documentation

---
# 🛠️ Tools & Technologies

 || Tool | Purpose || <br>
| **Microsoft Excel** |:- Data cleaning, KPI tables, PivotTables, Pivot Charts, Slicers, dashboard design |
| **Power Query** |:- Data import, cleaning and shaping (blank-row removal, type fixes) |<br>
| **Excel Formulas** |:- (`TRIM`), (`CLEAN`), (`PROPER`), (`IF/IFERROR/IFNA`), (`COUNTIF/COUNTIFS`), (`AVERAGE`), (`XLOOKUP`), (`INDEX-MATCH`) |

---

## 📂 Repository Structure

```
Smart-City-Traffic-Analytics/
├── 01_Business_Context/ 
|               └── Business Context, objectives, KPIs, stakeholders, business questions
├── 02_Dataset/
│   ├── 01_Raw_Data/                     # Smart_Mobility, Indian_Roads (original CSVs)
|   ├── 02_Processed_to Clean _Data/     # Smart_Mobility, Indian_Roads Cleaned.CSV
│   ├── 03_Data_Source/                  # README.docx
│   └── 04_Data_Dictionary/              # Smart-City-Traffic-Analytics Data Dictionary.docx
├── 03_Excel/
│   ├── 01_Raw_Excel/                    # indian_roads_dataset.xlsx , smart_mobility_dataset.xlsx
│   ├── 02_Clean_Excel_Data/             
|                └── 1_Smart_Mobility_Dataset , 2_Indian_Rode_Dataset   # Power Query cleaned workbooks
|   ├── 03_Pivot_Tables/                  # indian_Road_Dataset Pivot Table.xlsx , smart mobility dataset Pivot Table.xlsx
│   ├── 04_Excel_Dashboard/               # Smart City Analysis Final Dashboard.xlsx
│   ├── 05_Data_Cleaning_Notes/           # Indian_Roads_2_Dataset_Report.xlsx ,Smart_Mobility_2_Dataset_Report.xlsx
│   ├── 06_Pivot_Charts/                  # Indian Road Dataset Pivot Chart , Smart Mobility Dataset Pivot Chart.xlsx
├── 04_Presentation/                      # 1_Smart City Traffic Analytics – Interview-presentation.pptx
├── 05_Images/1_Dashboard_Screen_Short/   # Smart Mobility & Road Safety Analytics Dashboard.pptx
├── 06_Business_Probalm_Statement/        # Smart-City-Traffic-Analytics_Problam_Satemenr.docx
├── 07_README.md

```
---
## 🧮 Key KPIs

**Road Safety (Indian Roads dataset)**

- (`Total Accidents`), (`Total Casualties`), (`Total Fatal Accidents`) and (`Fatal Accident Rate`)
- (`Average Risk Score`)

**Traffic & Mobility (Smart Mobility dataset)**

- (`Total Vehicles`), (`Average Traffic Speed`), (`Average Road Occupancy`)
- (`Average Emission Level`) and (`Average Energy Consumption`) per congestion tier
---
## 📊 Dashboard Features

- **KPI cards** for both datasets (accidents, casualties, fatal rate, risk score, vehicles, speed, occupancy, emissions, energy)
- **12 Pivot  Charts** built on **12 PivotTables**:
  - *Traffic:* Traffic Volume by Hour, Average Speed by Traffic Condition, Traffic Condition Distribution, Emission & Energy by Condition, Occupancy & Speed during Accidents vs No Accidents, Road Occupancy by Traffic Light State
  - *Road Safety:* Accidents by City, Accidents by Cause, High-Risk City by Average Risk Score, Peak vs Non-Peak Accidents, Weather vs Severity, Visibility vs Severity
- **Slicers** with separate filter panels for the Mobility dataset and the Indian Roads dataset
- **Key Insights panel** summarizing the finding of every chart in plain language

---

## 🔍 Key Insights

**Traffic & Mobility**
1. Traffic Volume by Hour :- Peak traffic at Hour 19 (7 PM) with Average 171.13 vehicles. Lowest at Hour 9 with 142.85 vehicles. Overall Average = 153.92

2. Average Traffic Speed by Traffic Condition : - Low traffic has highest speed (59.9 km/h). High traffic has lowest speed (37.9 km/h). Overall Average Speed = 42.11 km/h

3. Traffic Condition Distribution : - High traffic condition is most common (63.32%). Medium = 29.50%, Low = 7.18%

4. Average Emission & Energy by Traffic Condition : - High congestion has highest Emissions (274.45). Energy Consumption is almost same across all conditions (17.2 - 17.5)

5. Occupancy & Speed during Accidents : - Very little difference in Occupancy and Speed between Accident and No-Accident cases. Both remain almost same (~54.5% Occupancy, ~42.1 km/h Speed)

6. Road Occupancy by Traffic Light State : - Green light has slightly higher Occupancy (55.12%). Red = 54.68%, Yellow = 54.46%. Overall difference is very small.

**Road Safety**
1. Accidents by City :- Chandigarh has the highest number of accidents

2. Accidents by Cause : - Distraction is the most common cause (4026). Over speeding is very close (4025). All causes are almost equally distributed

3. High Risk City by Average Risk Scroe :- Hyderabad has the highest Average Risk Score Among the analyzed Cities.

4. Peak Hours vs Non-Peak Accidents : - Peak Hours account for 24.74% of accidents. Non-Peak account for 75.26%

5. Weather vs Accident Severity : - Clear, Fog and Rain show almost identical severity pattern (Fatal ~15%, Major ~30%, Minor ~55%). Weather has no significant impact on severity

6. Visibility vs Accident Severity : - High, Low and Medium Visibility also show almost identical severity pattern. Visibility has no significant impact on severity

---

## 🎯 Skills Demonstrated

- Data cleaning and validation using Power Query and Excel formulas
- Data quality reporting (missing values, duplicates, data types, validation)
- Business-problem framing: problem statement, objectives, stakeholders, KPIs and business questions
- KPI design with `COUNTIF/COUNTIFS/AVERAGE`
- PivotTables, Pivot Charts and Slicers for self-service analytics
- Dashboard design and insight writing for non-technical stakeholders

---

## 💡 Recommendations

- Target patrols and enforcement at **evening peak hours (around 7 PM)** and at **distraction and overspeeding** cases.
- Since risk is spread evenly across cities, run **city-wide campaigns** rather than single-city drives.
- Use High-congestion windows to plan **signal-timing changes and emission-reduction measures**.

---

## 📎 Data Source

Traffic sensor and road accident datasets from public open-data sources (e.g. Kaggle, Data.gov.in).

---

## 👤 Author

**Shubham**
Aspiring Data Analyst | Python · SQL · Excel · Power BI
📍 Delhi, India






