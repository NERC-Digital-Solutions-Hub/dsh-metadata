# Elter_inflow_2012-2019.txt

- Description provides estimated hourly average inflow discharge (inflow_Q, m3 s-1) and water temperature (inflow_T, °C) for the inner basin of Elterwater from January 2012 to December 2019 (lat: 54.42869, lon: -3.034834).

- Data sources and inflow estimation
  - Inflow discharge (inflow_Q) derived from:
    - Gauged flow at Jeffy Knotts (NRFA station 735123; lat 54.42197, lon -2.989398) on the River Brathay.
    - Measured flow through a diversion pipeline (SCRT; lat 54.43312, lon -3.036982).
  - Estimation approach by period:
    - Jan 2012–Dec 2015: inflow ≈ 2% of gauged flow at Jeffy Knotts.
    - Jan 2016–Dec 2019: inflow ≈ 2% of gauged flow at Jeffy Knotts + measured pipeline flow.
  - Handling of missing pipeline values (<1%):
    - Imputed using a relationship between diversion measurements (Jan 2016–Dec 2019) and Brathay river gauged discharge (lake outflow) via a general additive model (GAM). Model fit: p < 0.01, R2 = 0.53.
  - Diversion constraints and rules:
    - Maximum pipeline discharge capped at 0.122 m3 s-1 (abstraction limit).
    - Minimum source discharge for permitted abstraction is 0.383 m3 s-1.
    - If source discharge exceeds the 95th percentile corresponding to the max capped diversion, diversion is set to 0.122 m3 s-1.
    - If source discharge drops below 0.383 m3 s-1, diversion is set to 0 m3 s-1.

  - Model reference for outflow-diversion relationship: Figure 1 (observations vs. model fit).

- Inflow temperature (inflow_T)
  - Measured on the diversion pipeline from July 2017 to December 2019.
  - Temperature estimation prior to July 2017 (January 2012–June 2017) using a linear relationship with the mean of the previous 12 hours of air temperature.
  - Final linear model (for temperature estimation):
    - Intercept 3.2, slope 0.67
    - R^2 = 0.880, RMSE = 1.30 °C
  - Temperature prediction is based on the 12-hour rolling average air temperature (Figure 2 shows observations and fitted line).

- Data structure and format
  - Single tab-delimited text file (.txt).
  - Three columns: Date (yyyy-mm-dd HH:MM:SS), inflow_Q (m3 s-1), inflow_T (°C).

- Data quality and limitations
  - Missing diversion values are minimal (<1%) and imputed via GAM-based relationship.
  - Inflow_Q estimation combines gauged river flow with pipeline measurements; subject to abstraction constraints and assumed relationships in periods without direct measurements.
  - Temperature estimates prior to 2017 rely on a linear regression with a strong fit (R^2 = 0.880) but are model-based.

- References
  - Environment Agency, 2000. Elterwater: The Lakes Business Plan.

- Potential uses for data support and analytics
  - Hydrological modelling and water resource management for Elterwater’s inner basin.
  - Ecological and environmental impact assessments related to inflow and water temperature.
  - Creation of dashboards or reports enabling end users to explore hourly inflow and temperature trends over 2012–2019.
  - Data provenance and quality checks to support reproducibility and policy decisions.