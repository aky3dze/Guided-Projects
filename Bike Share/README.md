# Toman Bike Share


- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Data Source and Overview](#data-source-and-overview)
- [Tools and concepts applied](#tools-and-concepts-applied)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Data visualization](#data-visualization)
- [Findings](#findings)
- [Conclusions and Recommendations](#conclusions-and-recommendations)

## Project Overview 
This project analyses 


## Objectives
- Identify key factors influencing ...
- Provide actionable insights to help ...
- [insert pic of email]
![bike email 2](https://github.com/user-attachments/assets/fbe74b2f-f7c3-4f6e-a4bd-3ee3dc83a35f)



## Data Source and Overview
This data was obtained [Github](https://github.com/Gaelim/YT_bike_share/blob/main/cost_table.csv). The dataset includes attributes such as . 


## Tools and concepts applied
- **Power BI** - for data analysis, visualization and dashboard creation
	- Concepts applied:
   	 1. Measures
   	 2. Calculated columns
   	 
## Exploratory Data Analysis
use common table expressions

**1.**
````sql
with cte_bike as (
select * from bike_share_yr_0
union all
select * from [dbo].[bike_share_yr_1])


select dteday, season, cte_bike.yr, mnth, hr, weekday, rider_type, riders, price, COGS, riders*price as revenue, 
riders*price - COGS*riders as profit 
from cte_bike
left join cost_table 
on cte_bike.yr = cost_table.yr
````	    

## Data Cleaning and Preparation
Data was efficiently cleaned and transformed with the PowerQuery editor in Power BI. Some of the applied steps include:
- Making first rows as headers
- Adding conditional columns to
   - assign labels to numeric responses such as job satisfaction, work-life balance, etc.
   - define age and salary brackets
   - assign numeric values to the YES and NO responses of attrition.
- Crosschecking datatypes and changing them when there is a need


## Data visualization
The Power BI dashboard provides an interactive interface, allowing for filtering based on year.
![bike](https://github.com/user-attachments/assets/e36ac378-984a-46a4-93d7-e1284aae5168)

## Findings

## Conclusions and Recommendations
