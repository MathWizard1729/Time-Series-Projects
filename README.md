# Time Series Projects

## Airline traffic forecasting (`Airline_TS.ipynb`)

Statistical analysis and forecasting of monthly airline traffic, October 2002 to March 2017,
focused on revenue passenger miles (`RPM_Domestic` and `RPM_International`).

**Analysis**
- Exploration and seasonal decomposition
- Trend and stationarity tests: Mann-Kendall, Kruskal-Wallis, ADF and KPSS, each before and after differencing
- Non-seasonal, seasonal and combined differencing

**Models compared**
- Holt-Winters exponential smoothing (additive trend and seasonality, period 12)
- `auto_arima`, then ARIMA and SARIMAX fits
- An LSTM network (TensorFlow/Keras)

Forecasts are scored with error metrics such as MAPE in the notebook.

## Data

`all_airlines_all_airports.csv` is read by the notebook but is **not included** here. Add it next to
the notebook before running. Each row is a month, with the date set to the first of the month.

## Running

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels pmdarima pymannkendall scikit-learn tensorflow
jupyter notebook Airline_TS.ipynb
```
