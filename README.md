# HR Attrition & Workforce Analytics Dashboard

Interactive Excel dashboard analyzing employee attrition (IBM HR dataset) - uncovers key drivers like age, tenure, overtime & job role using Pivot Tables, slicers & GETPIVOTDATA.

### Dashboard Preview
![HR Attrition Dashboard](https://github.com/aakriti80043-create/IBM-HR-Attrition-and-Workforce-Analytics-Dashboard/blob/main/Hr%20Dashboard.png)

**Tool:** Microsoft Excel (Pivot Tables, Pivot Charts, Slicers, GETPIVOTDATA, Conditional Formatting)
**Dataset:** [IBM HR Analytics Employee Attrition Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) (Kaggle) — 1,470 employee records

---

## Problem Statement

Employee attrition costs organizations significant time and money in recruiting, onboarding, and lost productivity. This dashboard analyzes IBM's HR dataset to identify **which employee segments are at highest risk of leaving**, so HR can prioritize retention efforts where they matter most.

---

## Key Findings

- **Overall attrition rate: 16.12%** (237 of 1,470 employees)
- **Age is the strongest demographic driver** — employees aged 18-25 leave at **35.77%**, nearly 3x the rate of employees aged 36-45 (9.19%)
- **Early tenure is the riskiest period** — attrition drops sharply from **29.82%** in years 0-2 to **8.13%** after 10 years
- **Overtime nearly triples attrition risk** — 30.53% attrition among employees working overtime vs. 10.44% among those who don't
- **Sales Representative is the highest-risk role** at **39.76%** attrition — more than double the company average
- **Single employees make up 50.6% of all departures**, despite being a smaller share of the workforce, suggesting marital status/life-stage may correlate with job mobility

---

## Dashboard Features

- **4 real-time KPI cards** — Total Employees, Attrition Rate, Average Tenure, Average Monthly Income
- **7 interactive visualizations**, each chart type deliberately chosen based on what the data represents:
  - Bar charts for department and job-role comparisons
  - Line charts for ordered trends (age band, tenure band)
  - A bar-with-baseline chart for overtime risk (instead of a misleading pie of independent rates)
  - A 100% stacked bar for "share of departures by marital status" (a true part-to-whole relationship)
- **4 linked slicers** (Department, Job Role, Overtime, Gender) connected across all pivot tables for fully interactive, cross-filtered exploration
- **Color-coded High-Risk Roles table** flagging the top job roles needing retention focus (High/Medium/Low risk tiers via conditional formatting)

---

## Approach

1. Cleaned the raw dataset — removed constant/non-informative columns (`EmployeeCount`, `Over18`, `StandardHours`)
2. Engineered helper fields (`Age Band`, `Tenure Band`) using nested `IF()` formulas for grouped analysis
3. Built multiple Pivot Tables to calculate attrition rate by Department, Overtime, Age Band, Tenure Band, Job Role, and Marital Status
4. Used `GETPIVOTDATA()` to pull pivot values into dedicated helper tables, decoupling charts from pivot refreshes/filters
5. Selected chart types based on what each metric actually represents (independent rates vs. true proportions of a whole), rather than defaulting to generic bar/pie charts
6. Connected slicers to all pivot tables via Report Connections for synchronized, dashboard-wide filtering

---

## Business Recommendation

Retention efforts should prioritize **early-career, early-tenure Sales employees working overtime** — this segment shows compounding risk across every major driver identified in the analysis.

---

## Author

**Aakriti Sharma**
🔗 [LinkedIn](https://linkedin.com/in/aakriti-sharma-37593a294)
💻 [GitHub](https://github.com/aakriti80043-create)
