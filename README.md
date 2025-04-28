# Revenue Overview Report

The **Revenue Overview** Power BI dashboard offers a clear summary of **Total Revenue** by **Month** and **Quarter**. Interactive bullet charts enable users to easily track revenue performance against defined targets, supporting better visibility and goal management.

<p align="center">
  <img src="https://raw.githubusercontent.com/louisehealey/RevenueOverview/main/RevenueTracker.png" width="600"/>
</p>
---

## 🔄 Dynamic Dashboard Title

As the user selects the desired year, the title of the report updates accordingly. 



---

## 🔘 Late Button
This calculated column identifies Purchase Orders with delivery dates **prior to today**, helping teams track and manage **overdue deliveries** more effectively.

 ``` 
LATE = 
IF(TODAY()>PurchaseOrders[Rev Delivery Date], "Y","N")

 ``` 
---

## 🔘 In-Bound Button
This calculated column flags Purchase Orders with delivery dates within the next **7 days**, helping teams prioritize and manage **upcoming deliveries** effectively
 ``` 
IN_BOUND = 
IF(
    PurchaseOrders[Rev Delivery Date] >= TODAY() && PurchaseOrders[Rev Delivery Date] <= TODAY() + 7,
    "Y",
    "N"
)
 ``` 
---

## 🖥️ Power BI Demo

Explore the interactive **Open Purchase Orders** report in action:

![OpenOrderGIF](https://github.com/louisehealey/OpenOrderReport/blob/main/OpenOrderGIF)

---
