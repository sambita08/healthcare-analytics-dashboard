# 🏥 Healthcare Operations & Clinical Anomaly Dashboard

An interactive **Power BI** dashboard that analyzes hospital operations, revenue cycle performance, and clinical anomalies across **54,860 patients (2019-2024)**. It helps operations, finance, and clinical teams spot cost outliers, plan staffing, and reduce bed-occupancy bottlenecks.

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Dashboard Preview](#-dashboard-preview)
- [Key Metrics](#-key-metrics)
- [Key Insights](#-key-insights)
- [Business Recommendations](#-business-recommendations)
- [Dataset](#-dataset)
- [Tools & Techniques](#-tools--techniques)
- [Repository Structure](#-repository-structure)
- [How to Use](#-how-to-use)
- [Author](#-author)

---

## 🎯 Overview

Hospitals face rising costs, long stays, and unpredictable demand. This project answers three questions:

1. **Operations:** How many patients are admitted, through which channels, and how long do they stay?
2. **Revenue Cycle:** Where are daily costs and billing concentrated, and for which patient groups?
3. **Clinical Anomalies:** Which patients are cost or length-of-stay outliers, and what drives their risk?

The report has two pages:

| Page | Purpose |
|------|---------|
| **Healthcare Operations and Revenue Cycle Analytics** | Volume, length of stay, daily cost, revenue, and bed occupancy |
| **Clinical Outcomes and Anomaly Tracking** | Flagged anomalies, high-risk patient register, and ML risk drivers |

---

## 🖼️ Dashboard Preview

### Page 1: Healthcare Operations and Revenue Cycle Analytics
![Operations and Revenue Dashboard](images/operations-revenue.png)

### Page 2: Clinical Outcomes and Anomaly Tracking
![Clinical Outcomes and Anomaly Dashboard](images/clinical-anomalies.png)

---

## 📊 Key Metrics

### Operations & Revenue
| Metric | Value |
|--------|-------|
| Total Patients | **54,860** |
| Avg Length of Stay | **15 days** |
| Avg Daily Cost | **$3,399** |
| Total Revenue | **$1,404M** |
| Emergency Share | **33%** |

### Clinical Anomalies
| Metric | Value |
|--------|-------|
| Anomaly Rate | **17%** |
| Total Flagged Anomalies | **9,177** |
| Emergency Share | **33%** |
| Long LOS Share of Anomalies | **40%** |

---

## 🔍 Key Insights

### Operations & Revenue Cycle
- **Pediatric cost spikes:** Extreme daily cost spikes occur in child (pediatric) acute care, while middle-aged and senior patients show stable, uniform daily costs across all six medical conditions.
- **Steady demand:** Admissions hold at roughly **850-1,000 patients per quarter** across Elective, Emergency, and Urgent channels from 2019 Q3 to 2024 Q1, which supports predictable baseline staffing.
- **Peak volumes:** Urgent admissions peaked in **2019 Q3 (~1,010 cases)** and Emergency admissions in **2020 Q3 (~990 cases)**.
- **Bed occupancy bottlenecks:** Despite an average stay of about 15.5 days, **Emergency Cancer (16.0 days)** and **Urgent Asthma (15.8 days)** admissions create the heaviest bed pressure.

### Clinical Anomalies & Risk
- **High Daily Cost dominates:** High Daily Cost outliers make up **59.8%** of flagged anomalies, versus **40.2%** for Long LOS outliers.
- **Not isolated to one specialty:** Anomalies are spread evenly across all six conditions (~1,480-1,560 cases each, led by Diabetes and Arthritis), so the cost problem is hospital-wide.
- **Anomaly split:** Of ~55K patients, **83.27% are Normal**, **10%** are High Daily Cost, and **6.73%** are Long LOS.
- **Length of Stay is the top risk driver:** The Key Influencers analysis identifies Length_of_Stay as the primary predictor of risk status (**2.20x** increase in likelihood) and of daily cost (**R² = 0.679**).
- **High-risk segments:** The Top Segments view surfaces six patient groups, with anomaly rates from **19.3%** (largest segment, 3,704 patients) up to **89.5%** (smallest, 636 patients).

---

## 💡 Business Recommendations

1. **Use expected stay at admission** to produce accurate cost estimates and flag high-risk patients early.
2. **Streamline insurance prior-authorizations** for patients predicted to have long stays.
3. **Plan Day-1 discharge, home-health, and step-down transfers** for Emergency Cancer and Urgent Asthma admissions to speed up bed turnover.
4. **Review short-stay, high-intensity care** (especially pediatric) to find the source of financial leakage.
5. **Keep baseline staffing steady**, since admission volume is stable and predictable.

---

## 🗂️ Dataset

- **Source:** `[ADD DATASET SOURCE / LINK, e.g. Kaggle dataset name]`
- **Size:** ~55K patient records (54,860 after cleaning)
- **Period:** 2019-2024
- **Main fields:** Age, Medical Condition, Admission Type, Insurance Provider, Billing Amount, Date of Admission, Discharge Date, Test Results

**Calculated fields:** Length_of_Stay, Daily_Cost (Billing Amount ÷ Length_of_Stay), Age Group (Child / Adult / Middle-Aged / Senior), Anomaly Status (High Daily Cost / Long LOS / Normal)

---

## 🛠️ Tools & Techniques

- **Power BI Desktop** for the report and visuals
- **Power Query** for data cleaning and transformation
- **DAX** for measures and calculated columns
- **Key Influencers visual** (AI/ML) for risk driver and segment analysis
- **Slicers and filters** for Year/Quarter/Month, Insurance Provider, Admission Type, Medical Condition, Age Group, Test Results, and Anomaly Status
- **Visuals:** KPI cards, line chart, clustered column chart, matrix heatmap, donut chart, bar chart, and table

---

## 📁 Repository Structure

```
healthcare-operations-anomaly-dashboard/
├── README.md
├── LICENSE
├── .gitignore
├── dashboard/
│   └── Healthcare_Dashboard.pbix
├── data/
│   └── healthcare_dataset.csv
└── images/
    ├── operations-revenue.png
    └── clinical-anomalies.png
```

---

## ▶️ How to Use

1. Download `Healthcare_Dashboard.pbix` from the `dashboard` folder.
2. Open it in **Power BI Desktop** (free from Microsoft).
3. If prompted, point the data source to the CSV in the `data` folder.
4. Use the slicers to explore by year, insurance provider, admission type, condition, and age group.

---

## 👤 Author

**[YOUR NAME]**
🔗 [LinkedIn](YOUR_LINKEDIN_URL) | 📧 YOUR_EMAIL

⭐ If you found this project useful, please give it a star!
