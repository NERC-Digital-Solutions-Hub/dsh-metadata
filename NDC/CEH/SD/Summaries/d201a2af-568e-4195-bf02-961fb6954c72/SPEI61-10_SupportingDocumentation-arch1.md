# Supporting Information

## Overview
- Datasets of 1 km and 5 km gridded Standardised Precipitation-Evapotranspiration Index (SPEI) for Great Britain.
- SPEI based on Climatic Water Balance (CWB = precipitation minus evapotranspiration) over various accumulation periods (1, 3, 6, 12, 18, 24 months) and for all 12 calendar months.
- Time coverage: 1961–2012; standard fitting period: 1961–2010.
- Stored in NetCDF4 format on the CEH-THREDDS-WATER server.

## Motivation
- Derived within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices against impacts data for monitoring and early warning.
- SPEI incorporates evapotranspiration, offering a drought measure that can be compared to hydrological and ecological variables and used for drought monitoring across time scales.
- Provides multiple time-scale perspectives:
  - 1-month SPEI: short-term soil moisture/crop stress.
  - 3-month SPEI: short- to medium-term moisture; seasonal CWB.
  - 6-month SPEI: medium-term trends; potential links to streamflow/reservoir levels.
  - 12-month SPEI: long-term CWB patterns; ties to longer hydrological signals.
  - 18–24-month SPEI: extended long-term patterns; groundwater-related signals.

## Data Sources
- CEH-GEAR: Gridded estimates of daily and monthly areal rainfall for the UK.
- CHESS PET: Potential evapotranspiration dataset for Great Britain.

## Method for deriving SPEI grids
- SPEI is computed from the cumulative CWB for each location, with accumulation ending in the target month (e.g., 6-month SPEI for July 1998 uses Feb–Jul 1998 CWB).
- For each grid cell, SPEI is calculated for all durations (1, 3, 6, 12, 18, 24 months) and all months (12×6 time series per location).
- Distribution fitting:
  - Primary: generalised logistic distribution (log-logistic) via the SCI R package.
  - Fitting process: maximum likelihood; if that fails, L-moments; if that fails, method of moments.
  - SPEI values are transformed to normal scores (mean 0, sd 1) with no units.
  - Truncation: SPEI values beyond ±5 are capped to that limit.
  - About 95% of SPEIs fall within -2 to +2; about 68% within -1 to +1.
- Serial/autocorrelation considerations:
  - For accumulation periods > 12 months, the underlying annual CWB series includes overlapping data, creating autocorrelation.
  - Monthly SPEIs and concatenated monthly series are likely autoregressive due to overlapping data; handle in trend analyses accordingly.

## Data Format and Access
- Format: NetCDF4, CEH gridded dataset conventions.
- Structure: two-dimensional spatial grids (Great Britain) with twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- Data scope: 1961–2012 (limited by CHESS PET and CEH-GEAR availability).
- Access: CEH-THREDDS-WATER server.

## Practical Considerations for Analysts
- Use across scales: 1 km for local analyses; 5 km for regional drought assessment and easier handling.
- Be mindful of autocorrelation and non-independence when performing frequency or trend analyses on SPEI time series.
- Choose accumulation period according to the drought signal of interest (short-term vs. long-term impacts).
- Interpretation hinges on "normal scores" with no units; relate to historical CWB distributions rather than physical units directly.
- Data derived under project DrIVER; ensure alignment with monitoring/early warning objectives and other impact datasets.

## Acknowledgments
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative, under the DrIVER project.

## References (key context)
- Vicente-Serrano et al. (2010a, 2010b, 2011, 2012, 2013) on SPEI development and applications.
- Stagge et al. (2015) on distributions for climax drought indices and related discussions.
- Fitting and methodological references for SPEI computation and distribution choices.
- CEH-GEAR and CHESS PET data sources underpinning the SPEI derivation.