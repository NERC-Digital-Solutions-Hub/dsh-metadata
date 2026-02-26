# Climate Change and Future Drought Projections

## Overview
- Provides future climate projections for the Mun River basin, Northeast Thailand, focusing on near-future period 2021–2050.
- Variables: maximum temperature (Tmax), minimum temperature (Tmin), and rainfall.
- Model ensembles and scenarios:
  - 14 CMIP5 models for two scenarios: RCP4.5 and RCP8.5.
  - 8 CMIP6 models for SSP5-8.5.
- Spatial resolution: 0.25-degree grids.
- Raw data from Earth System Grid Federation (ESGF) accessed December 2020; data regridded (bilinear interpolation) and bias-corrected.
- Bias correction:
  - Rainfall: empirical distribution (no distribution fitting); corrects intensity and frequency; high quantile correction for future rainfall.
  - Temperature: normal distribution fitting.
- Baseline reference: 1981–2010 observations; post-correction data available in 91 grids covering Mun River basin.
- Outputs include projections of meteorological, hydrological, and agricultural droughts under multiple land-use change (LUC) scenarios.

## Data Sources and Processing
- Data provenance: ESGF portal (Dec 2020).
- Spatial and statistical adjustments:
  - Re-gridding to 0.25-degree grids.
  - Bias correction using Quantile Mapping (rainfall and temperature).
- Drought indices and scenarios:
  - Meteorological drought: SPEI (Standardized Precipitation Evapotranspiration Index).
  - Hydrological drought: SRI (Standardized Runoff Index).
  - Agricultural drought: SSMI (Standardized Soil Moisture Index).
  - Land-use change scenarios: BAU (Business As Usual) and CCU (Forest Conservation and Urban Growth); case sets include CC, LUC_BAU, LUC_CCU, CC+LUC_BAU, CC+LUC_CCU.
- References for methods:
  - Khadka et al. (2022) for near-future climate projections and bias correction details.
  - Penny et al. (2021) and related works for land-use change scenarios.
- Units:
  - Rainfall: mm.
  - Temperatures: degree Celsius.

## Drought Projection Datasets

### 1) MeteorologicalDroughts
- Structure: 4 timescales folders (1-month, 3-month, 6-month, 12-month).
- Each timescale contains three drought characteristics: duration, intensity, severity.
- File format: CSV with 13 columns (grid_ID, lat, lon, Observed, projections from 8 CMIP6 models, and ensemble mean).
- File organization example:
  - 1_MeteorologicalDroughts/1-month_timescale/1-month_duration.csv
  - 1_MeteorologicalDroughts/1-month_timescale/1-month_intensity.csv
  - 1_MeteorologicalDroughts/1-month_timescale/1-month_severity.csv
  - ... similarly for 3-, 6-, and 12-month timescales.

### 2) HydrologicalDroughts
- Structure: top-level folders by scenario combinations:
  - CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only.
- Each scenario folder contains 4 timescales (1-, 3-, 6-, 12-month).
- Each timescale contains three drought characteristics: duration, intensity, severity.
- File organization mirrors MeteorologicalDroughts with 13-column CSVs.

### 3) AgriculturalDroughts
- Structure mirrors HydrologicalDroughts (CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only).
- Each timescale (1-, 3-, 6-, 12-month) includes duration, intensity, severity CSVs (13-column format).

### 4) ETCCDI_ClimateExtremes
- Content: Future climate extreme indices (ETCCDI) with indices:
  CDD, CWD, R20, R40, R95p, R99p, RX1day, RX5day, SDII, TX90p, TXx, TN90p, TNx, WSDI.
- Each index folder contains three CSV files:
  - CMIP5-RCP45, CMIP5-RCP85, CMIP6-SSP5-85.
- File format: CSV with columns:
  - lat, lon, grid_ID, Observed, projections from climate models, ensemble average.
- Table 1 provides the definitions and units for each index (e.g., TXx in °C, RX1day in mm, CDD in days, etc.).

## Model Ensembles, Scenarios, and Temporal Coverage
- CMIP5 models:
  - 14 models for RCP4.5 and RCP8.5.
- CMIP6 models:
  - 8 models for SSP5-8.5.
- Temporal focus: near-future period 2021–2050.
- Outputs span meteorological, hydrological, agricultural droughts, and climate extremes under multiple CC/LUC scenarios.

## File Organization and Access
- All drought-related CSV files share a consistent 13-column schema:
  - Column 1: grid_ID
  - Column 2: lat
  - Column 3: lon
  - Column 4: Observed (baseline period)
  - Columns 5–12: projections from 8 CMIP models
  - Column 13: ensemble (average of model projections)

## References and Notes
- Bias correction and methodology:
  - Khadka, D. et al. (2022): details on projected changes in near-future climate and extremes for northeast Thailand.
- ETCCDI indices:
  - Karl, T.R. et al. (1999): baseline for ETCCDI definitions and indices.