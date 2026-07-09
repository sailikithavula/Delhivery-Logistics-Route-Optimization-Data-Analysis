# Delhivery Logistics & Route Optimization Analysis

An end-to-end data analytics and business intelligence project focused on optimizing supply chain operations, evaluating delivery performance, and calculating trip-level resource utilization for Delhivery.

---

## 📌 Project Overview
Logistics networks operate at a massive scale where minor inefficiencies in routing, vehicle allocation, or transit times cascade into heavy financial losses. 

This project tackles these challenges using a two-phased data strategy:
1. **Data Preprocessing & EDA (Python):** Cleaned, restructured, and engineered critical time-based and spatial features from raw, complex logistics logs.
2. **Business Intelligence (Power BI):** Constructed an interactive multi-dashboard system to monitor trip performance, evaluate regional delivery efficiencies, and audit logistics costs.

---

## 🛠️ Tech Stack & Tools
* **Data Processing & Analysis:** Python (Pandas, NumPy)
* **Data Visualization (Exploratory):** Matplotlib, Seaborn
* **Business Intelligence & Modeling:** Power BI, DAX (Data Analysis Expressions)
* **Environment:** Jupyter Notebook

---
## ⚙️ Project Steps

### 1. Data Processing & Feature Engineering (Python)
* Imported raw shipping transaction logs using `Pandas` to execute initial data shape verification (`df.info()`, `df.describe()`).
* Extracted localized feature components by breaking down trip creation timestamps into distinct attributes (hours, days, and months) to capture peak operational waves.
* Handled granular, segment-level data rows by aggregating them into unified trip-level summaries to resolve systemic row redundancy.
* Established an outlier mitigation strategy to isolate transit exceptions without warping baseline velocity metrics.

### 2. Business Intelligence & Data Modeling (Power BI)
* Ingested the polished Python output data structures into Power BI to construct a scalable data model.
* Engineered custom operational performance metrics using **DAX** equations to compute critical variables across distinct distribution loops.

### 3. Specialized Dashboard Architecture
Designed a targeted, multi-page business intelligence dashboard tailored for supply chain stakeholders:
* **Delivery Efficiency & Route Optimization Dashboard:** Compares performance variations across core logistics distribution types (**Carting** vs. **FTL**) and highlights gridlocks by cross-examining actual transit windows against **OSRM** algorithmic predictions.
* **Cost & Resource Utilization Dashboard:** Focuses on financial and asset auditing by calculating the **Average Cost Per Trip** and identifying lanes where fleet capacity is under-utilized.
* **Trip Performance & SLA Tracker:** Maps out geographic package volumes and visualizes delivery Service Level Agreement (SLA) breaches to isolate underperforming regional corridors.

---

## 📈 Power BI Dashboard
*(Tip: Take a screenshot of your dashboard, upload it to this repository, and link it below!)*
![Delhivery Dashboard](./Screenshot%202025-06-27%20224509.png)

---

## 💡 Key Results & Business Recommendations

* **The Warehouse Bottleneck:** Granular timestamp comparisons revealed that transit delays were rarely caused by slow driving or vehicle breakdown. Instead, structural bottlenecks were heavily concentrated within sorting hubs and Tier-3 center terminals during localized sorting waves.
* **Algorithmic Corridor Gaps:** Long-haul Carting corridors showed the highest discrepancy margins when measured against ideal OSRM trip benchmarks, indicating that route planning models need to actively adjust for specific infrastructure constraints on those lanes.
* **Fleet Capacity Optimization:** Full Truck Load (FTL) operations displayed stable and predictable margin structures. Conversely, local Carting loops frequently operated well below capacity. 
* **Strategic Recommendation:** Consolidate local Carting loops. It is recommended to group regional hub shipments onto shared runs to increase vehicle utilization rates, reduce empty miles, and minimize the overall average cost per trip.

---
