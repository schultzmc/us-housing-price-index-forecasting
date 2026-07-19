# US Housing Price Index Forecasting
A time series analysis forecasting the US Housing Price Index (HPI) using SARIMA and ARMAX models.

## Abstract
This project analyzes 41,265 observations across 21 variables combining US Housing Price Index (HPI) data with macroeconomic and financial market indicators, spanning January 1991 to December 2023. The analysis fits a SARIMA(p,d,q)x(P,D,Q) model on the non-seasonally adjusted monthly HPI series, then extends to an ARMAX/lagged regression model using macroeconomic variables (GDP, inflation, unemployment, imports, exports) as exogenous predictors. The goal is to decompose trend, seasonal, and cyclical components of US housing prices and evaluate short-term forecasting performance.

## Files 
- Final-Project.Rmd / Final_Project.Rmd — main R Markdown files containing the analysis
- Final-Project.pdf / Final_Project.pdf — knitted PDF outputs of the final report
- USDataset.csv — combined HPI, macroeconomic, and financial indicator dataset used for the analysis
- plot_acf.png, plot_pacf.png — autocorrelation and partial autocorrelation plots
- plot_diff1.png, plot_diff2.png — differenced series plots for stationarity checks
- plot_hpi_original.png — original (undifferenced) HPI series
- plot_sarima_acf.png, plot_sarima_res.png — SARIMA model diagnostics
- plot_armax_acf.png, plot_armax_res.png — ARMAX model diagnostics
- plot_forecast.png — forecasted HPI values
- plot_qq.png — Q-Q plot for residual normality check

## How to Run
Open Final-Project.Rmd in RStudio and knit to PDF (requires USDataset.csv in the same directory).

## Methods
- Box-Jenkins approach: identification, estimation, and diagnostic checking
- Log transformation to stabilize variance
- ADF and KPSS unit root tests for stationarity
- Regular and seasonal differencing (s = 12 for monthly data)
- ACF/PACF inspection to identify candidate SARIMA orders
- SARIMA modeling on the non-seasonally adjusted HPI series
- ARMAX/lagged regression extension using macroeconomic variables as exogenous predictors

## Data Source
Data combines FHFA Housing Price Index records, IMF World Economic Outlook variables, and S&P 500 daily closing prices, publicly available on Kaggle.

## Author
Madison Schultz 
