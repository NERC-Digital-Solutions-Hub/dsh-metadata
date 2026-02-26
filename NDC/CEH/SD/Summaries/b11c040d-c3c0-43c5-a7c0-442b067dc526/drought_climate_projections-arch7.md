# Climate Change and Future Drought Projections

## Overview
- Spatial focus: Mun River basin, Northeast Thailand
- Timeframe: near-future period 2021–2050
- Climate variables: projected maximum/minimum temperature and rainfall
- Spatial resolution: 0.25-degree grids; bias-corrected data available for 91 grids
- Baseline and projections: Observed baseline (1981–2010) with future projections

## Modeling and Scenarios
- Climate models:
  - 14 CMIP5 models for RCP4.5 and RCP8.5
  - 8 CMIP6 models for SSP5-8.5
- Data processing:
  - Re-gridded to 0.25 degrees (bilinear interpolation)
  - Bias correction:
    - Rainfall: quantile mapping using reference period observations
    - Temperature: normal distribution fitting
- Future case scenarios (5 total):
  - CC only
  - LUC_BAU
  - LUC_CCU
  - CC + LUC_BAU
  - CC + LUC_CCU

## Drought Indices and Types
- Drought types and indices:
  - Meteorological drought: SPEI
  - Hydrological drought: SRI
  - Agricultural drought: SSMI
- Agricultural and Hydrological droughts assessed under land-use change (LUC) scenarios:
  - BAU and CCU combinations
- ETCCDI climate extremes:
  - Indices and definitions summarized in accompanying table

## Data Organization and Files
- Datasets organized into four main folders:
  - 1_MeteorologicalDroughts
    - Subfolders: 1-, 3-, 6-, 12-month timescales
    - Files: duration, intensity, severity (CSV) for each timescale
  - 2_HydrologicalDroughts
    - Subfolders by scenario: CC_only, CC+LUC_BAU, CC+LUC_CCU, LU_BAU_only, LU_CCU_only
    - Each with 1-, 3-, 6-, 12-month timescales
    - Files: duration, intensity, severity (CSV) for each timescale
  - 3_AgriculturalDroughts
    - Similar structure to Hydrological folder with comparable timescales and metrics
  - 4_ETCCDI_ClimateExtremes
    - Indices folders: CDD, CWD, R20, R40, R95p, R99p, RX1day, RX5day, SDII, TX90p, TXx, TN90p, TNx, WSDI
    - Each index contains three CSVs: CMIP5-RCP45, CMIP5-RCP85, CMIP6-SSP5-85
- CSV structure (common to all files):
  - 13 columns total
  - Column 1: grid_ID
  - Column 2: lat
  - Column 3: lon
  - Column 4: Observed (baseline)
  - Columns 5–12: projections from climate models
  - Column 13: ensemble (average of models)

## GIS-ready Attributes and Schema
- Spatial attributes:
  - Each CSV provides grid_ID with corresponding lat/lon
  - Observed baseline and multi-model projections per grid
- Data compatibility:
  - Consistent 0.25-degree grid spacing for climate data
  - Per-grid drought characteristics (duration, intensity, severity) across timescales
  - ETCCDI indices available for spatial visualization of extremes

## Usage and Applications for GIS Work
- Visualization:
  - Map drought duration, intensity, and severity across the Mun River basin
  - Compare CC vs. LUC scenarios and BAU vs. CCU combinations
  - Visualize climate extremes (ETCCDI indices) spatially
- Analysis:
  - Multi-model ensemble comparisons by scenario and timescale
  - Assess impacts of land-use changes on drought metrics
  - Integrate with other GIS layers (hydrology, land cover, infrastructure) for decision support
- Data handling considerations:
  - Manage multi-folder dataset with consistent coordinate reference system
  - Validate bias-corrected fields against baseline observations
  - Prepare aggregated or regional summaries (e.g., basin-wide metrics)

## References and Notes
- Methodology and data sources referenced in Khadka et al. (2022) and Khadka et al. (2021)
- Land-use scenarios and methodological details discussed in Penny et al. (2021)
- ETCCDI index definitions and usage aligned with established climate-extremes literature (Karl et al., 1999)