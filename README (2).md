# Bulgaria Population Forecast: Time Series Modelling (2010–2024)

Time series analysis and forecast of Bulgaria's total population using trend models, exponential smoothing and ARIMA in IBM SPSS Statistics. Coursework in Time Series Analysis Software at the University of National and World Economy (UNWE), Sofia.

## Objective

To identify the long-term trend in Bulgaria's population, compare forecasting methods and choose the most accurate one for a short-term forecast (2025–2026).

## Data

- **Source:** National Statistical Institute of Bulgaria (NSI)
- **Type:** annual, non-seasonal time series, 2010–2024 (15 observations)
- **File:** `bulgaria_population_2010_2024.csv`

## Tools

- **IBM SPSS Statistics**: sequence charts, autocorrelation function (ACF), curve estimation, exponential smoothing, ARIMA
- **Microsoft Excel**: data preparation

## Methodology

1. **Visual analysis:** sequence chart of the series
2. **Stationarity check:** the slowly decaying ACF (lag 1 ≈ 0.75) shows a non-stationary series with a trend
3. **Trend model selection:** comparison of 11 curve estimation models in SPSS
4. **Holt's exponential smoothing:** suitable for a series with a trend and no seasonality
5. **ARIMA(1,1,0):** first differencing to reach stationarity
6. **Model comparison** by R², MAPE and parameter significance

## Exploratory Findings

- The population fell from **7.50 million (2010)** to **6.44 million (2024)**, a decline of about 14%.
- The series has **three phases**:
  - 2010–2011: a sharp drop after the 2011 census updated the official figures
  - 2011–2021: a steady decline driven by emigration, low birth rates and high mortality
  - 2021–2022: another sharp drop after the 2021 census, followed by stabilisation
- The 2011 and 2022 drops are **structural breaks** caused by census revisions, not real one-year demographic changes. This was taken into account in the modelling.

## Model Comparison

| Model | R² | MAPE | Notes |
|---|---|---|---|
| Linear trend | 0.919 | – | Best of 11 curve estimation models, chosen for simplicity |
| **Holt's exponential smoothing** | **0.919** | **0.788%** | RMSE ≈ 97,800 people |
| ARIMA(1,1,0) | 0.900 | 0.868% | AR(1) coefficient not significant (p = 0.700) |

**Selected model: Holt's exponential smoothing.** It has higher R², lower forecast error and fewer weak parameters than ARIMA.

## Forecast

Both models forecast a continued decline, to about **6.3 million people in 2026**.

## Author

**Viktoria Vutova**: [LinkedIn](https://www.linkedin.com/in/viktoria-vutova-964294247)
