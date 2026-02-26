# Purpose

- The document describes a generic software implementation of a Fuzzy changepoint approach to assess how well numerical models capture local-scale shifts in environmental time series.
- It compares two time series (observations benchmark vs. model simulation) to identify changepoints, estimate their uncertainty via bootstrap, convert changepoint information to fuzzy numbers, and use fuzzy logic to evaluate timing agreement.
- The app provides individual similarity scores for each changepoint; higher scores indicate better model performance in capturing local temporal changes.

- Input and data requirements:
  - User uploads a CSV file containing: Dates (YYYY-MM-DD), ts_1 (benchmark/observations), ts_2 (model to be evaluated).
  - Data must have one observation per line and use the specified column order.
  - Acceptable formats: CSV (also tab-delimited accepted).

- Data preparation and workflow:
  - Pre-process data to remove seasonality using an AR(1) or AR(2) model before other functionality becomes available.
  - After preprocessing, users choose what to evaluate (mean, variance, or mean and variance) and the number of bootstrap samples for confidence intervals on changepoint locations.
  - Run analysis to generate plots and tables summarising results.
  - The app outputs per-changepoint similarity scores; higher scores imply better model alignment with observed shifts.

- Running and implementation details:
  - Requires R and the necessary R packages (see Session_info.txt).
  - Ways to run:
    - Copy contents of app.R into an R terminal.
    - Open app.R in RStudio and click Run App.
  - Individual functions can be executed from Fuzzy_CPT_functions.R.
  - Tested with R versions 3.5.3 and 3.6.1; additional guidance in Session_info.txt.
  - Shiny app running guidance available at Shiny’s website (as of 2021).

- Outputs and reproducibility:
  - After analysis, a download tab appears offering:
    - A spreadsheet of results.
    - The model code used to produce the analysis.
  - The download tab disappears if the app is reset.

- Reference:
  - Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software.