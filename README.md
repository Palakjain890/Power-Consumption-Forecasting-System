# Power Consumption Forecasting - Tetouan City

This project aims to forecast hourly power consumption in Zone 1 of Tetouan City using statistical, machine learning, and deep learning models. The models were trained on weather-influenced energy data from the UCI Machine Learning Repository.

## 📊 Problem Statement

Accurately predicting electricity demand is crucial for efficient urban energy management. This project focuses on building forecasting models to predict hourly consumption patterns for January 2017, incorporating environmental factors such as temperature, humidity, wind speed, and solar radiation.

## 🗃️ Dataset

- Source: [UCI Machine Learning Repository - Tetouan Power Consumption Dataset](https://archive.ics.uci.edu/dataset/849/power+consumption+of+tetouan+city)
- Time period: Jan 1, 2017 – Dec 30, 2017 (10-min intervals)
- Features: Temperature, Humidity, Wind Speed, General Diffuse Flow, Power Consumption (Zones 1–3)

## 🔧 Preprocessing Steps

- Converted time format and removed missing values
- Resampled 10-min data to hourly frequency
- Created lag-based features and included exogenous weather variables
- Applied seasonal decomposition to detect trends and cycles

## 📈 Models Used

- **ARIMA, SARIMA, SARIMAX**
- **XGBoost**
- **Random Forest**
- **Deep Learning**: RNN, LSTM, GRU

## 🧪 Evaluation Metrics

- Root Mean Squared Error (RMSE)  
- Mean Absolute Percentage Error (MAPE)  
- R² Score

## ✅ Results

| Model         | RMSE   | MAPE   | R²     |
|---------------|--------|--------|--------|
| ARIMA         | 0.11   | 4.01%  | 0.9375 |
| SARIMA        | 0.12   | 4.57%  | 0.9199 |
| SARIMAX       | 0.11   | 5.26%  | 0.9354 |
| LSTM          | 0.1122 | 4.83%  | 0.9318 |
| GRU           | 0.11   | 4.19%  | 0.9400 |
| **XGBoost**   | 0.0873 | 3.79%  | 0.9568 |
| **Random Forest** | **0.0808** | **3.51%** | **0.9630** |

✅ **Best performance achieved using Random Forest Regression.**

## 📌 Key Takeaways

- Weather data (especially temperature) significantly impacts power consumption.
- Ensemble models (XGBoost, RF) performed better than classical and deep models.
- Time series cross-validation ensured robust generalization to unseen data.

## 🔮 Future Work

- Explore **transformer-based models** and **temporal convolutional networks (TCNs)** for capturing long-range dependencies.
- Integrate **calendar effects** (weekends, holidays) and **real-time sensors** for richer feature sets.
- Build **hybrid ensemble models** combining statistical and deep learning methods.
- Deploy the best-performing model into a **real-time dashboard** for smart energy monitoring.

## 📚 Guide

Project supervised by **Dr. Pritam Anand**  
Dhirubhai Ambani Institute of Information and Communication Technology
