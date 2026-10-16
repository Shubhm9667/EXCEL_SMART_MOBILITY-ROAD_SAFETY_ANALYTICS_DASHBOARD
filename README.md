## 🚦 Smart City Traffic Analytics: Smart Mobility & Indian Road Safety Dashboard
_2 dataset analytics project that combines two real-world datasets, 20,000 Indian road accident records and 5,000 smart-mobility sensor readings, into a single interactive Excel dashboard. It covers raw data cleaning, data quality reports, KPI design, PivotTables, Pivot Charts and slicers, so city authorities can see road safety and traffic flow in one place._

---
## 📌 Table of Contents
- <a href="#overview">Overview</a>
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

