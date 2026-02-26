# Elter_inflow_2012-2019.txt

## Overview
- Estimated hourly inflow discharge and water temperature for the inner basin of Elterwater (coords: 54.42869, -3.034834) from January 2012 to December 2019.
- Designed for GIS-based analysis and map-enabled visualization of hydrological inflow dynamics.

## Data content and structure
- Variables:
  - inflow_Q: hourly inflow discharge (m3 s-1)
  - inflow_T: inflow water temperature (°C)
  - Date: timestamp (yyyy-mm-dd HH:MM:SS)
- File format: tab-delimited text with 3 columns (Date, inflow_Q, inflow_T).

## Data sources and estimation methods
- Primary gauged flow source: Environment Agency at Jeffy Knotts (NRFA station 735123; 54.42197, -2.989398) on the River Brathay.
- Pipeline diversion: measured flow through the diversion pipeline (54.43312, -3.036982), provided by South Cumbrian Rivers' Trust (SCRT).
- Inflow estimation approach:
  - 2012–2015: inflow ≈ 2% of gauged flow at Jeffy Knotts.
  - 2016–2019: inflow ≈ 2% of gauged flow at Jeffy Knotts plus measured pipeline flow.
  - Missing pipeline discharge values (<1%): imputed using a relationship derived from Jan 2016–Dec 2019 data between pipeline measurements and Brathay river gauge discharge (lake outflow) via a general additive model (GAM) with R-squared = 0.53.
  - When source discharge exceeded the 0.122 m3 s-1 diversion cap (0.122 m3 s-1 is the Environment Agency abstraction limit) the diversion discharge was capped at 0.122 m3 s-1.
  - When source discharge dropped below 0.383 m3 s-1, diversion was set to 0 m3 s-1.
- Inflow_T estimation:
  - July 2017–Dec 2019: direct temperature measurements on the diversion pipeline.
  - Jan 2012–Jun 2017: estimated via linear regression using the mean of the previous 12 hours of air temperature.
  - Regression model: intercept 3.2, slope 0.67; R^2 = 0.880; RMSE = 1.30°C.

## Temporal and spatial scope
- Temporal coverage: January 2012 – December 2019 (hourly data).
- Spatial references:
  - Inflow location: inner basin of Elterwater (54.42869, -3.034834).
  - Gauged source: Jeffy Knotts (NRFA 735123; 54.42197, -2.989398).
  - Diversion pipeline: (54.43312, -3.036982).
- Data resolution: hourly time series.

## Data quality, limitations, and considerations for GIS
- Mixed data sources (gauged flow, pipeline measurements) with data fusion and imputation.
- Several assumptions and model fittings:
  - Inflow estimation relies on fixed percentages of gauged flow for different periods and a GAM-based relationship for missing pipeline contributions.
  - Temperature estimation uses a regression model with a strong fit (R^2 = 0.880) for pre-2017 values.
- Key limitations:
  - Inflow uncertainty linked to estimation methods (percent-of-gauged-flow, GAM fit, annual variability).
  - Only ~1% of pipeline values were missing; the rest are measured.
- The dataset is suitable for GIS analyses that need hourly inflow and temperature alongside spatial references, but users should account for estimation methods and potential uncertainties in analyses or visualizations.

## Use in GIS workflows
- Suitable for creating time-series maps of inflow and temperature at the Elterwater inflow point and for linking with watershed or river network layers.
- Can be joined with spatial layers representing gauging stations, diversion pipelines, and lake outflow for integrated hydrological modeling.
- Useful for quality assurance and trend analyses across 2012–2019 at decadal or hourly scales.

## Reference
- Environment Agency, 2000. Elterwater: The Lakes Business Plan.