# 🌍 Nairobi Air Quality Analysis and ARIMA Modeling

This project explores Nairobi's air quality over time and builds a forecasting model using ARIMA. It follows a full machine learning workflow, from **data preparation** to **model evaluation** and **forecasting**.

---

## 📌 Project Objectives

- **Analyze** air quality trends in Nairobi using real-world data.
- **Build and evaluate** an ARIMA time series model to predict future pollution levels.
- **Leverage MongoDB** for efficient data storage and retrieval.
- **Communicate insights** through visualizations and metrics.

---

## 📂 Workflow Overview

### 1️⃣ Data Preparation
✅ Import clean time-series data from **MongoDB**  
✅ Handle missing values and ensure proper **datetime indexing**

### 2️⃣ Exploratory Data Analysis (EDA)
✅ **Trend and seasonality analysis** using moving averages  
✅ **Correlation heatmaps** and **distribution plots**  


### 3️⃣ Modeling (ARIMA)
✅ Perform **stationarity tests** and transformations  
✅ Fit **AutoRegressive Integrated Moving Average (ARIMA)** model  
✅ Evaluate performance using **RMSE and AIC**  


### 4️⃣ Forecasting & Communication
✅ Generate future predictions  
✅ Compare predicted vs actual values  

---

## 🛠️ Technologies Used

- `Python`
- `Pandas`, `NumPy`
- `Matplotlib`, `Seaborn`, `Plotly`
- `Statsmodels`, `Scikit-learn`
- `PyMongo` for database connectivity
- `Jupyter Notebook`

---

## 📈 Model Performance

- The ARIMA model effectively captures time-series patterns.
- Model evaluation metrics:
  - **RMSE:** *X.XX* (replace with actual value)
  - **AIC Score:** *X.XX*
- The model produces reliable forecasts with well-defined confidence intervals.
 

---

### 📌 How to Run the Notebook

1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/airquality-arima.git
   cd airquality-arima
