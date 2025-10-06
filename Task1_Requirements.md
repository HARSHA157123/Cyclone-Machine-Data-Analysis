# 🌀 Task 1 Requirements – Cyclone Machine Data Analysis

This document outlines the detailed requirements, objectives, and deliverables for **Task 1** of the Data Science Internship Assessment — *Cyclone Machine Data Analysis (Time-Series)*.

The goal is to analyze three years of cyclone machine sensor data to identify shutdowns, detect operational states, discover anomalies, and forecast temperature trends using machine learning and statistical methods.

---

## 📘 Task 1.1 – Data Preparation & Exploratory Analysis

### Objective:
Prepare and explore the raw dataset to ensure high-quality, continuous, and reliable time-series data.

### Requirements:
- Load the 3-year dataset (~370,000 records at 5-minute intervals).
- Handle **missing values**, **timestamp gaps**, and **outliers**.
- Ensure a strict 5-minute time index with no gaps.
- Generate **summary statistics** (mean, std, percentiles).
- Create a **correlation matrix** to analyze relationships among variables.
- Visualize representative slices (e.g., 1 week and 1 year) to demonstrate normal machine behavior.

### Expected Output:
- Clean, structured dataset ready for analysis.
- Visual and statistical summaries showing data quality and consistency.

---

## ⚙️ Task 1.2 – Shutdown / Idle Period Detection

### Objective:
Automatically identify and quantify shutdown or idle periods in the cyclone machine’s operation.

### Requirements:
- Programmatically detect shutdown events using relevant features (e.g., temperature and pressure drop thresholds).
- Calculate **total downtime** and **number of shutdown events** across 3 years.
- Visualize a full-year timeline with shutdown periods highlighted.

### Expected Output:
- `shutdown_periods.csv` — start time, end time, and duration of each shutdown.
- A plot showing machine activity vs. shutdowns over time.

---

## 🧭 Task 1.3 – Machine State Segmentation (Clustering)

### Objective:
Segment active machine data into interpretable operational states using clustering techniques.

### Requirements:
- Exclude shutdown periods; retain only active operation data.
- Apply **multivariate clustering** (KMeans, DBSCAN, or HDBSCAN) on key features or engineered aggregates (lags, deltas, rolling stats).
- Identify and describe meaningful states (e.g., *Normal*, *High Load*, *Degraded*).
- Compute frequency and duration statistics per cluster.

### Expected Output:
- `clusters_summary.csv` — summary statistics for each cluster/state.
- Visualization of clustered states and their transitions.

---

## 🚨 Task 1.4 – Contextual Anomaly Detection & Root Cause Analysis

### Objective:
Detect and analyze anomalies within operational contexts (states) and provide possible causes.

### Requirements:
- Build state-aware anomaly detection models (e.g., cluster-specific **Isolation Forest** or **rolling MAD thresholds**).
- Identify anomaly periods with metadata (start, end, duration, affected variables).
- Select 3–6 significant anomalies and propose **root cause hypotheses** using timing and variable relationships.
- Visualize each anomaly with relevant context (time series + cluster labels).

### Expected Output:
- `anomalous_periods.csv` — anomalies with context and duration.
- Plots showing anomalies overlaid on cluster/state data.
- Written analysis of causes for each selected anomaly.

---

## 🔮 Task 1.5 – Short-Horizon Forecasting

### Objective:
Predict short-term trends of key operational variables for proactive maintenance insights.

### Requirements:
- Forecast `Cyclone_Inlet_Gas_Temp` for the next **1 hour (12 steps)**.
- Compare multiple methods — baseline persistence vs. statistical/ML models (ARIMA, Prophet, RandomForest, or LSTM).
- Evaluate performance using **RMSE** and **MAE** metrics.
- Discuss performance differences and practical forecasting challenges (shutdowns, regime changes).

### Expected Output:
- `forecasts.csv` — true vs. predicted values.
- Forecasting plots comparing model performance.
- Written evaluation and discussion.

---

## 💡 Task 1.6 – Insights & Storytelling

### Objective:
Synthesize all analyses into key operational insights and recommendations.

### Requirements:
- Summarize how shutdowns, clusters, anomalies, and forecasts interrelate.
- Identify data-driven operational patterns (e.g., states prone to anomalies or preceding shutdowns).
- Present **3–5 concise insights** connecting analysis results to actionable recommendations.

### Expected Output:
- A short report section or slide summarizing insights and actionable findings.
- Visuals supporting insights (e.g., correlation between cluster anomalies and shutdowns).

---

## 📦 Deliverables

| File Name | Description |
|------------|-------------|
| **task1_analysis(final).ipynb** | Main notebook implementing all six tasks end-to-end |
| **data.csv** | Original dataset (3-year time series) |
| **shutdown_periods.csv** | Detected shutdowns (start, end, duration) |
| **clusters_summary.csv** | Summary statistics for each operational state |
| **anomalous_periods.csv** | List of detected anomalies with context |
| **forecasts.csv** | Forecasted vs actual inlet gas temperatures |
| **plots/** | Folder with all visualization outputs (shutdowns, clusters, anomalies, forecasts) |
| **README.md** | Project overview and setup instructions |
| **Task1_Requirements.md** | This document describing objectives and deliverables |

---

## 📧 Contact

**Author:** Harsha  
**Email:** harsha157123@gmail.com  
**Year:** 2025  

---

## 📜 License

This project is released under the **MIT License**.
