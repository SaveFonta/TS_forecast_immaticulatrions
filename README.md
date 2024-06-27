# TS_forecast_immaticulatrions
 This is the script of the "Forecasting Competition" of Unibo. The goal of the competition is to forecast the number of immatriculated cars in Italy in March 2024. The time serie of the immatriculation arrives till February 2024 ("auto.xlsx"). I tried to fit a few models to reduce the MAPE and the MSE, after a decomposition of the Time Series (in two different ways). I tried canonical exponential smoothing, Holt and Winters exponential smoothing, then I fitted a SARIMA model,  a VAR model using other countries' values,  ARIMAX using gasoline prices (carburanti.xlsx) and other countries' prices as regressors. I also found a big shock in March 2020 due to the COVID epidemy, so I tried to model it using a dummy variable. 