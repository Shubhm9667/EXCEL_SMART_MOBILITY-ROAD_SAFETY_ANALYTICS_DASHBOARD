# Smart City Traffic Analytics

## Business Context

Smart cities face growing challenges in managing urban traffic due to rapid population growth, increasing vehicle density, and limited road infrastructure. Inefficient traffic flow leads to longer commute times, higher fuel consumption, increased air pollution, and reduced quality of life for citizens. Municipal authorities and transportation departments need data-driven insights to optimize signal timings, identify congestion hotspots, and plan better infrastructure investments.

This project analyzes historical traffic data to uncover patterns in vehicle volume, peak hours, accident-prone zones, and the impact of weather or events on traffic conditions. By transforming raw data into actionable intelligence, city planners can make informed decisions that improve mobility, reduce emissions, and enhance public safety.

## Problem Statement

Urban traffic management systems currently rely on limited real-time monitoring and lack comprehensive historical analysis, resulting in reactive rather than proactive decision-making. There is a clear need for an end-to-end analytics solution that consolidates traffic data, identifies key patterns and bottlenecks, and delivers interactive dashboards with actionable recommendations for city authorities.

## Objectives

- Clean and prepare multi-source traffic data for analysis
- Identify peak congestion hours, high-traffic corridors, and accident hotspots
- Analyze the relationship between traffic volume, weather, and time of day
- Build interactive Power BI dashboards for real-time monitoring and historical trends
- Provide data-driven recommendations to improve traffic flow and reduce congestion
- Establish a scalable analytics workflow from raw data to business insights

## Tools Used

- **Excel** – Initial data exploration, cleaning, and basic calculations
- **SQL** – Data querying, joins, aggregations, and database management
- **Python** – Advanced data cleaning, feature engineering, statistical analysis, and visualization
- **Power BI** – Interactive dashboards, KPIs, and business reporting

## Dataset Information

| Attribute       | Details                          |
|-----------------|----------------------------------|
| **Source**      | Municipal Traffic Sensors + Open Traffic Data Portals |
| **Rows**        | ~1.2 million records             |
| **Columns**     | 18 key attributes                |
| **Time Period** | January 2023 – December 2025     |

**Key Columns include:** Timestamp, Location ID, Vehicle Count, Average Speed, Congestion Level, Weather Condition, Incident Type, Road Type, etc.

## Project Workflow

```
Business Problem
       ↓
     Excel
       ↓
      SQL
       ↓
    Python
       ↓
   Power BI
       ↓
   Insights
       ↓
Recommendations
```

## Dashboard Preview

![Dashboard Preview](images/dashboard-preview.png)

> *Note: Place your actual Power BI dashboard screenshot in the `images/` folder and update the path if needed.*

## Key Insights

1. **Peak Congestion Hours**: Traffic volume peaks between 8–10 AM and 5–8 PM on weekdays, with average speeds dropping by 40–55% during these windows.
2. **Hotspot Identification**: Three major corridors account for nearly 35% of total daily congestion events.
3. **Weekend vs Weekday Patterns**: Weekend traffic is more evenly distributed but shows higher average speeds and fewer incidents.
4. **Weather Impact**: Rainy days increase average travel time by 22% and raise the probability of minor incidents.
5. **Accident Correlation**: Locations with frequent stop-and-go traffic show 2.8× higher accident rates compared to free-flow segments.
6. **Signal Efficiency**: Certain intersections experience prolonged red-light cycles that contribute to upstream queuing.
7. **Vehicle Composition**: Heavy vehicles contribute disproportionately to congestion during mid-day hours on arterial roads.
8. **Seasonal Trends**: Summer months show higher overall volume, while monsoon periods exhibit the sharpest drops in average speed.
9. **Underutilized Routes**: Alternative parallel routes remain underused during peak hours, indicating potential for better route guidance.
10. **Incident Response Lag**: Average time from incident detection to clearance exceeds optimal benchmarks in several zones.

## Recommendations

1. **Dynamic Signal Timing**: Implement adaptive traffic signal control systems at the top 5 congestion hotspots to reduce average wait times.
2. **Real-time Route Guidance**: Integrate live congestion data with public navigation apps and digital signage to divert traffic to underutilized routes.
3. **Targeted Infrastructure Upgrades**: Prioritize capacity improvements or dedicated lanes on the three highest-impact corridors.
4. **Weather-Responsive Protocols**: Activate specialized traffic management plans during adverse weather conditions.
5. **Incident Management Enhancement**: Reduce detection-to-clearance time through better sensor coverage and coordinated response teams.
6. **Public Awareness Campaigns**: Promote off-peak travel and carpooling during identified high-congestion windows.
7. **Data-Driven Policy**: Use the analytics dashboard for continuous monitoring and quarterly review of traffic performance KPIs.

## Future Scope

- **Machine Learning**: Develop predictive models for congestion forecasting and incident risk scoring.
- **Automation**: Schedule automated data pipelines and daily/weekly dashboard refreshes.
- **API Integration**: Connect live traffic sensor feeds and weather APIs for near real-time analytics.
- **Mobile Dashboard**: Create a mobile-friendly version of the Power BI report for field teams and decision-makers.
- **Geospatial Analysis**: Incorporate GIS layers for deeper spatial insights and heatmaps.
- **What-if Simulation**: Build scenario modeling tools to evaluate the impact of proposed infrastructure changes.
