# 🌀 Cyclone Machine Data Analysis (Task 1)

Time-series analysis of 3 years of cyclone machine sensor data to detect shutdowns, segment operational states, identify anomalies, and forecast short-term temperature trends.  
This project demonstrates a full end-to-end industrial data science workflow using Python.

---

## 📂 Repository Structure

```
.
├── task1_analysis(final).ipynb    # Main analysis notebook
├── data.csv                       # Raw input dataset
├── outputs/                        # Generated outputs
│   ├── shutdown_periods.csv
│   ├── clusters_summary.csv
│   ├── anomalous_periods.csv
│   └── forecasts.csv
├── plots/                          # Visualization outputs
│   ├── shutdowns_plot.png
│   ├── clusters_overview.png
│   ├── anomalies_visuals.png
│   └── forecasts_plot.png
└── README.md                       # This file
```

---

## 🎯 Objective

- Detect and quantify **shutdown / idle periods**  
- Segment machine behavior into distinct **operational states**  
- Perform **contextual anomaly detection** within states  
- Forecast short-term trends for `Cyclone_Inlet_Gas_Temp`  
- Derive actionable **insights** on operations and potential failures

---

## 🔍 Methodology Highlights

| Stage | Approach |
|-------|----------|
| Data Preparation | Handle missing timestamps, outliers; enforce uniform 5-min intervals |
| Shutdown Detection | Identify idle periods via thresholds, generate event statistics |
| Clustering | Use KMeans / DBSCAN to segment active data into states |
| Anomaly Detection | Apply Isolation Forest / MAD within each cluster |
| Forecasting | Build and compare ARIMA, Prophet, and baseline models |
| Insight Analysis | Correlate anomalies, state transitions, and shutdowns |

---

## 📈 Key Insights (Sample)

- Short shutdowns often precede or follow unstable load states  
- “High Load” state shows higher anomaly density  
- Certain temperature deviations precede shutdowns — possible early warning signals  
- Prophet model handles non-stationary seasonal patterns better in this dataset

---

## 🧰 Technologies & Libraries

- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn, statsmodels, prophet, matplotlib, seaborn  

---

## 🚀 How to Run (Locally)

1. **Clone this repository:**
   ```bash
   git clone https://github.com/HARSHA157123/Cyclone-Machine-Data-Analysis.git
   cd Cyclone-Machine-Data-Analysis
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the Jupyter Notebook:**
   ```bash
   jupyter notebook task1_analysis(final).ipynb
   ```

4. The notebook automatically reads `data.csv` and produces output files under `outputs/` and visualizations under `plots/`.

---

## 📄 Deliverables

| File | Description |
|------|--------------|
| `shutdown_periods.csv` | Timestamps & durations of shutdown events |
| `clusters_summary.csv` | Statistical summary of each operational state |
| `anomalous_periods.csv` | Detected anomalies with metadata |
| `forecasts.csv` | Forecasted vs actual temperature values |
| `plots/` | Visualizations for shutdowns, clusters, anomalies, and forecasts |

---

## 🛠️ Future Improvements

- Deploy real-time monitoring with alert generation  
- Implement advanced clustering (HDBSCAN, PCA-based reduction)  
- Extend to multivariate forecasting (LSTM / VAR models)  
- Integrate visualization dashboards (Streamlit or Grafana)

---

## 📧 Contact

**Author:** Harsha  
**Email:** harsha157123@gmail.com  
**Year:** 2025  

---

## 📜 License

This project is released under the **MIT License**.
