# Revenue Overview Report

The **Revenue Overview** Power BI dashboard offers a clear summary of **Total Revenue** by **Month** and **Quarter**. Interactive bullet charts enable users to easily track revenue performance against defined targets, supporting better visibility and goal management.
 
``` 
RevenuePerformanceMeasure =
VAR TR = SUM('Revenue Table'[Revenue])
VAR GR = SUM('Revenue Table'[Goal])
RETURN 
  IF(GR > 0, TR / GR, BLANK())
 ``` 
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

## 📂 Quarter and Month Tabs

Using buttons and custom bookmarks, the report is organized into separate tabs, allowing for easier navigation between different time views—such as quarterly and monthly data.
<p align="center">
  <img src="https://raw.githubusercontent.com/louisehealey/RevenueOverview/main/RevenueTrackerTabChange.gif" width="600"/>
</p>

## ℹ️ Tool Tips
Using both the default and custom tooltips provides more context to the report. In addition to the default tooltips (**Total Revenue %** and **Total Goal %**), exact figures for the **Total Revenue in Dollars** (`Total Revenue ($$)`) and the **Total Goal in Dollars** (`Total Goal ($$)`) are also included. These custom tooltips offer additional data points without overcrowding the visual, making the report easy and fast to digest.

<p align="center">
  <img src="https://raw.githubusercontent.com/louisehealey/RevenueOverview/main/RevenueTrackerToolTip.gif" width="600"/>
</p>
