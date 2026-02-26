# Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach

- What it is
  - A generic implementation of a Fuzzy changepoint approach to assess how well numerical models capture local scale shifts in environmental time series, following Hollaway et al. (2021).

- Core approach
  - Detects changepoints in two time series (observations vs. model simulation).
  - Uses bootstrap to estimate uncertainty on changepoint locations.
  - Converts changepoint locations and confidence intervals into fuzzy numbers.
  - Applies fuzzy logic to evaluate agreement in changepoint timing between series.
  - Produces a similarity score for each changepoint; higher scores indicate better model performance at capturing local temporal changes.

- Data requirements
  - Input: CSV file with three columns in this order: Dates (YYYY-MM-DD), ts_1 (benchmark/observations), ts_2 (model time series).
  - Accepts tab-delimited files as an alternative.
  - One observation per line.

- Pre-processing and data preparation
  - Pre-process to remove seasonality using an AR1 or AR2 model before analysis.
  - Changing the uploaded data or AR settings resets the app.

- Analysis options
  - Evaluate changes on mean, variance, or both.
  - Choose the number of bootstrap samples for constructing confidence intervals on changepoint location.

- Output and results
  - Graphs and tables summarising results.
  - Downloadable spreadsheet of results and/or the analysis code used.
  - Download tab available after analysis; disappears on app reset.

- Running the application
  - Requires R and the necessary packages (listed in Session_info.txt).
  - Run via Shiny app (app.R) by:
    - Copying app.R into an R terminal, or
    - Opening app.R in RStudio and clicking Run App.
  - Individual functions are available in Fuzzy_CPT_functions.R for direct execution.
  - Tested with R versions 3.5.3 and 3.6.1.

- References
  - Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software. DOI: https://doi.org/10.1016/j.envsoft.2021.104993

- Relevance for environmental monitoring analysts
  - Provides a standardized, transparent method to validate model performance against observed environmental shifts.
  - Facilitates uncertainty quantification in changepoint timing, improving interpretation for policy and monitoring evaluations.
  - Supports data management by enabling export of results and reproducible analysis code.