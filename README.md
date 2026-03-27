# 🔧 Predictive Maintenance using RUL Prediction

## 📌 Overview

This project builds an end-to-end Predictive Maintenance system to estimate the Remaining Useful Life (RUL) of industrial machines using machine learning. By leveraging historical sensor data, the model predicts how long a machine can operate before failure, enabling proactive maintenance and reduced downtime.

## 🚀 Key Features
* Predicts Remaining Useful Life (RUL) using multivariate time-series sensor data
* Implements advanced feature engineering (rolling stats, lag features, domain-based stress features)
* Uses XGBoost for high-performance prediction
* Prevents data leakage via machine-based train-test split
* Converts predictions into actionable Risk Bands for business decision-making

## 🗂️ Dataset
* ~120,000 records with 25 features
* Includes:
  * Machine ID, timestamps
  * Operational settings (machine type, shift)
  * Sensor readings (temperature, vibration, pressure, voltage, RPM)


## ⚙️ Tech Stack
* Python (Pandas, NumPy)
* Scikit-learn (Pipelines, preprocessing)
* XGBoost (modeling)
* Matplotlib / Seaborn (visualization)

## 🧠 Methodology
* Data Preprocessing
* Missing value imputation (median/mode)
* Encoding categorical variables
* Feature Engineering
* Time-series: rolling mean, rolling std, lag features
* Domain features: thermal, mechanical, electrical stress
* Model Building
* Ridge Regression (baseline)
* Random Forest
* XGBoost (final model)
* Evaluation Metric: RMSE
* Focus on minimizing large prediction errors

## 📊 Results
* XGBoost achieved best performance with lowest RMSE
* High recall for critical failures, ensuring safety
* Slight overprediction bias to prevent unexpected breakdowns


## 📉 Business Impact
* Enables predictive maintenance instead of reactive repairs
* Reduces downtime and maintenance costs
* Helps in better resource planning and scheduling

## Risk Band Classification
* RUL Range	Risk Level
* 0–85	Critical
* 85–150	High
* 150–280	Medium
* >280	Safe

## ⚠️ Challenges Addressed
* Data leakage → solved via machine-based splitting
* Noisy sensor data → handled using rolling features
* Complex degradation → captured using domain knowledge

## 🔮 Future Improvements
* Implement LSTM/RNN models for sequence learning
* Deploy model on real-time IoT/edge devices
* Enhance generalization across different machine types
