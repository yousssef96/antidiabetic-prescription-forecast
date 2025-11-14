# Forecasting Antidiabetic Drug Prescriptions in Australia

## Project Overview
This project aims to **forecast monthly antidiabetic drug prescriptions in Australia** using time series modeling. Accurate forecasts support healthcare planning and resource allocation.  

The focus is on **SARIMAX modeling**, given the strong seasonality in the data, and comparing it with a baseline model to determine the best-performing approach.



## Objectives
1. Develop a forecasting model to predict monthly antidiabetic drug prescriptions.  
2. Apply a systematic modeling procedure using **SARIMAX**.  
3. Compare the model against a **baseline** (last season’s values).  
4. Identify the **champion model** based on performance metrics.



## Dataset
The dataset contains **monthly counts of antidiabetic drug prescriptions** in Australia.  
- **Time span:** [1991-2008]  
- **Frequency:** Monthly  
- **Variables:**  
  - `ds`: Month of prescription  
  - `y`: Number of prescriptions  

> *Note:* No exogenous variables were used in this analysis.



## Methodology

### 1. Exploratory Data Analysis
- Visualized the time series to observe trends and seasonality.  
- Performed **time series decomposition** to extract trend and seasonal components.  

### 2. Data Preparation
- Checked stationarity and applied transformations where necessary.  
- Split dataset: last **36 months used as a test set** for rolling forecasts.  

### 3. Model Building
- Applied **SARIMAX**, accounting for the strong seasonal patterns in the data.  
- Determined optimal `(p, d, q)(P, D, Q)_m` parameters.  
- Conducted residual analysis to validate the model.  

### 4. Forecasting and Evaluation
- Performed **rolling 12-month forecasts** on the test set.  
- Compared SARIMAX forecasts with a **baseline model** using last season’s values.  
- Metric: **Mean Absolute Percentage Error (MAPE)**  

| Model                 | MAPE       |
|-----------------------|------------|
| SARIMAX               | 7.90       |
| Last Season Baseline  | 12.69      |

**Conclusion:**  
The SARIMAX model outperforms the baseline, effectively capturing seasonal patterns and providing more accurate forecasts.



