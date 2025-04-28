# OpenOrderReport

The **Revenue Overview** Power BI dashboard offers a clear summary of **Total Revenue** by **Month** and **Quarter**. Interactive bullet charts enable users to easily track revenue performance against defined targets, supporting better visibility and goal management.

![OpenOrderReport Screenshot](https://raw.githubusercontent.com/louisehealey/OpenOrderReport/main/OpenOrdeReport.png)

---

## ⏱️ Last Data Refresh

The report uses [worldtimeapi.org](https://worldtimeapi.org/api/timezone/America/New_York) to display the last time the dataset was refreshed when using **Import Mode**.

![Refresh Screenshot](https://raw.githubusercontent.com/louisehealey/OpenOrderReport/main/Refresh%20Pic.png)

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
