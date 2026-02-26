# Climate Change and Future Drought Projections

## Overview
- Study area: Mun River basin, Northeast Thailand.
- Time horizon: near-future period 2021–2050.
- Climate variables: projected maximum temperature, minimum temperature, and rainfall.
- Drought projections: meteorological (SPEI), hydrological (SRI), and agricultural (SSMI) droughts.
- Climate models and scenarios:
  - 14 CMIP5 models for RCP4.5 and RCP8.5.
  - 8 CMIP6 models for SSP5-8.5.
- Spatial resolution: 0.25-degree grid.
- Data access and processing: raw data from ESGF (Dec 2020), regridded to 0.25°, bias-corrected, and bias corrections explained below.
- Guidance and references: bias correction method based on Quantile Mapping; rainfall corrected via empirical distribution; temperature bias-corrected by normal distribution fitting. See Khadka et al. (2022) for details.

## Climate Data and Bias Correction
- Bias-correction approach:
  - Rainfall: empirical distribution to correct intensity and frequency; higher quantiles corrected for future values.
  - Temperature: fit to a normal distribution.
- Reference period for bias correction: 1981–2010.
- Output: bias-corrected near-future data available for 91 grids within the Mun basin.
- Data formats: baseline Observed values plus projections from multiple climate models; ensemble means provided.

## Drought Indices and Scenarios
- Drought indices and methodologies:
  - Meteorological drought: Standardized Precipitation Evapotranspiration Index (SPEI).
  - Hydrological drought: Standardized Runoff Index (SRI).
  - Agricultural drought: Standardized Soil Moisture Index (SSMI).
- Land-use scenarios (LUC) and climate scenarios:
  - Scenarios: CC_only (climate change only), CC+LUC_BAU (CC with BAU land-use), CC+LUC_CCU (CC with CCU land-use), LU_BAU_only, LU_CCU_only.
  - Five future cases: CC; LUC_BAU; LUC_CCU; CC+LUC_BAU; CC+LUC_CCU.
- Drought characteristics examined: duration, intensity, and severity.
- Temporal scales: 1-, 3-, 6-, and 12-month timescales.

## Datasets and File Structure
- Main datasets:
  - 1_MeteorologicalDroughts
  - 2_HydrologicalDroughts
  - 3_AgriculturalDroughts
  - 4_ETCCDI_ClimateExtremes
- Meteorological Droughts (1_MeteorologicalDroughts):
  - Subfolders by timescale: 1-month, 3-month, 6-month, 12-month.
  - Each timescale contains duration, intensity, and severity CSV files.
- Hydrological Droughts (2_HydrologicalDroughts):
  - Subfolders for CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only.
  - Within each: 1-, 3-, 6-, 12-month timescales with duration, intensity, severity CSV files.
- Agricultural Droughts (3_AgriculturalDroughts):
  - Same folder structure as Hydrological Droughts (CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only).
  - Timescales and CSVs as above.
- Climate extremes (4_ETCCDI_ClimateExtremes):
  - Indices folders: CDD, CWD, R20, R40, R95p, R99p, RX1day, RX5day, SDII, TX90p, TXx, TN90p, TNx, WSDI.
  - Each index contains three CSVs: CMIP5-RCP45, CMIP5-RCP85, CMIP6-SSP5-85.
- CSV format (common across datasets):
  - 13 columns: grid_ID, lat, lon, Observed (baseline), columns 5–12 with projections from 8 CMIP6 models, last column as ensemble average.
  - All files include observed baseline data plus multi-model projections and ensemble mean.

## What This Enables for Analysis
- Model comparison and ensemble synthesis across CMIP5 and CMIP6 under multiple scenarios.
- Correlation analyses between climate projections, drought indices, and extreme indices.
- Spatial risk assessment and trend analysis for drought types and timescales.
- Scenario planning by contrasting CC_only, LUC variants, and combined CC+LUC scenarios.
- Development of predictive models and data-driven decision support for water resources and agriculture in the Mun River basin.
- Data provenance and reuse: grid IDs, coordinates, baseline observations, and model ensembles documented; metadata and sources trackable.

## Important References and Notes
- Bias correction methodology and near-future projections: Khadka et al. 2022 (Int J. Climatol.).
- Land-use scenarios details: Penny, Djordjević, Chen 2021 (Environ Res Lett).
- ETCCDI climate extremes definitions and indices documentation: Karl et al. 1999 (Climh Change workshop summary).