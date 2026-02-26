# Supporting Information

- This document describes a dataset of 1 km and 5 km gridded Standardised Precipitation-Evapotranspiration Index (SPEI) for Great Britain, a drought index based on climatic water balance (precipitation minus evapotranspiration) over various accumulation periods.

## I. Brief Description of the dataset
- Gridded SPEI data at 1 km and 5 km resolutions for Great Britain.
- SPEI computed for accumulation periods: 1, 3, 6, 12, 18, 24 months; calculated for each of the 12 calendar months.
- Data are autocorrelated in monthly and longer series due to accumulation and standardisation processes.
- Fitted distribution: generalised logistic (log-logistic) distribution using a standardisation period 1961–2010.
- Dataset covers 1961–2012; produced from CHESS PET (potential evapotranspiration) and CEH-GEAR rainfall data; stored as NetCDF4 on the CEH-THREDDS-WATER server.

## II. Motivation
- Part of the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) focusing on drought indices within monitoring and early warning systems.
- SPEI incorporates evapotranspiration, unlike SPI, enabling assessment of water surplus/deficit and drought rarity across time scales.
- Applications include drought variability/reconstruction, climate-change context, hydrological/agricultural/ecological impacts, and drought monitoring systems.
- SPEI time scales provide different information:
  - 1-month: short-term soil moisture/crop stress.
  - 3-month: short- to medium-term moisture/seasonal CWB.
  - 6-month: medium-term CWB trends, potential links to streamflow/reservoirs.
  - 12-month: long-term CWB patterns (link to streamflow/reservoirs).
  - 18–24-month: very long-term CWB and potential groundwater signals.
- Rationale for two resolutions: 1 km for detailed local analyses; 5 km for regional studies with smaller file sizes and faster loading.
- Data provenance: CEH-GEAR rainfall estimates and CHESS PET dataset.

## III.1 Data Sources
- CEH-GEAR: Gridded daily/monthly areal rainfall (UK, for hydrological use).
- CHESS PET: Potential evapotranspiration dataset.

## III.2 Method for deriving the SPEI grids
- SPEI defined from the cumulative probability of observed Climatic Water Balance (CWB) for each location.
- For each location, SPEI is computed for durations (1, 3, 6, 12, 18, 24 months) and for each calendar month (72 time series per location).
- Distribution fitting: generalised logistic distribution (log-logistic) fitted to historic CWB accumulations; alternatives like GEV discussed but not used due to tail behavior and fitting robustness for this context.
- Parameter estimation via R package SCI (maximum likelihood; L-moments fallback; method of moments as last resort).
- SPEI normalization: transform to normal scores (mean 0, sd 1); units removed; values truncated at ±5 to avoid extremes.
- Typical range: ~95% of SPEIs within -2 to 2; ~68% within -1 to 1.
- Temporal considerations:
  - Longer durations (>12 months) use overlapping data, creating autocorrelation in the underlying series; impacts independence assumptions in frequency analysis.
  - Concatenated monthly SPEI series (for trend analyses) are also autocorrelated due to data overlap; must account for serial correlation in analyses.
- Timeframe: standard fitting period 1961–2010; dataset extends to 2012 due to data availability.

## IV. Format of the SPEI dataset
- File format: NetCDF4 following CEH gridded dataset conventions.
- Structure: two-dimensional GB spatial grids; twelve monthly grids per year; one file per accumulation period.
- Projection: British National Grid.
- Values: SPEI as normal scores (unitless) within -5 to 5.
- Access: CEH-THREDDS-WATER server.

## V. Acknowledgments
- Output of the DrIVER project; funding from the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

- Note: The dataset builds on numerous cited studies regarding SPEI methodology and drought indices, including Vicente-Serrano et al. (2010a) for SPEI definition and distribution fitting considerations.