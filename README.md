# OutagesUSA_1
PysPark experimental around USA outages in 2023 using ML

# ⚡ US Power Outages Analysis with PySpark — 2023

A data analysis and machine learning project using **PySpark MLlib** on the public **EAGLE-I** dataset (Oak Ridge National Laboratory), containing **77,341 records** of power outages across the United States in 2023.

---

## 🎯 Objectives

- Explore outage patterns by state, event type, and time of day
- **Classify the event type** (Severe Weather, Vandalism, etc.) using a Random Forest model
- **Predict outage duration** in hours using Linear Regression
- Visualize findings with Matplotlib charts inline in the notebook

---

## 📂 Repository Structure

```
OutagesUSA_1/
├── data/
│   └── eaglei_outages_with_events_2023.csv   ← dataset (77k rows)
├── OutagesUSA_1.ipynb.ipynb                  ← main notebook (Google Colab)
├── .gitignore
└── README.md
```

---

## 📊 About the Dataset

| Column | Description |
|---|---|
| `event_id` | Unique event identifier |
| `state` | US state |
| `county` | County name |
| `Event Type` | Category: Severe Weather, Vandalism, etc. |
| `start_time` | Outage start time |
| `duration` | Duration in hours |
| `min_customers` | Minimum number of customers affected |
| `max_customers` | Maximum number of customers affected |
| `mean_customers` | Average number of customers affected |

**Source:** [EAGLE-I — Oak Ridge National Laboratory](https://www.ornl.gov/)

---

## 📈 Expected Results

| Model | Metric | Expected Value |
|---|---|---|
| Random Forest | Accuracy | ~75–85% |
| Random Forest | F1-Score | ~0.75 |
| Linear Regression | RMSE | ~8–15 h |
| Linear Regression | R² | ~0.15–0.35 |

> The low R² in the regression model is expected — outage duration depends heavily on external factors not present in the dataset (local infrastructure, crew response time, equipment age).

---

## 🧰 Technologies

- [PySpark 3.5](https://spark.apache.org/docs/3.5.0/) — distributed data processing
- PySpark MLlib — machine learning pipelines
- Matplotlib — data visualization
- Google Colab — cloud execution environment
- Google Drive — dataset storage

---

## 📄 License

MIT — free to use and modify.

---

*Study project — public data from EAGLE-I / Oak Ridge National Laboratory*
