
# 🚕 Taxi Demand Forecasting (Time Series)
# Temporal-series-Sweet-Lift-Taxi
Time series forecasting project to predict hourly taxi demand at airports using historical order data. The project includes data resampling, exploratory analysis, feature engineering (lags and rolling means), and regression models evaluated with RMSE to support operational decision-making.


## 📌 Project Overview
This project focuses on forecasting the **hourly number of taxi orders at airports** using historical data provided by **Sweet Lift Taxi**.  
Accurate demand prediction helps optimize driver availability during peak hours and improves operational efficiency.

The task was developed as part of a **Time Series Analysis sprint**, following a structured data science workflow.

---

## 🎯 Objective
Build a predictive model that estimates the number of taxi orders for the **next hour**, achieving a **Root Mean Squared Error (RMSE) ≤ 48** on the test dataset.

---

## 📂 Dataset
- **Source:** `/datasets/taxi.csv`
- **Target variable:** `num_orders`
- **Frequency:** Raw data resampled to **1-hour intervals**

---

## 🧪 Project Structure

The project follows four main stages:

### 1️⃣ Data Preparation
- Converted datetime column to `datetime64`
- Set datetime as index
- Resampled data to hourly intervals
- Checked data consistency and missing values

### 2️⃣ Exploratory Data Analysis
- Analyzed overall demand trends
- Identified hourly and weekly seasonality
- Visualized demand patterns over time

### 3️⃣ Feature Engineering & Model Training
- Created calendar features:
  - year, month, day, hour, day of week
- Generated lag features and rolling means
- Split data into:
  - **Training set:** 90%
  - **Test set:** 10%
- Trained multiple models:
  - Linear Regression
  - Random Forest Regressor

### 4️⃣ Evaluation & Results
- Evaluated models using **RMSE**
- Selected the best-performing model
- Achieved RMSE below the required threshold

---

## 📊 Results
- The final model successfully captures short-term demand patterns.
- Hour-based features and recent demand (lags) were the most influential.
- The model meets the project requirement of **RMSE ≤ 48**.

---

## 🛠️ Tools & Libraries
- Python
- pandas, numpy
- scikit-learn
- matplotlib

---

## ✅ Conclusion
The developed model provides reliable hourly demand forecasts and can be used to support real-time operational decisions, such as allocating taxi drivers more efficiently during high-demand periods.

Future improvements could include:
- Gradient boosting models (XGBoost, LightGBM)
- Longer seasonal feature windows
- Automated retraining pipelines
