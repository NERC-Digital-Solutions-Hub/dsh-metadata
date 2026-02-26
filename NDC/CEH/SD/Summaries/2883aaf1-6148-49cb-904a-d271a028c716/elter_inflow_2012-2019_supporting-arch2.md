# Elter_inflow_2012-2019.txt

## Purpose and scope
- Estimated hourly average inflow discharge (inflow_Q) and water temperature (inflow_T) of the inflow to the inner basin of Elterwater (lat: 54.42869, lon: -3.034834) for 2012–2019.
- Data derived from a combination of gauged river flow and a diversion pipeline, with coordinates and station references provided.

## Data sources
- Gauged flow at Jeffy Knotts (NRFA station 735123; lat: 54.42197, lon: -2.989398) on the River Brathay.
- Measured flow through a diversion pipeline (SCRT) at lat: 54.43312, lon: -3.036982.
- Method changes occurred between 2012–2015 versus 2016–2019 for inflow estimation.
- Abstraction limits: pipeline max 0.122 m3/s; source river minimum permitted discharge 0.383 m3/s.
- Data and relationships used for imputations and modelling described below.

## Inflow_Q methodology
- 2012–2015: inflow_Q estimated as 2% of gauged flow at Jeffy Knotts.
- 2016–2019: inflow_Q = 2% of gauged flow at Jeffy Knotts plus measured pipeline flow.
- Missing pipeline discharge values (<1%) imputed using the relationship between pipeline measurements (Jan 2016–Dec 2019) and gauged River Brathay discharge (lake outflow) via a general additive model (GAM).
- Rule-based adjustments:
  - If source discharge exceeds the 95th percentile corresponding to the maximum (capped) diversion discharge (0.122 m3/s), diversion is maximised at 0.122 m3/s.
  - If source discharge drops below 0.383 m3/s, diversion is 0 m3/s.
  - Between these flows, a GAM was fitted between measured lake outflow and diversion discharges (p < 0.01, R^2 = 0.53).
- Resulting approach combines gauged flow with diversion data under defined constraints.

## Inflow_T methodology
- Inflow temperature measured on the diversion pipeline from July 2017 to December 2019.
- For January 2012–June 2017, temperature was estimated using a linear relationship with the mean of the previous 12 hours’ air temperature:
  - Model: temperature = 3.2 + 0.67 × (12-hour rolling mean air temp)
  - R^2 = 0.880, RMSE = 1.30 °C (Figure 2 shows fit).
- This relationship was used to estimate inflow temperature prior to direct measurements.

## Data structure and contents
- Single tab-delimited text file (.txt) with 3 columns:
  - Date (YYYY-MM-DD HH:MM:SS)
  - inflow_Q (m3 s-1)
  - inflow_T (°C)

## Data quality and stewardship
- Data are verified, quality assured, cleaned, and transformed for standardised use.
- Generated datasets are stored and uploaded to appropriate data portals as part of ongoing environmental monitoring.

## Temporal coverage and units
- Time period: January 2012 – December 2019.
- Units: inflow_Q in cubic metres per second (m3 s-1); inflow_T in degrees Celsius (°C).

## Limitations and caveats
- Inference relies on estimation methods for 2012–2015 and imputation for missing pipeline values.
- Model performance:
  - GAM linking lake outflow and diversion discharges: R^2 = 0.53 (p < 0.01).
  - Temperature estimation via air temperature: R^2 = 0.880; RMSE = 1.30 °C.
- Dependency on underlying assumptions about abstraction limits and relationships between flows.

## Reference
- Environment Agency, 2000. Elterwater: The Lakes Business Plan.