# Fuzzy changepoint approach to evaluate how well numerical models capture local scale shifts in environmental time series

## Purpose
- Presents a generic implementation of a Fuzzy changepoint approach to assess how well numerical models capture local-scale shifts in environmental time series.
- Compares two time series (typically observations vs. model simulation) to locate changepoints and uses bootstrap to quantify uncertainty in changepoint locations.
- Converts changepoint locations and confidence intervals into fuzzy numbers and applies fuzzy logic to evaluate how well the timing of changepoints agrees between the series.
- Produces individual similarity scores for each changepoint, with higher scores indicating better model performance at capturing observed temporal changes.
- Users upload a CSV file containing the two time series to be compared.

## Running the application
- Requires installing R and the necessary packages; tested on R versions 3.5.3 and 3.6.1 (see Session_info.txt).
- Run options:
  - Copy contents of app.R into an R terminal and run.
  - Open app.R in RStudio and click the Run App button.
  - Run individual functions from Fuzzy_CPT_functions.R.
- Additional running guidance available from standard R Shiny documentation.

## Using the application
- Input file format: CSV (tab-delimited accepted); one observation per line with three columns in this order:
  - Dates (YYYY-MM-DD)
  - ts_1: benchmark/observations
  - ts_2: model time series to evaluate against ts_1
- Pre-processing: after upload, remove seasonality using an AR(1) or AR(2) model before other functionality is enabled; changing the file or AR settings resets the app.
- Analysis options after pre-processing:
  - Choose what to evaluate (mean, variance, or mean and variance).
  - Set the number of bootstrap samples for constructing confidence intervals on changepoint location (reflecting uncertainty).
- Output: pressing analyse generates plots and tables summarising results.
- Post-analysis: a download tab appears to download a spreadsheet of results and/or the model code used for the analysis; the download tab disappears if the app is reset.

## References
- Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software. https://doi.org/10.1016/j.envsoft.2021.104993