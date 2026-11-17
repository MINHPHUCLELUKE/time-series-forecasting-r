# Time Series Forecasting in R

Two forecasting case studies, each tested the way a forecast is actually used: on data the model has not seen.

| Case study | Question | Headline |
|---|---|---|
| [Global CO2 at Mauna Loa](./co2) | How well did a SARIMA forecast made in April 2025 match what NOAA then measured? | All 17 new readings fell inside the 95% band, but the forecast ran high and the gap grew. A simpler trend cut the error by a fifth. |
| [Bitcoin index](./bitcoin) | Does an ARIMA model forecast a crypto index better than a random walk? | No. Month to month it did no better, and over two years a simple upward drift mattered far more than the ARIMA structure. |

**Live reports:** [CO2](https://minhphucleluke.github.io/time-series-forecasting-r/co2/co2-forecasting-report.html) · [Bitcoin](https://minhphucleluke.github.io/time-series-forecasting-r/bitcoin/bitcoin-forecasting-report.html)

## How both studies are tested

1. **Fit on the past, test on the future.** The last 24 months are held back, and every model is fit only on the data before them.
2. **Compare with simple benchmarks.** A model earns its place only if it beats a naive forecast: a random walk for Bitcoin, a seasonal naive forecast for CO2.
3. **Report what the numbers say,** including when the original model turns out not to be the best one.

The CO2 study adds a reality check: forecasts from the end of the study period compared with 17 months of real readings published afterwards.

## Repository layout

```
co2/        SARIMA forecasting of Mauna Loa CO2 (R Markdown, data, figures, report)
bitcoin/    ARIMA and GARCH analysis of a monthly Bitcoin index (R Markdown, data, figures, report)
```

Each folder has its own README with findings and method, the `.Rmd` source, the data, the rendered HTML report and the original full write-up as a PDF.

## Tools

`R` · `forecast` · `TSA` · `tseries` · `rugarch` · `R Markdown`
