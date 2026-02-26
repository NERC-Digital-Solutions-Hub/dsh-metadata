# Elter_inflow_2012-2019.txt

## Purpose and scope
- Provides estimated hourly average inflow discharge (inflow_Q) and water temperature (inflow_T) for the inner basin of Elterwater from January 2012 to December 2019.
- Data intended to support environmental health monitoring, policy scrutiny, and informing future decisions about water inflows and thermal dynamics.

## Data sources and derivation
- Inflow_Q derived from:
  - Gauged flow at Jeffy Knotts (NRFA station 735123) on the River Brathay.
  - Measured flow through a diversion pipeline (from SCRT).
- Calculation approach:
  - 2012–2015: inflow_Q = 2% of the gauged flow at Jeffy Knotts.
  - 2016–2019: inflow_Q = 2% of gauged flow at Jeffy Knotts plus measured pipeline flow.
- Handling missing diversion data:
  - <1% of diversion values were missing and imputed based on the relationship between pipeline measurements (Jan 2016–Dec 2019) and the gauged discharge in the River Brathay (lake outflow).
- Operational constraints and modeling:
  - Pipeline maximum hourly discharge capped at 0.122 m3/s; minimum source river discharge during abstraction 0.383 m3/s.
  - A general additive model (GAM) linked lake outflow to diversion discharges, used to interpolate/distribute flows where needed (R-squared = 0.53, p < 0.01).
- Inflow_T (temperature):
  - Direct measurements on the diversion pipeline from July 2017 to Dec 2019.
  - Temperature estimates for Jan 2012–June 2017 derived from a linear regression using the mean of the previous 12 hours’ air temperature; model: intercept 3.2, slope 0.67, R2 = 0.880, RMSE = 1.30°C.

## Data structure
- Single tab-delimited text file (.txt) with three columns:
  - Date (YYYY-MM-DD HH:MM:SS)
  - inflow_Q (m3/s)
  - inflow_T (°C)

## Data governance, transparency, and limitations
- Provenance includes data from Environment Agency and SCRT; reference cited: Environment Agency, 2000 (Elterwater: The Lakes Business Plan).
- Transparent accounting of data synthesis methods (percent-based inflow estimation, addition of pipeline flow, imputation for missing values, GAM relationship, and temperature estimation model).
- Acknowledges data-driven decisions and modeling choices that introduce estimation rather than direct measurement, with respective fit metrics (GAM R2 = 0.53; regression R2 = 0.880).
- Implicit considerations for metadata quality and data sharing: the dataset describes data sources, methods, and imputation steps, aiding reproducibility; however, full dataset-level metadata and accessibility constraints are not detailed.

## Relevance for monitoring and policy decision-making
- Enables assessment of hydrological inputs and thermal regime in the Elterwater inner basin, informing water resource management and potential ecological impacts.
- Supports evaluation of abstraction effects via the diversion pipeline and compliance with regulatory limits.
- Provides a temporal record suitable for trend analysis, policy evaluation, and communication of complex results through model-based estimates and measured data.