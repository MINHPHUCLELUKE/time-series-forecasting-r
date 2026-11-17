# Time Series Forecasting in R

Two time series analysis reports in R, each taking a real series from exploration through stationarity testing, transformation, model specification and selection.

| Report | Series | Selected model | Highlights |
|---|---|---|---|
| [Global CO2 Concentration Time Series Analysis and Forecasting](./co2) | Monthly CO2 at Mauna Loa, Apr 2015 to Apr 2025 | SARIMA(1,2,2)(0,1,1)[12] | Eight SARIMA candidates compared; 10-month forecast predicting 430 ppm, which NOAA confirmed in May 2025 |
| [Bitcoin Index Time Series Analysis](./bitcoin) | Monthly Bitcoin index, Aug 2011 to Jan 2025 | ARIMA(1,1,0) | Box-Cox transformation, model specification with ACF/PACF, EACF and BIC table, ML and CSS estimation |

**Full reports (PDF):** [CO2](./co2/global-co2-time-series-analysis.pdf) · [Bitcoin](./bitcoin/bitcoin-index-time-series-analysis.pdf)

## Follow-up analyses

Each project also has a short follow-up that tests the selected model on data it did not see:

- **CO2:** the report's forecast compared with 17 months of NOAA readings published afterwards. [View (live)](https://minhphucleluke.github.io/time-series-forecasting-r/co2/follow-up/co2-forecasting-report.html)
- **Bitcoin:** ARIMA(1,1,0) compared with a random walk on the last 24 months. [View (live)](https://minhphucleluke.github.io/time-series-forecasting-r/bitcoin/follow-up/bitcoin-forecasting-report.html)

## Repository layout

```
co2/        Report (PDF), key figures, data, follow-up analysis
bitcoin/    Report (PDF), key figures, data, follow-up analysis
```

## Tools

`R` · `forecast` · `TSA` · `tseries` · `urca` · `lmtest` · `R Markdown`
