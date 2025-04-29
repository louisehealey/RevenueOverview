# Revenue Overview Report

The **Revenue Overview** Power BI dashboard offers a clear summary of **Total Revenue** by **Month** and **Quarter**. Interactive bullet charts enable users to easily track revenue performance against defined targets, supporting better visibility and goal management.

<p align="center">
  <img src="https://raw.githubusercontent.com/louisehealey/RevenueOverview/main/RevenueTracker.png" width="600"/>
</p>
---

## 🔄 Dynamic Dashboard Title

The DashboardTitle measure generates a dynamic report title based on the selected year. It extracts the maximum date currently filtered in the report, retrieves its year and appends it to the static text label "Revenue Overview". This allows the report title to automatically update to reflect the year being analyzed, providing clear and context-sensitive labeling for the report.
 ``` 
DashboardTitle =
VAR SEL_YEAR= YEAR(MAX('Revenue Table'[FirstOfTheMonth]))
RETURN
"Revenue Overview" & ": " & SEL_YEAR
 ``` 

<p align="center">
  <img src="https://raw.githubusercontent.com/louisehealey/RevenueOverview/main/DashboardTitle.gif" width="600"/>
</p>
---


---
