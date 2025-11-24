# IT-Expenditure-Analysis

A comprehensive dashboard for analyzing Actual, Forecast, and Planned IT spend across regions, business areas, and cost categories.

📌 Project Overview
This project focuses on analyzing IT expenditure across Business Areas, Regions, Countries, IT Areas, and Cost Element Groups using Power BI.
The objective is to provide transparency into Actual vs Forecast vs Plan spending and identify overspend, underspend, and cost optimization opportunities.

🎯 Key Objectives
Understand how IT costs are distributed across:

Business Areas
Regions
IT Areas
Cost Element Groups
Analyze variance between:
Actual vs Plan
Forecast vs Plan

Identify:

Overspending regions/cost groups
Underutilized budgets
Cost drivers in IT operations
Enable stakeholders to make data-driven budgeting decisions.

🗂 Dataset Description
The Excel file contains two sheets:

1. Data (Historical Spend)
Date	Month (text form: Jan, Feb, etc.)
Business Area	IT business unit
Region	APAC / EMEA / AMERICAS
Country	Specific geography
IT Sub Area	Sub-categories
IT Area	Major IT domain
Cost Element Name	Detailed spend item
Cost Element Group	Category grouping
Cost Element Sub Group	Sub-category
Actual	Actual monthly cost
Forecast	Forecasted cost
Plan	Budgeted cost

2. Future Data
Same structure, except it contains only:
Actual (future estimate)

🔧 Data Preparation Steps

1. Import Dataset
Load Excel file into Power BI
Promote headers
Fix data types

2. Date Conversion
Month text (e.g., “Jan”) converted to numeric month
New date constructed:
NewDate = DATE(2024, MonthNumber, 1)
Sort MonthYear by NewDate

3. Cleaning & Formatting
Remove duplicates
Handle blanks in Actual/Forecast/Plan
Create hierarchies: Region → Business Area → IT Area → Cost Element

4. DAX Measures Created
Total Actual
Total Forecast
Total Plan
Variance (Actual – Plan)
Variance %
Overspend % (KPI)

📊 Dashboard Pages & Visuals
📍 Page 1: Executive Overview

Visuals:
Column Chart: Actual vs Forecast vs Plan by Month
KPI Card: Overspend % (highlights red if >0)
Treemap: Cost Element Group Contribution
Slicers: Date, Region, IT Area, Business Area

Insights:
Monthly spend pattern
Top-cost categories
Overall budget adherence
Quick filters for multi-dimensional analysis

🌍 Page 2: Regional Drilldown

Visuals:
Map Chart: IT Spend by Country
Bar Chart: Region-wise Variance
Matrix: Region → Business Area → Actual/Forecast/Plan

Insights:
Geographic cost hotspots
Region-level overspending
Business area breakdown by region

📦 Page 3: Cost Category Analysis

Visuals:
Bar Chart: Spend by Cost Element Group
Table: Top 10 overspending Cost Elements
Line/Area Chart: Forecast vs Plan vs Actual trends by IT Area

Insights:
Category-level cost drivers
High-risk cost elements
IT Area budget alignment

🔍 Exploratory Data Analysis (EDA)

Recommended visuals used:
Matrix for variance breakdown
Bar charts for Business Area distribution
Trend charts for time-series patterns

Key insights explored:
Which Business Areas spend the most
Regional distribution of IT costs
Cost Element Groups contributing max spend
Sub Areas causing overspend
Month-on-month variance

🛠 Tools & Technologies
Power BI Desktop
Power Query
DAX (Data Analysis Expressions)
Excel

✔ Outcome

The dashboard provides:
Clear financial visibility
Identification of overspend areas
Month-wise cost trends
Region and category drilldowns
Faster decision making for budget optimization
