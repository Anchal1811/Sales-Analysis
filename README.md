# Sales Analysis: End-to-End BI Pipeline

An end-to-end data analytics project focused on transforming raw, unformatted corporate sales data into a structured relational schema to extract actionable business insights. The pipeline utilizes **Excel** for initial data inspection, **Python (Pandas)** for automated data cleaning, **SQL (MySQL)** for data storage and structural validation, and **Power BI** for interactive business intelligence reporting.

## 📊 Project Visual
Below is a preview of the interactive dashboard developed in Power BI, connected to the cleaned dataset:

![Sales Dashboard](sales.png)

---

## 🛠️ Tech Stack & Workflow

1. **Data Ingestion & Inspection (Excel):** Evaluated the raw dataset (`sales_raw_500.xlsx`) containing 520 records to map out missing entries, syntax inconsistencies, and duplicate transactional records.
2. **Data Cleaning & Transformation (Python/Pandas):** Implemented automated cleaning rules via a Jupyter Notebook (`Sales Analysis.ipynb`). This stage filtered out incomplete fields, cast appropriate data types, and exported a clean baseline (`sales_cleaned.csv`), trimming down the final dataset to **482 validated records**.
3. **Database Relational Setup (SQL):** Imported the structured dataset into a MySQL database to ensure data integrity and query-readiness for business reporting.
4. **Data Modeling & Visualization (Power BI):** Developed an interactive dashboard (`sales.pbix`) utilizing specialized DAX metrics to track profitability, revenue streams, and regional distribution.

---

## 📉 Data Quality & Pipeline Summary

* **Raw Data Input:** 520 rows of untrusted entries.
* **Processed Dataset:** 482 entries successfully validated after removing anomalies, null fields, and redundant rows.
* **Pipeline Goal:** Establishing a repeatable data flow that standardizes raw tabular inputs into reliable reporting metrics.

---

## 🚀 Quick Business Insights

Based on the validated 482 records and the calculated dashboard measures, the analysis reveals the following insights:

* **Regional Revenue Breakdown:** Sales distribution is segmented across four key regions—**East, West, North, and South**. The visuals allow stakeholders to trace exactly which geographical territory handles the highest concentration of transaction volumes.
* **Profitability Margin Analysis:** Utilizing custom DAX calculations, specifically the **`% of Profit on Sales`** metric, the reporting engine explicitly separates total revenue from actual net profitability. This identifies high-margin vs. high-volume product categories, pinpointing where operational costs may be eroding profit lines.
* **Product Concentration:** Distinct visual trends highlight which product subsets act as the primary cash drivers versus those suffering from sluggish turnover rates, enabling tighter inventory control and targeted regional marketing.

---

## 📂 File Architecture

* `sales_raw_500.xlsx`: The source unstructured spreadsheet data.
* `Sales Analysis.ipynb`: The Pandas-driven cleaning scripts handling data prep and normalization.
* `sales_cleaned.csv`: Output baseline utilized for relational database mapping.
* `sales.pbix`: Power BI workbook containing data models, DAX measures, and visual canvases.
* `sales.png`: Static snapshot of the final reporting dashboard.

---

## 🔧 Setup & Installation

1. **Data Processing:** Open and run `Sales Analysis.ipynb` in a Jupyter environment to verify data processing steps.
2. **Database Schema:** Import `sales_cleaned.csv` into your preferred SQL environment (e.g., MySQL workbench).
3. **Dashboard Reporting:** Open `sales.pbix` in Power BI Desktop to inspect the calculations, underlying data schema, and interactive charts.
