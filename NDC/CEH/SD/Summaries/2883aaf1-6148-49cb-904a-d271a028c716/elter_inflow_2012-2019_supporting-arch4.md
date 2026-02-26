# Elter_inflow_2012-2019.txt

## Overview
- Dataset of estimated hourly average inflow discharge (inflow_Q) and water temperature (inflow_T) for the inner basin of Elterwater, 2012-2019.
- Provides temporal coverage from January 2012 to December 2019 with three columns: Date, inflow_Q (m3 s-1), inflow_T (°C).

## Data content and structure
- File type: tab-delimited text (.txt) with 3 columns:
  - Date (yyyy-mm-dd HH:MM:SS)
  - inflow_Q (m3 s-1)
  - inflow_T (°C)

## Inflow discharge (inflow_Q) methodology
- Baseline from Environment Agency gauged flow at Jeffy Knotts (NRFA station 735123).
- Diversion pipeline flow measured by South Cumbrian Rivers' Trust (SCRT).
- 2012–2015: inflow_Q estimated as 2% of gauged flow at Jeffy Knotts.
- 2016–2019: inflow_Q estimated as 2% of gauged flow at Jeffy Knotts plus measured diversion pipeline flow (SCRT).
- Missing diversion values (<1% of records) were imputed using:
  - Relationship between diversion pipeline measurements and gauged discharge in the River Brathay (lake outflow) to guide estimation.
- Constraints:
  - Maximum pipeline discharge cap: 0.122 m3 s-1 (abstraction limit).
  - Minimum source discharge when abstraction is allowed: 0.383 m3 s-1.
  - If source discharge exceeded the 95th percentile guiding the cap, diversion set to 0.122 m3 s-1.
  - If source discharge dropped below 0.383 m3 s-1, diversion set to 0.
  - For intermediate flows, a General Additive Model (GAM) was fitted between measured lake outflow and diversion discharges (R-squared = 0.53; p < 0.01).

## Inflow temperature (inflow_T) methodology
- Direct measurements on the diversion pipeline from July 2017 to December 2019.
- To estimate inflow_T for 2012–June 2017, a linear regression was developed using:
  - Predictor: mean of the previous 12 hours' air temperature
  - Response: inflow_T
  - Model: intercept = 3.2, slope = 0.67
  - Fit: R-squared = 0.880, RMSE = 1.30 °C
- This model was used to estimate inflow_T prior to July 2017 measurements.

## Data quality, assumptions, and limitations
- Inflow_Q relies on multiple data sources and several imputation/estimation steps.
- GAM fit for outflow–diversion relationship explains about 53% of variance (moderate fit).
- Temperature estimates for 2012–2017 depend on a regression with air temperature, introducing model-based uncertainty.
- If diversion data are missing, imputation is guided by established relationships and established bounds.

## Data provenance and references
- Primary sources:
  - Environment Agency gauged flow at Jeffy Knotts (NRFA 735123)
  - Diversion pipeline measurements from SCRT
- Reference: Environment Agency, 2000. Elterwater: The Lakes Business Plan.

## Practical implications for data leadership
- Clear lineage and multi-source integration with explicit imputation rules and model choices.
- Metadata should document the bounds, cap/ minimums, and model performance (e.g., GAM R^2 and RMSE for traceability and future improvement).
- Opportunities to improve data quality: reduce reliance on imputed/diversion-derived values, validate GAM predictions against more observations, and enhance metadata on data gaps.