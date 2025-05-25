# Credit-Card-Transaction-Volume-Forecasting-Anomaly-Detection.


📌 Overview

#1. Data Preprocessing

Dataset: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Loaded data, checked for missing values (none found).

Converted time to datetime format.

Aggregated data hourly:

total_txns: Count of transactions.

total_amount: Sum of transaction amounts.

fraud_count: Sum of frauds (Class).

2. Exploratory Data Analysis (EDA)
   
Line plots for total_txns and total_amount.

Time series decomposition attempted (limited insight due to short duration).

Moving averages (3h, 6h) used to smooth trends.

3. Forecasting Models
   
Prophet: Forecasted values without train-test split (short dataset).

ARIMA: Performed stationarity tests, used auto-ARIMA for short-term prediction.

4. Anomaly Detection

Compared predicted vs. actual values.

Flagged anomalies where residual > 2 × standard deviation.
