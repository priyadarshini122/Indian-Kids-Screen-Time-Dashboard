# 📱 Indian Kids Screen Time Dashboard

An interactive Power BI dashboard that analyzes and visualizes screen time trends among Indian children. This project aims to provide data-driven insights into how kids in India are spending time on digital devices, categorized by device usage, time slots, location, and parental controls.

## 📊 Project Overview

This dashboard helps understand:
- How much time kids are spending on screens daily and weekly
- Device preferences (Mobile, Tablet, Laptop, TV)
- Most used time slots (Morning, Noon, Evening, Night)
- Screen time usage by age group and gender
- Parental control adoption and screen time limits
- Regional differences in screen usage

## 🔧 Tools Used

- **Power BI** – for data modeling, DAX calculations, and interactive dashboard creation
- **Excel / CSV** – as the primary data source
- **DAX** – for calculated measures and KPIs

## 📈 Key Features

- 📌 **Overview Page**: Summary KPIs like average screen time, parental control usage, and total kids surveyed.
- 📅 **Time Usage Analysis**: Hourly screen time distribution across different days.
- 🧑‍👧 **Demographic Insights**: Age-wise and gender-wise comparison of screen usage.
- 📍 **Location-based View**: State-wise or region-wise differences in screen behavior.
- ⏳ **Exceeded Limit Tracker**: Identifies how many children exceed the healthy screen time limit (Min = 0, Max = 1 hr/day).
- ✅ **Parental Control Effectiveness**: Visual correlation between screen time and parental control settings.

## 🧮 DAX Measures Used

```DAX
Total Screen Time = SUM(ScreenTime[HoursSpent])
Average Screen Time = AVERAGE(ScreenTime[HoursSpent])
Exceeded Limit = IF([Total Screen Time] > 1, "Yes", "No")
Parental Control Usage % = DIVIDE(CALCULATE(COUNTROWS(ScreenTime), ScreenTime[ParentalControl] = "Yes"), COUNTROWS(ScreenTime))
