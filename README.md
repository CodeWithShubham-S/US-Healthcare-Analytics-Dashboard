# 🏥 US Healthcare Analytics & Price Optimization Dashboard

[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://products.office.com/excel)
[![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)](https://sheets.google.com)
[![Data Analytics](https://img.shields.io/badge/Domain-Healthcare_Analytics-blue?style=for-the-badge)](#)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)](#)

An end-to-end healthcare data analytics and financial optimization project analyzing **9,999 patient records** from US hospitals over a 5-year period. This project features dynamic executive dashboards, pricing optimization matrices, clinical resource allocation models, and demographic distribution insights.

---

## 📌 Executive Summary

* **Total Patient Volume:** 9,999 patients
* **Total Healthcare Billing:** $233.30 Million ($232,975,908 validated billing)
* **Average Billing per Patient:** $23,379.40
* **Average Length of Stay (ALOS):** 13.8 Days (Overall Inpatient Mean)
* **Time Span:** 2018 – 2023

---

## 📸 Dashboard & Analysis Previews

### 1. Executive Management Dashboard
> High-level KPI scorecards, medical condition billing bar charts, admission distribution donut chart, and insurance revenue column charts.
![Executive Dashboard](screenshots/Executive_dashboard.png)

### 2. Price Optimization Matrix
> Cross-tabulated multi-variable analysis showing average billing across age cohorts and condition categories.
![Price Optimization Matrix](screenshots/price_Optimization.png)

### 3. Demographic & Clinical Breakdown
> Patient segmentation by gender, chronic condition burden, and age cohorts.
![Demographic Analysis](screenshots/demographics.png)

### 4. Hospital Resource Management
> Spot trends in how/when patients are admitted to better use hospital resources (staff, rooms).
![Hospital Resource Management](screenshots/Hospital_Management.png)
---

## 🔍 Key Business & Clinical Insights

### 1. Oncology & Diabetes Drive Disproportionate Costs
* **Cancer** represents the single highest financial burden, accounting for **$65.19 Million** (28.0% of total hospital billing) across **1,647 patients**, with an average cost of **$39,688.33** per patient. Average cancer billing peaks in the **Young Adult (18–30)** cohort at **$42,132.60**.
* **Diabetes** incurs the second highest average billing at **$30,102.74** per patient ($42.93M total), while also requiring the longest inpatient duration at **14.16 days**.
* **Obesity** accounts for the lowest per-patient average cost at **$12,511.82**.

### 2. Admission Type Dynamics & Inpatient Stays
* **Emergency Admissions** lead total traffic at **35.9% (3,587 patients)**, contributing **$86.91 Million** in revenue with an average stay of **14.03 days**.
* **Urgent Admissions** represent **33.4% (3,335 patients)** with **$75.65 Million** in billings.
* **Elective Admissions** account for **30.8% (3,077 patients)** with the shortest stay (**9.96 days**), demonstrating high operational turnaround efficiency.

### 3. Payer Mix & Demographic Burden
* **Medicare** is the largest insurance payer, covering **24.3% of all patients (2,428)** and generating **$55.56 Million** in billing.
* Private insurers (**Cigna**, **Aetna**, **Blue Cross**, and **UnitedHealthcare**) distribute remaining patient coverage evenly (~18%–19% each).
* **Senior Citizens (61–85)** constitute the largest patient demographic (**36.6%**, 3,660 patients) and incur the highest aggregate medical condition burden, with **Hypertension** being the most prevalent diagnosis (**21.6% overall**; heavily male-skewed).

---

## 🛠️ Data Architecture & Methodology

1. **Data Cleaning & Auditing:**
   * Handled character replacement errors (OCR/digit-letter swaps such as 'O' vs. '0') in raw billing records.
   * Standardized text casing and categories across medical conditions and diagnostic test outcomes.
   * Addressed serial date formatting and reconciled unbounded formula ranges.

2. **Formulas & Analytical Modeling:**
   * Dynamic matrix calculations using `=AVERAGEIFS()`, `=COUNTIFS()`, and `=SUMIFS()`.
   * Standardized percentage formatting (`0.0%`) to eliminate floating-point and integer rounding mismatches.
   * Dynamic bounded range indexing to link summary tables directly with chart visualizations.

3. **Data Visualization:**
   * Built visual hierarchy matching 16:9 / 13–15" display guidelines.
   * Clean scorecards for top-level KPIs.
   * Multi-series column, bar, and donut charts aligned to spreadsheet grid borders.

---

## 📂 Repository Structure

```text
US-Healthcare-Analytics-Dashboard/
│
├── data/
│   └── Healthcare_Data.csv              # Cleaned dataset (9,999 records)
│
├── screenshots/
│   ├── dashboard_overview.png           # Executive Dashboard screenshot
│   ├── price_optimization.png           # Price optimization matrix & charts
│   └── demographic_analysis.png         # Demographic & clinical analysis
│
├── INSIGHTS_OF_US_HEALTHCARE.xlsx       # Interactive Excel workbook with all sheets
├── README.md                            # Comprehensive project documentation
└── LICENSE                              # MIT License
