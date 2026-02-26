# Climate Change and Future Drought Projections

## Overview
- Near-future climate projections (2021–2050) for the Mun River basin, Northeast Thailand.
- Based on 14 CMIP5 models (RCP4.5 and RCP8.5) and 8 CMIP6 models (SSP5-8.5) with 0.25-degree resolution.
- Raw data from the Earth System Grid Federation (ESGF) portal, December 2020; data re-gridded to 0.25° and bias-corrected.
- Bias correction: rainfall via empirical distribution (quantile mapping) to 1981–2010; temperatures fit to normal distribution.
- Projections cover meteorological, hydrological, and agricultural droughts using standardized indices; 5 land-use scenarios with two drivers:
  - Land-use change (LUC): BAU or CCU (Forest Conservation and Urban Growth)
  - Land-use scenarios: BAU, CCU
- Five future cases: CC only (CC), LUC_BAU, LUC_CCU, CC+LUC_BAU, CC+LUC_CCU.
- Data organized into four categories: Meteorological Droughts, Hydrological Droughts, Agricultural Droughts, and Climate Extremes (ETCCDI).

## Data and Methods

- Data sources and processing
  - ESGF climate model outputs (CMIP5 and CMIP6) for near-future projections.
  - Spatial resolution after processing: 0.25 degrees.
  - Bias correction applied before use; rainfall bias-corrected with empirical distribution; temperature bias-corrected to normal distribution.
  - 91 grids used for bias-corrected rainfall and temperature in the near-future.
- Drought indicators
  - Meteorological drought: Standardized Precipitation Evapotranspiration Index (SPEI).
  - Hydrological drought: Standardized Runoff Index (SRI).
  - Agricultural drought: Standardized Soil Moisture Index (SSMI).
- Drought assessment references provided for methodology details.

## Drought Data Content by Category

- 1_MeteorologicalDroughts
  - Timescales: 1-month, 3-month, 6-month, 12-month.
  - For each timescale: files for duration, intensity, and severity.
  - File structure example: 1-month_duration.csv, 1-month_intensity.csv, 1-month_severity.csv, etc.
  - CSVs have 13 columns: grid_ID, lat, lon, Observed, eight CMIP6 model projections, and ensemble average.
- 2_HydrologicalDroughts
  - Land-use scenarios: CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only.
  - Within each scenario: 1-, 3-, 6-, and 12-month timescales.
  - Each timescale includes duration, intensity, and severity CSVs.
  - All CSVs follow the same 13-column structure as Meteorological Droughts.
- 3_AgriculturalDroughts
  - Same structure as Hydrological Droughts with CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only.
  - Timescales: 1-, 3-, 6-, 12-month; each with duration, intensity, and severity CSVs.
  - 13-column format consistent with other drought datasets.
- 4_ETCCDI_ClimateExtremes
  - Climate indices folders: CDD, CWD, R20, R40, R95p, R99p, RX1day, RX5day, SDII, TX90p, TXx, TN90p, TNx, WSDI.
  - Each index contains three CSVs: CMIP5-RCP45, CMIP5-RCP85, CMIP6-SSP5-85.
  - CSV format includes: lat, lon, grid_ID, Observed, model projections, and ensemble average.
  - Indices defined with units (e.g., TXx in °C, RX1day in mm) and descriptions provided in documentation.

## Data Structure and Access

- File organization follows a consistent hierarchical directory structure per category and scenario.
- All drought-related CSVs contain 13 columns and grid-level data (grid_ID, lat, lon) plus Observed and model projections.
- Projections are available per model and as an ensemble average to support multi-model assessment.
- Data are prepared for integration into standard environmental monitoring workflows and dashboards.

## Purpose for Analysts

- Produces time-consistent indicators of environmental health and drought risk under multiple climate and land-use futures.
- Enables standardised assessment of policy performance over time and across scenarios.
- Facilitates merging with other datasets to enhance value beyond single-use analyses.
- Supports accessibility of underlying data via structured datasets and clearly defined metadata.