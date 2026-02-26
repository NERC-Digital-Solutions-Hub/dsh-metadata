# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-monthly]

## Overview
- MaRIUS project (2014–2017) developed a risk-based approach to drought and water scarcity.
- Provides Grid-to-Grid (G2G) model outputs on a 1 km x 1 km grid across Great Britain for two key hydrological variables: river flow (m3 s-1) and soil moisture (mm water/m soil), as monthly means.
- Time periods: Historical Baseline (1900–2006), Baseline (1975–2004), Near-Future (2020–2049), Far-Future (2070–2099).
- 100 ensemble members per period; driving data come from weather@home2 (WAH2) regional climate model ensembles.
- Additional spatial datasets included: digitally-derived catchment areas and estimated NRFA gauging station locations.

## Model and outputs
- Model: Grid-to-Grid (G2G) is a national-scale, 1 km grid hydrological model with 15-minute time-steps; parameterised largely from spatial datasets (e.g., soils, land cover) and accounts for urban land-cover effects on runoff. Generally not calibrated per catchment; focuses on natural flow regimes.
- Inputs: daily precipitation and potential evaporation (PE). Snow module not used (assumes rain). Calibration is not performed per catchment.
- Temporal and spatial resolution: 1 km x 1 km grid, 15-minute time-step; outputs are monthly means of daily values (flow in m3 s-1; soil moisture in mm water/m soil).
- Periods and ensembles: 100 G2G simulations for HISTBS (1900–2006), BS (1975–2004), NF (2020–2049), and FF (2070–2099).
- Calendar: 360-day year; months are 30 days (affecting time references and spin-up handling).

## Driving data and processing
- Driving data: MaRIUS weather@home2 (WAH2) climate data (HadRM3P nested in HadAM3P) with bias-corrected precipitation and Penman-Monteith PE.
- Future PE: two variants; this dataset uses the adjusted stomatal resistance version, which moderates projected low-flow declines.
- Reprojection and weighting: WAH2 data re-projected from ~25 km to 1 km G2G grid; within each coarse cell, non-uniform precipitation distribution is assigned using spatial weights based on average rainfall patterns.
- Spin-up considerations: first two years of HISTBS, NF, and FF should be ignored for analyses or used solely for model spin-up.

## Data structure and access
- Output format: NetCDF4, one file per period and ensemble member; file naming: G2G_WAH_var_<period>*<ensemble>.nc (e.g., HISTBS*, BS*, NF*, FF*).
- Domain: 700 km x 1000 km GB extent; values defined for land grid boxes; sea points set to missing (-9999).
- Versioned ancillary datasets:
  - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment area (km2) for each 1 km grid cell.
  - MaRIUS_G2G_NRFAStationIDGrid.nc and MaRIUS_NRFAStationIDs.csv: NRFA gauging station locations mapped to the 1 km grid (1285 stations; 260 with daily time series).

## Data interpretation and usage guidance
- Comparisons to observations:
  - Can be compared to observation-driven G2G runs or NRFA data, but only statistically over multi-decadal periods; do not expect exact time-series matches (e.g., 1976).
  - Differences indicate biases in driving data (WAH2) or model structure, not exact historical replication.
- Future-period analyses:
  - Compare NF/FF outputs to the BS baseline, not to observed time series.
  - Impacts models (economic, ecological, agricultural) should be compared against BS outputs rather than observed outcomes.
- Ensemble interpretation:
  - Treat each ensemble member as a plausible realization; analyze differences between historical and future distributions rather than chasing single-member changes.
  - Ensemble members with the same index across periods are not directly related and should not be compared (e.g., BS1 vs NF1).
- Data caveats:
  - G2G does not include abstractions or discharges; no catchment-specific calibration.
  - Bias correction applies to precipitation; PE for future periods uses adjusted stomatal resistance values.
  - 360-day calendar yields 30-day months; spin-up years should be excluded from primary analyses.
  - NRFA-based catchment representations on the 1 km grid may not perfectly match observed NRFA catchments due to discretisation.

## Practical notes for analysts
- Key metrics: monthly means of flow (m3 s-1) and soil moisture (mm water/m soil) on a 1 km grid; supplementary spatial data for catchments and gauging stations.
- Data provenance and usage are designed to support drought/water-scarcity risk assessment and scenario planning for policy and research.
- Dataset acknowledged to be an outcome of the MaRIUS project, funded by the UK Natural Environment Research Council (NE/L010208/1).

## References (selected)
- Foundational model and data papers on G2G, soil data, and drought analyses (Bell et al.; Kay et al.; Rudd et al.; Guillod et al.; Monteith; Hough & Jones).
- Related works on low-flow frequency, drought risk, and hydro-meteorological time series generation.