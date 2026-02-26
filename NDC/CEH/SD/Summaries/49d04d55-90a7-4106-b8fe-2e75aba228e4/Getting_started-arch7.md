# 1. Purpose

## Overview
- This is a generic implementation of a Fuzzy changepoint approach to evaluate how well numerical models capture local scale shifts in environmental time series.
- It compares two time series (typically observations vs. model simulation) to locate changepoints and uses bootstrap to estimate uncertainty in changepoint locations.
- Changepoint locations and their confidence intervals are converted to fuzzy numbers; fuzzy logic assesses how well the timing of changepoints agrees between the series.
- The app outputs individual similarity scores for each changepoint, with higher scores indicating better model performance at capturing local temporal changes.
- Users upload a CSV containing the two time series.

## How it works
- Detects changepoints in both time series and estimates location uncertainty via bootstrap.
- Converts changepoints and CIs to fuzzy numbers; applies fuzzy logic to evaluate timing agreement.
- Returns a similarity score per changepoint, reflecting model performance on local temporal shifts.

## Using the application
- Input format: CSV (tab-delimited accepted). One observation per line, columns in this order:
  - Dates: YYYY-MM-DD
  - ts_1: Time series 1 (benchmark/observations)
  - ts_2: Time series 2 (model to evaluate)
- Pre-processing: remove seasonality using an AR1 or AR2 model before other functionality; app will reset if data or AR settings change.
- After preprocessing: choose evaluation focus (mean, variance, or mean and variance) and specify the number of samples for confidence intervals (uncertainty).
- Run: click analyse to perform the analysis; outputs include plots and tables.
- Download: a tab appears to download a spreadsheet of results and/or the model code used; the download tab disappears if the app is reset.

## Running the application
- Prerequisites: install R and required packages (see Session_info.txt).
- Ways to run:
  - Copy the contents of app.R into an R terminal and run.
  - Open app.R in RStudio and click Run App.
- Individual functions can be executed from Fuzzy_CPT_functions.R.
- Tested with R versions 3.5.3 and 3.6.1; see Session_info.txt for details.
- Additional guidance on running Shiny apps is available at shiny.rstudio.com.

## Reference
- Hollaway, M.J.; Henrys, P.A.; Killick, R.; Leeson, A.; Watkins, J. (2021). Evaluating the ability of numerical models to capture important shifts in environmental time series: A Fuzzy change point approach. Environmental Modelling & Software. https://doi.org/10.1016/j.envsoft.2021.104993

## Relevance for GIS Specialists
- Data preparation and integration: accepts two time series (e.g., observed vs. modeled) that can be derived from GIS-based data layers or spatially distributed time series.
- Outputs suitable for GIS workflows: provides quantitative similarity scores per changepoint and associated plots/tables that can be linked to spatial analyses (e.g., model performance across locations or regions when applied to multi-site data).
- Uncertainty framing: bootstrap-based changepoint uncertainty and fuzzy logic outputs support robust decision-making in spatial planning and environmental management.
- Preprocessing in spatial context: AR-based deseasonalization can be aligned with spatial-temporal data cleaning typically performed in GIS projects.
- Practical constraints: requires CSV-formatted time series data with consistent temporal resolution and clean pre-processing, aligning with data standardisation challenges common in GIS work.