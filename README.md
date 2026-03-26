# 📊 Inflation Forecasting in India: A Hybrid ML & Econometric Analysis

## 🚀 Project Overview

This project builds a **robust inflation forecasting system for India** using a combination of:

* Machine Learning (XGBoost)
* Deep Learning (LSTM)
* Time-Series Modeling (Prophet)
* Econometric Validation (Granger Causality)

Unlike typical forecasting projects, this work goes beyond prediction to answer a critical question:

> **Are macroeconomic variables truly driving inflation, or merely acting as predictive proxies?**

---

## 🎯 Problem Statement

Inflation forecasting is central to:

* Monetary policy decisions (RBI)
* Investment strategy
* Risk management in financial systems

Traditional models fail to capture:

* Non-linear dependencies
* External macroeconomic shocks
* Temporal dynamics

This project addresses these limitations using a **multi-model hybrid approach combined with causal validation techniques**.

---

## 📂 Dataset & Data Sources

* Indian CPI Inflation Data (2013–2025)

* Macroeconomic variables:

  * Brent Crude Oil Prices
  * USD/INR Exchange Rate
  * Rainfall & Temperature Anomalies
  * Repo Rate

* External data via APIs (e.g., NASA POWER)

---

## ⚙️ System Architecture

### 1. Data Engineering

* Time-index alignment across multiple sources
* Missing value handling
* Feature normalization

### 2. Feature Engineering (Critical Component)

* Lag features (t-1, t-2, t-6, t-12)
* Differencing for stationarity
* Rolling statistics
* ADF test for validation

> Key Insight: Inflation is strongly autoregressive — lagged features dominate predictive power.

---

## 🤖 Models Implemented

### 🔹 XGBoost (Primary Model)

* Handles structured macroeconomic data efficiently
* Captures non-linear interactions

### 🔹 LSTM

* Models sequential dependencies
* Effective for temporal pattern learning

### 🔹 Differenced LSTM

* Predicts Δ inflation instead of absolute values
* Improves stability and convergence

### 🔹 Prophet

* Baseline model capturing trend + seasonality

---

## 📊 Model Evaluation

Evaluation metrics:

* RMSE
* MAE

Comparison performed across:

* Food inflation
* Fuel inflation
* Miscellaneous sector

---

## 🔍 Interpretability & Causal Analysis (Core Contribution)

### 1. SHAP Analysis (Model Explainability)

SHAP values reveal:

* Lagged inflation variables are dominant predictors
* Brent crude, USD/INR, and rainfall anomalies contribute meaningfully
* Higher crude prices generally increase predicted inflation

---

### 2. Granger Causality Testing (Econometric Validation)

Contrary to initial expectations:

* Brent crude **does NOT Granger-cause food inflation**
* No statistically significant lagged causal relationship observed

---

## ⚠️ Key Insight: Correlation vs Causation

A critical finding of this project:

> **Brent crude is a strong predictive feature but not a causal driver of food inflation in this dataset**

Interpretation:

* ML models capture **predictive correlations**
* Econometric tests evaluate **temporal causality**
* Brent crude likely acts as a **proxy for broader macroeconomic conditions**

---

## 🧠 Economic Interpretation

The relationship between crude oil and food inflation is:

* **Indirect**, not direct
* Likely mediated via:

  * Transportation costs
  * Supply chain dynamics
  * Fuel price transmission

This highlights the importance of combining:

* Machine Learning
* Domain knowledge
* Statistical testing

---

## 📈 Key Results

| Insight       | Conclusion                               |
| ------------- | ---------------------------------------- |
| Lag features  | Strongest predictors                     |
| Brent crude   | Predictive, not causal                   |
| Hybrid models | More robust than single-model approaches |

---

## 🛠 Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* TensorFlow / Keras
* Prophet
* SHAP
* Statsmodels

---

## 🚧 Limitations

* No multivariate causal modeling (VAR not implemented)
* Limited macroeconomic feature space
* No real-time deployment

---

## 🔮 Future Work

* Vector Autoregression (VAR) for multivariate causality
* SHAP interaction effects
* Real-time forecasting dashboard (Streamlit)
* Integration with financial decision systems

---

## 💡 What Makes This Project Different

Most ML projects stop at prediction.

This project goes further by:

* Challenging model outputs using statistical tests
* Distinguishing correlation from causation
* Integrating ML with economic reasoning

---

## 📌 Conclusion

This project demonstrates that:

> **High predictive performance does not imply causal understanding**

By combining machine learning with econometric validation, it provides a more **reliable and interpretable framework for inflation forecasting**.

---

## 👨‍💻 Author

Shubhan Agrawal
B.Tech CSE | AI, Data Science & Finance Enthusiast

---
