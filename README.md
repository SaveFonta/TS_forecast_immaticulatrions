# TS_forecast_immatriculations

This repository contains the script for the "Forecasting Competition" at the University of Bologna (Unibo). The objective of the competition is to forecast the number of car registrations in Italy for March 2024. The time series data for car registrations is available up to February 2024 in the file `auto.xlsx`.

## Overview

In this project, several models were tested to minimize the Mean Absolute Percentage Error (MAPE) and Mean Squared Error (MSE) after decomposing the time series data in two different ways. The implemented models include:

- Canonical Exponential Smoothing
- Holt-Winters Exponential Smoothing
- SARIMA (Seasonal Autoregressive Integrated Moving Average)
- VAR (Vector Autoregression) using car registrations from other countries
- ARIMAX (Autoregressive Integrated Moving Average with Explanatory Variables) using gasoline prices (`carburanti.xlsx`) and car registrations from other countries as regressors

Additionally, a significant shock in March 2020 due to the COVID-19 pandemic was modeled using a dummy variable.

## Results

The ARIMAX model with other countries' car registrations as regressors yielded the lowest MAPE at approximately 10%. However, predictions from the ARIMA and Exponential Smoothing models also closely matched the actual values, despite the assumption of normality not being met.

### Predicted vs Actual Values

- **Actual Value:** 162,083
- **SARIMA (1,0,1)(0,1,2)[12]:** 160,057.07
- **Exponential Smoothing:** 159,519.97
- **Holt-Winters:** 157,737.23

Interestingly, the Naive Model 1, which predicts the next value using the average of the series, provided the best prediction:

- **Naive Model 1 Prediction:** 163,158.3

## Conclusion

The ARIMAX model was the most accurate in terms of MAPE, but other models like ARIMA and Exponential Smoothing also performed well. Despite the non-normality of the data, these models provided close estimates, with the Naive Model 1 surprisingly giving the best prediction.

## Files

- `auto.xlsx`: Contains the time series data for car registrations up to February 2024.
- `Carburanti.xlsx`: Contains gasoline prices used as regressors in the ARIMAX model.
- `Progetto_Time_Series.Rmd`: The main script for running the different forecasting models (it is an RMarkdown file)
- 'Progetto_Time_Series.html': the output of the code and the final project

## Usage

1. Ensure you have the necessary libraries installed.


