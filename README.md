
# 💊 Pharmacy Fulfillment & Patient Experience Dashboard

This Power BI dashboard provides a comprehensive view of pharmacy performance, patient satisfaction, and prescription fulfillment efficiency — modeled after real operational insights from CVS Health.

---

## 📌 Overview

This dashboard analyzes pharmacy data to highlight how effectively prescriptions are being fulfilled, how long customers wait, and how they feel about their experience. It’s ideal for showcasing healthcare analytics, Power BI visualization, and patient-centric metrics in your portfolio.

---

## 📊 Key Features

| Section                         | Description                                                       |
|----------------------------------|-------------------------------------------------------------------|
| **KPI Cards**                   | Total prescriptions, % on-time fulfillment, avg. wait time, rating |
| **Trends Over Time**            | Daily/monthly trend of prescriptions filled                       |
| **Fulfillment Efficiency**      | Comparison of wait time by fulfillment type (in-store vs delivery) |
| **Regional Analysis**           | Prescription counts by location                                   |
| **Customer Sentiment**          | Word cloud from review text, rating distribution, donut visual     |

---

## 📁 Dataset

**File:** `CVS_Pharmacy_Analytics_Sample.xlsx`  
**Fields:**
- `Prescription_ID`
- `Date_Filled`
- `Pharmacy_ID`, `Location`
- `Fulfillment_Type`
- `Wait_Time_Minutes`, `Was_On_Time`
- `Customer_Review`, `Rating`

---

## 📐 DAX Measures Used

```DAX
-- % of prescriptions filled on time
OnTimeRate = 
DIVIDE(
    COUNTROWS(FILTER(Sheet1, Sheet1[Was_On_Time] = "Yes")),
    COUNTROWS(Sheet1)
)

-- (Optional) Dynamic Title
DashboardTitle = 
"CVS Pharmacy Performance - Updated " & FORMAT(TODAY(), "MMM DD, YYYY")
```

---

## 🎯 Insights Enabled

- Identify delivery bottlenecks or wait time issues
- Compare performance across locations
- Analyze sentiment from real reviews
- Spot trends in fulfillment performance

---

## 💡 Tools Used

- Power BI Desktop  
- DAX for custom KPIs  
- Word Cloud (custom visual)  
- Excel for data simulation

---

## 🚀 How to Use

1. Download `CVS_Pharmacy_Analytics_Sample.xlsx`
2. Open Power BI Desktop → Get Data → Excel
3. Load Sheet1 and create visuals as outlined
4. Customize slicers, titles, and themes
5. Export to PDF, PowerPoint, or publish via Power BI Service

---

## 📄 License

MIT License — feel free to use or modify for portfolio, internal use, or learning.

---

## 🙋 Contact

Built by Shruti Devani — inspired by CVS Health analytics experience.  

