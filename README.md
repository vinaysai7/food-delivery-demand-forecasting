🍔 Food Delivery Demand Forecasting

📌 Problem Statement

Food delivery platforms face large fluctuations in daily order volume due to factors like weekdays, weekends, promotions, and customer behavior.
Accurate demand forecasting is critical for delivery partner allocation, operational planning, and cost optimization.

This project focuses on predicting daily food delivery order volume using historical order data and machine learning techniques.

🎯 Objective

Forecast daily order volume using historical data

Capture temporal patterns such as weekly seasonality and recent demand trends

Compare machine learning models against a baseline forecast

Generate actionable insights for operational planning

📊 Dataset Overview

The dataset is sourced from a Zomato-style food delivery dataset and includes:

orders.csv – order-level transaction data

restaurants.csv – restaurant metadata

deliveries.csv – delivery-related operational data

Key attributes used:

Order date and status

Order value and discount information

Aggregated daily order counts

Raw data is transformed into a daily time-series forecasting table.

🧠 Approach
1. Data Preparation

Filtered only completed/delivered orders

Aggregated order-level data to daily granularity

Created a forecasting-ready dataset with one row per day

2. Feature Engineering

Calendar features: day of week, weekend flag, month

Lag features: previous day, previous week, and bi-weekly order volume

Rolling features: 7-day and 14-day rolling averages

3. Train–Test Split

Time-based split (80% train, 20% test)

Avoided random splitting to prevent data leakage

4. Models Trained

Baseline (previous day demand)

Linear Regression

Random Forest Regressor

5. Evaluation Metrics

MAPE (Mean Absolute Percentage Error)

RMSE (Root Mean Squared Error)

📈 Results

Machine learning models significantly outperformed the baseline forecast

Random Forest captured non-linear demand patterns effectively

Lag and rolling features were the strongest predictors of demand

Final model reduced MAPE by X% compared to the baseline forecasting approach.

🔍 Key Insights

Weekends consistently show higher order volume

Recent demand (last 7 days) strongly influences future demand

Promotional discounts lead to short-term demand spikes

These insights can help operations teams proactively plan delivery capacity.

🛠️ Tech Stack

Language: Python

Libraries: Pandas, NumPy, scikit-learn, Matplotlib

Modeling: Linear Regression, Random Forest

Evaluation: MAPE, RMSE
