# RUL Prediction using CMAPSS Dataset (FD004)

This repository contains a complete pipeline for Remaining Useful Life (RUL) prediction of jet engines using the CMAPSS FD004 dataset. The project compares multiple regression models including Random Forest, Linear Regression, XGBoost, and LSTM to predict the RUL of engines based on time-series sensor data.

---

## 📁 Dataset

The data used in this project is from the [NASA CMAPSS dataset](https://www.nasa.gov/content/prognostics-center-of-excellence-data-set-repository). Specifically, the `FD004` sub-dataset, which simulates high operating conditions and a larger number of sensors (21 sensors).

### Files Used:
- `train_FD004.txt`: Training data
- `test_FD004.txt`: Test data
- `RUL_FD004.txt`: Actual RUL values for the test set

---

## ⚙️ Workflow Overview

1. **Data Preprocessing**  
   - Assign column names
   - Add RUL to training data
   - Normalize sensor values using MinMaxScaler

2. **Visualization**  
   - Sensor values vs. RUL
   - Sensor histograms
   - Sensor time-series for a single engine

3. **Feature Engineering**  
   - Select all 21 sensor columns as features

4. **Modeling**
   - `RandomForestRegressor`
   - `LinearRegression`
   - `XGBoostRegressor`
   - `LSTM (Keras Sequential)`

5. **Sequence Generation**  
   - Create fixed-length sequences for the LSTM model

6. **Evaluation**
   - Metrics: MAE, RMSE
   - Visual comparisons: line plots and scatter plots of true vs predicted RUL

---

## 📊 Model Comparison

| Model              | MAE   | RMSE  |
|-------------------|-------|-------|
| Random Forest      | ~     | ~     |
| Linear Regression  | ~     | ~     |
| XGBoost            | ~     | ~     |
| LSTM               | ~     | ~     |

(*Exact values shown in output*)

---

## 📦 Dependencies

Install required packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost tensorflow
