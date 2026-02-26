# Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach

## Overview
- Generic software implementation of a Fuzzy changepoint (CPT) approach to assess how well numerical models capture local-scale shifts in environmental time series.
- Compares two time series (observations vs. model) to locate changepoints and quantify uncertainty via bootstrap.
- Converts changepoint locations and confidence intervals to fuzzy numbers and uses fuzzy logic to evaluate timing agreement between series.
- Produces individual similarity scores for each changepoint; higher scores indicate better model performance in capturing observed temporal changes.

## Data and inputs
- User uploads a CSV (or tab-delimited) with:
  - Dates: YYYY-MM-DD, one observation per line
  - ts_1: benchmark time series (observations)
  - ts_2: time series to evaluate against the benchmark (model)
- Data must be pre-processed to remove seasonality (via AR1 or AR2) before other functionality is available; app resets if data or AR settings change.

## Running the application
- Prerequisites: install R and required packages (details in Session_info.txt); tested with R 3.5.3 and 3.6.1.
- Ways to run:
  - Copy app.R contents into an R terminal and run
  - Open app.R in RStudio and click Run App
  - Run individual functions from Fuzzy_CPT_functions.R
- Additional guidance: reference information on running R Shiny apps at shiny.rstudio.com.

## Analysis options and outputs
- After preprocessing, select what to evaluate for changepoints: mean, variance, or mean and variance together.
- Choose the number of bootstrap samples to generate confidence intervals for changepoint locations (representing uncertainty).
- Run analysis to generate plots and tables summarising results.
- Download tab (available after analysis) allows exporting:
  - Spreadsheet of results
  - Model code used to produce the analysis
  - Note: download tab disappears if the app is reset.

## Implementation and environment
- The application provides a generic implementation of the fuzzy CPT approach described in Hollaway et al. (2021).
- Key features:
  - Uncertainty estimation for changepoint locations via bootstrap
  - Conversion of results to fuzzy numbers and evaluation via fuzzy logic
  - Per-changepoint similarity scores with interpretation tied to model performance
- Documentation and references:
  - Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software. https://doi.org/10.1016/j.envsoft.2021.104993

## Reference
- Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software. https://doi.org/10.1016/j.envsoft.2021.104993