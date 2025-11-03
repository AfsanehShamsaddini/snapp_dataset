
# Lyft Ride Analysis & Prediction

## Project Overview

This project analyzes and models Lyft ride data in Tehran. It includes **data cleaning, feature engineering, exploratory data analysis (EDA), visualizations, and predictive modeling**. The goal is to understand ride patterns and predict key metrics, including daily trip counts and service types.

**Note:** The original data is from the **Uber and Lyft Dataset, Boston, MA**. Lyft rides were extracted and transformed to simulate ride data for Tehran, so this dataset is **synthetic and not real**.

---

## 📂 Repository Structure

| Notebook               | Description                                                                                                                                                             |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Data Cleaning.ipynb`  | Loads raw data, removes irrelevant columns, maps Lyft service types, handles datetime, and creates synthetic Tehran-based dataset.                                      |
| `Visualization.ipynb`  | Explores the dataset through plots, charts, heatmaps, and examines distributions, skewness, and outliers.                                                               |
| `Model Building.ipynb` | Builds predictive models for: <br> 1) Regression → `route_day_count` <br> 2) Classification (Multiclass) → `service_type` <br> 3) Classification (Binary) → `peak_hour` |

---

## 📂 Dataset

The cleaned dataset is available as:
`snapp_data_clean.csv`

Key features include:

* **source:** Pickup district (District1 to District22)
* **destination:** Drop-off location (`Poonak Azad University`)
* **datetime:** Timestamp of the ride
* **service_type:** Ride type (`Sharing`, `Eco`, `Eco Plus`)
* **hour/day/month/weekday/part_of_day:** Derived time features
* **peak_hour:** Binary feature indicating rush hours
* **route:** Source → Destination path
* **route_day_count:** Daily number of trips per route
* **mean_hour_by_source:** Average pickup hour per source
* **service_type_day_count:** Daily trip count per service type
* **service_type_weekday_count:** Weekly trip count per service type

---

## 🔍 Features & EDA

* Distribution of rides by district, service type, part of day, hour, day, month, and weekday.
* Top 10 busiest routes.
* Correlation heatmaps and outlier/skewness detection.

---

## 🤖 Predictive Modeling

Three predictive tasks:

1. **Regression:** Predict `route_day_count`

   * Model: `RandomForestRegressor`
   * Metrics: MAE, RMSE, R²

2. **Classification (Multiclass):** Predict `service_type`

   * Model: `RandomForestClassifier`
   * Metrics: Accuracy, F1-score, Classification Report

---

## ⚙️ Preprocessing

* Numerical columns: Median imputation, scaling with StandardScaler.
* Categorical columns: Mode imputation, one-hot encoding.
* Pipelines used for reproducible preprocessing and modeling.

---

## 🔧 How to Run

1. Clone the repository:

```bash
git clone <your-repo-url>
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open and run notebooks:

```bash
jupyter notebook
```

* Run `Data Cleaning.ipynb` → generate cleaned dataset
* Run `Visualization.ipynb` → explore dataset
* Run `Model Building.ipynb` → train and evaluate models

---

## Author

**Afsaneh Shamsaddini**


