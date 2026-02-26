# Elter_inflow_2012-2019.txt

## Overview
- Dataset of hourly average inflow discharge (inflow_Q, m3 s-1) and inflow water temperature (inflow_T, °C) for the inflow to the inner basin of Elterwater, covering January 2012 to December 2019.

## Data sources and how inflow is estimated
- Inflow_Q:
  - Derived from Environment Agency gauged flow at Jeffy Knotts (NRFA station 735123) on the River Brathay and measured flow through the diversion pipeline (SCRT).
  - 2012–2015: inflow = 2% of gauged flow at Jeffy Knotts.
  - 2016–2019: inflow = 2% of gauged flow at Jeffy Knotts plus measured pipeline flow.
  - Missing pipeline values (<1% of observations) imputed using the relationship between diversion measurements (2016–2019) and River Brathay gauged discharge; pipeline discharge capped at 0.122 m3/s and source river discharge minimum is 0.383 m3/s when abstraction is permitted.
  - When source discharge exceeded the 95th percentile used for capping, diversion discharge set to 0.122 m3/s; when source discharge dropped below 0.383 m3/s, diversion set to 0 m3/s.
  - Between flows, a general additive model (GAM) fitted between the measured lake outflow and diversion discharges (p < 0.01, R^2 = 0.53).

- Inflow_T:
  - Measured on the diversion pipeline from July 2017 to December 2019.
  - Relationship established between mean of the previous 12 hours’ air temperature and inflow temperature; used to estimate inflow temperature for January 2012–June 2017.
  - Linear regression (intercept = 3.2, slope = 0.67) to predict inflow temperature from 12-hour rolling air temperature data.
  - Model performance: R^2 = 0.880, RMSE = 1.30 °C.

## Data structure
- Single tab-delimited text file with 3 columns:
  - Date (yyyy-mm-dd HH:MM:SS)
  - inflow_Q (m3 s-1)
  - inflow_T (°C)

## Key assumptions and constraints
- Abstraction limits applied to pipeline flow:
  - Maximum hourly pipeline discharge: 0.122 m3/s
  - Minimum source river discharge when abstraction is permitted: 0.383 m3/s
- Diversion logic based on source discharge relative to thresholds:
  - If source > threshold, diversion capped at 0.122 m3/s
  - If source < 0.383 m3/s, diversion = 0
  - Intermediate values handled via GAM relationship (2016–2019 data)

## Provenance and references
- Environment Agency, 2000. Elterwater: The Lakes Business Plan.
- Diversion pipeline data supplied via South Cumbrian Rivers' Trust (SCRT).
- Gauged flow data from Environment Agency / NRFA (Jeffy Knotts, station 735123).

## Practical use for analysts
- Enables analysis of inflow dynamics and temperature in relation to river discharge and abstraction regimes.
- Suitable for validating hydrological models, assessing impact of abstraction on lake input, and calibrating temperature-inflow relationships.
- Includes explicit data processing steps and uncertainty indicators (GAM fit, R^2, p-values) and clear handling for missing values and data gaps.