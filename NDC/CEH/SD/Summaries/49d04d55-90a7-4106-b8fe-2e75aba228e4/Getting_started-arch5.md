# 1. Purpose

- Presents a generic implementation of a Fuzzy changepoint approach to evaluate how well numerical models capture local scale shifts in environmental time series.
- Compares two time series (typically observations vs model simulation) to detect changepoints and uses bootstrap to estimate uncertainty in changepoint locations.
- Converts changepoint locations and their confidence intervals into fuzzy numbers and applies fuzzy logic to assess agreement in changepoint timing between the series.
- Outputs individual similarity scores for each changepoint, where higher scores indicate better model performance at capturing local temporal changes. Users upload a CSV containing the two time series.

## 2. Running the application

- Requires R and the required R packages (see Session_info.txt).
- How to run:
  - Copy the contents of app.R into an R terminal and run.
  - Or open app.R in RStudio and click the Run App button.
- Individual functions can be executed from scripts in Fuzzy_CPT_functions.R.
- Tested on R versions 3.5.3 and 3.6.1; testing details available in Session_info.txt.
- Additional guidance on running R Shiny apps is available at the linked Shiny documentation.

## 3. Using the application

- Acceptable input format: CSV (tab-delimited also allowed); one observation per line with these columns in this order:
  - Dates: YYYY-MM-DD
  - ts_1: Time series 1 (benchmark/observations)
  - ts_2: Time series 2 (model to evaluate)
- Pre-processing requirement: remove seasonality using an AR(1) or AR(2) model before other functionality becomes available. Changing the uploaded data or AR settings will reset the app.
- After pre-processing, specify:
  - What to evaluate for changepoints (mean, variance, or mean and variance)
  - The number of samples used to generate confidence intervals for changepoint locations
- Run analysis by pressing the analyse button. Output includes plots and tables summarising results.
- Download options:
  - A tab to download a spreadsheet of results and/or the model code used.
  - The download tab disappears if the app is reset.

## 4. References

- Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software. https://doi.org/10.1016/j.envsoft.2021.104993

## Data Stewardship considerations

- Data format and metadata: Ensure input CSV adheres to required column order and date format (YYYY-MM-DD) to guarantee reproducible results.
- Provenance and reproducibility: The app supports exporting results and the used model code; preserve raw input data and the analysis scripts to enable reruns.
- Data quality and standards: Seasonality removal is a defined preprocessing step; provide clear metadata on AR model settings used (AR1/AR2) and any data transformations.
- Interoperability and updates: The app resets if inputs or settings change, highlighting the need for versioned datasets and traceable preprocessing steps to maintain auditability.
- Handling large datasets and formats: Be aware of potential challenges with large time series and non-standard formats; document any format conversions and transfer considerations.