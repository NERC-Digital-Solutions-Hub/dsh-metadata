# Fuzzy changepoint approach to evaluate how well numerical models capture local scale shifts in environmental time series

## Purpose
- Provides a generic implementation of a Fuzzy changepoint approach to evaluate how well numerical models capture local scale shifts in environmental time series.
- Compares two time series (typically observations vs. model simulation) to detect changepoint locations.
- Uses bootstrap to estimate uncertainty in changepoint locations.
- Converts changepoint results to fuzzy numbers and applies fuzzy logic to assess timing agreement between series.
- Returns per-changepoint similarity scores, where higher scores indicate better model performance at capturing local scale changes.
- App expects a user-uploaded CSV containing the two time series to be compared.

## Running the application
- Requires R and the necessary packages (see Session_info.txt).
- Ways to run the Shiny app:
  - Copy the contents of app.R into an R terminal and run.
  - Open app.R in RStudio and click Run App.
- Individual analysis functions are available in Fuzzy_CPT_functions.R.
- Tested with R versions 3.5.3 and 3.6.1.
- Additional guidance on running Shiny apps available at the Shiny documentation link provided in the document.

## Using the application
- Acceptable input formats: CSV (tab-delimited allowed); one observation per line.
- Required columns, in this order:
  - Dates: YYYY-MM-DD
  - ts_1: time series 1 (typically observations)
  - ts_2: time series 2 (typically the model to evaluate)
- Pre-processing requirement:
  - After upload, the data must be pre-processed to remove seasonality (using an AR1 or AR2 model) before other functionality is available.
  - If the uploaded file or AR model settings change, the app resets.
- Analysis configuration after preprocessing:
  - Choose what to evaluate for changepoints: mean, variance, or mean and variance together.
  - Choose the number of samples to generate bootstrap confidence intervals for changepoint locations.
  - Click analyse to run; outputs include plots and tables summarising results.
- Outputs and data export:
  - A download tab appears after analysis to download a spreadsheet of results and/or the model code used.
  - The download tab disappears if the app is reset.
  
## Outputs and interpretation
- Provides individual similarity scores for each detected changepoint; higher scores reflect better alignment of changepoint timing between observation and model data.
- Produces plots and tables that summarise changepoint locations and associated uncertainty.
- Enables sharing of results and reproducible analysis by exporting data and code.

## Reference
- Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software. https://doi.org/10.1016/j.envsoft.2021.104993