# Elter_inflow_2012-2019.txt

## Overview
- Dataset of estimated hourly average inflow discharge (inflow_Q) and water temperature (inflow_T) for the inner basin of Elterwater, covering January 2012 to December 2019.
- Location specifics provided (lat/longs) for the inflow area; dataset comprises three columns: Date, inflow_Q (m3 s-1), inflow_T (°C).

## Data content and structure
- Data file format: tab-delimited text (.txt) with 3 columns:
  - Date (YYYY-MM-DD HH:MM:SS)
  - inflow_Q (m3 s-1)
  - inflow_T (°C)
- Inflow_Q described as inferred flow into the basin, derived from multiple sources.
- Inflow_T described as water temperature of the inflow, with temperature data available from July 2017 to December 2019; earlier temperatures estimated via a regression model.

## Provenance and data processing
- Inflow_Q derivation:
  - Primary gauged flow source: Environment Agency measurement at Jeffy Knotts (NRFA station 735123) on the River Brathay.
  - Diversion pipeline measurements (SCRT) used to supplement gauged flow.
  - 2012–2015: total inflow estimated as 2% of the gauged flow at Jeffy Knotts.
  - 2016–2019: total inflow estimated as 2% of gauged flow at Jeffy Knotts plus measured pipeline flow.
  - Missing pipeline discharge values (<1%) imputed using the relationship between pipeline measurements (2016–2019) and River Brathay gauged discharge.
  - Physical constraints applied: max hourly pipeline discharge 0.122 m3 s-1; minimum source river discharge when abstraction allowed 0.383 m3 s-1.
  - Rule-based adjustments: if source discharge exceeds the 95th percentile corresponding to the max diversion, set diversion to 0.122 m3 s-1; if source < 0.383 m3 s-1, set diversion to 0 m3 s-1.
  - A General Additive Model (GAM) related lake outflow to diversion discharges was fitted (R2 = 0.53; p < 0.01) for interpolation.
- Inflow_T derivation:
  - Direct measurements on the diversion pipeline from July 2017 to Dec 2019.
  - Temperature estimation for Jan 2012–June 2017 via a linear regression using the mean of the previous 12 hours' air temperature to predict inflow temperature.
  - Regression model: intercept = 3.2, slope = 0.67; R2 = 0.880; RMSE = 1.30°C.
- Documentation and references:
  - Data sources include Environment Agency and SCRT flows; reference: Environment Agency, 2000. Elterwater: The Lakes Business Plan.
  - Structural description notes the 3-column data format and timestamps.

## Quality, limitations, and uncertainty
- Inflow_Q: dependent on assumptions and relationships between gauged flows, pipeline measurements, and imposed caps; missing pipeline values imputed using historical relationships.
- Model performance: GAM fit (R2 = 0.53) indicates moderate explanatory power for outflow–diversion relationship; some uncertainty in derived inflow values.
- Inflow_T: pre-2017 temperatures estimated from air temperature with a strong linear relation (R2 = 0.880), but still subject to meteorological variability and regression uncertainty (RMSE ~1.3°C).
- Temporal coverage: 2012–2019, with direct temperature measurements only from 2017–2019.
- Units and coordinates are specified, aiding interoperability but requiring consistent unit handling in downstream use.

## Metadata and documentation
- Data structure clearly defined: tab-delimited text file with Date, inflow_Q, inflow_T.
- Location coordinates provided for context: inflow area lat 54.42869, long -3.034834.
- Data sources and transformation steps described, enabling reproducibility or future reprocessing.

## Data Stewardship considerations
- Standards and governance:
  - Document data provenance, sources, and all estimation/transformation steps (including cap rules and regression models) in metadata.
  - Record model parameters (GAM details, regression intercept/slope) and versioning for reproducibility.
  - Include notes on imputation strategies for missing pipeline discharge values.
  - Ensure units are consistently applied and clearly labeled (m3 s-1, °C).
- Data quality management:
  - Capture and communicate uncertainties from estimation methods and model fits.
  - Track any updates to source data (gauged flows or pipeline measurements) that would alter derived inflows.
- Access, storage, and sharing:
  - Maintain the .txt data file with clear schema documentation; consider cataloging in a dataset repository with provenance, methodology, and references.
  - Include a licensing statement or usage rights if applicable, and ensure alignment with referenced sources (Environment Agency, SCRT) in metadata.
- Interoperability:
  - The structure (Date, inflow_Q, inflow_T) supports time-series analyses; ensure time zone handling is explicit if applicable.
  - When integrating with other datasets, align dates, units, and aggregation levels (hourly) to prevent mismatches.