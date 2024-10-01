# Electricity Demand and Price Prediction

## Goal:

This project focuses on forecasting time series data by merging two distinct datasets: energy consumption and weather data. Utilizing data from several cities in Spain, it addresses the challenge of predicting future energy demand and pricing based on multivariate time series analysis.

A variety of forecasting models are employed, including XGBoost Regressor, GRU (Gated Recurrent Unit), LSTM (Long Short-Term Memory), CNN (Convolutional Neural Network), CNN-LSTM, and LSTM-Attention. Additionally, hybrid models such as GRU-XGBoost and LSTM-Attention-XGBoost are implemented, leveraging the strengths of multiple techniques in ensemble forecasting.

The aim is to improve the accuracy of electricity demand and price forecasts, contributing to the development of energy forecasting systems and providing valuable insights for decision-making in the energy sector.

## Dataset Overview:

The data is a combination of energy consumption and weather information from various Spanish cities, forming a multivariate time series forecasting problem. The energy dataset includes data on electricity generation from different sources like fossil fuels, wind, and coal. The weather dataset covers metrics such as temperature, humidity, pressure, wind speed, and more.

The dataset contains four years of weather data, accessible from the [OpenWeather API](https://openweathermap.org/api), along with electricity consumption, pricing, and generation data for Spain from the [ENTSO-E portal](https://transparency.entsoe.eu/dashboard/show). Pricing data was sourced from the [Spanish TSO Red Electric España](https://www.esios.ree.es/en/market-and-prices?date=27-03-2023#).

## Methodology:

The project is divided into four key stages:

1. **Data Loading and Exploration**: Using `os` and `pandas`, data is loaded and processed into a DataFrame. A correlation matrix is plotted to explore relationships between features.
2. **Preprocessing**: This involves handling missing values, extracting features like hour, weekday, month, and year, visualizing the data, normalizing and reshaping it, and performing the Dickey-Fuller test to check stationarity.
3. **Model Development and Training**: PCA is used for feature selection, target variables are normalized, and models including XGBoost, GRU, LSTM, CNN, CNN-LSTM, LSTM-Attention, GRU-XGBoost, and LSTM-Attention-XGBoost are built for forecasting.
4. **Model Evaluation**: The Mean Absolute Error (MAE) is calculated for both training and validation sets. The performance of all models is compared and analyzed at the end.

## Requirements

To run this project, you'll need to install the following libraries:

- `matplotlib`
- `numpy`
- `pandas`
- `math`
- `seaborn`
- `xgboost`
- `tensorflow`
- `keras`
- `scikit-learn`
