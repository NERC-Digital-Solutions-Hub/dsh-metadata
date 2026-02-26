# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by observed data (1980 to 2011)

## Overview for Analysts Monitoring the Environment
- Provides Grid-to-Grid (G2G) hydrological model outputs of natural river flows for Northern Ireland (NI) at 1 km x 1 km resolution.
- Outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow, for water years October–September and December–November as appropriate.
- Datasets support monitoring water quantity under observed meteorological forcing (1980–2011) and can be used alongside projection-driven datasets for comparative analysis.

## What’s in the Dataset
- Monthly mean river flow (m3 s-1) for NI on a 1 km x 1 km grid.
- Annual maxima of daily mean river flow (m3 s-1) for NI on a 1 km x 1 km grid.
- Annual minima of 7-day mean river flow (m3 s-1) for NI on a 1 km x 1 km grid.
- Coverage on a 187 km x 170 km domain aligned with the GB National Grid; non-tidal river cells with catchment area ≥ 50 km² are included; others are set to missing.
- Time period: 1980–2011 (with monthly and annual summaries).
- A complementary dataset provides G2G estimates for NI driven by UKCP18 Regional (12 km) climate projections.
- Additional spatial datasets:
  - Digitally-derived catchment areas on a 1 km x 1 km grid.
  - 1 km x 1 km grid identifying majority lake cells.
  - Estimated locations of flow gauging stations on the 1 km x 1 km grid, with station information.

## Hydrological Model: Grid-to-Grid (G2G) Overview
- A national-scale grid-based hydrological model operating typically at 1 km x 1 km with ~15-minute time steps.
- Configured for NI and parts of the Republic of Ireland that drain to NI rivers.
- Outputs gridded, natural river flow estimates for gauged and ungauged rivers; calibration is not performed at the catchment level (uses nationally applicable values).
- Urban/suburban land cover effects on runoff are represented within the model.
- Known performance: generally good for catchments with natural flow regimes; limitations where artificial abstractions/discharges are strong or complex sub-surface hydrology exists (notably flows downstream of Lough Neagh).
- Lake/reservoir storage effects on downstream flows are not accounted for; lakes are treated as rivers in grid cells where applicable.

## Input Data and Processing
- Meteorological inputs:
  - Daily precipitation at 1 km (CEH-GEAR).
  - Monthly evaporation (PE) for short grass (MORECS).
  - Daily min/max temperature at 1 km (Met Office).
- Data processing steps:
  - Precipitation and PE data re-projected to the 1 km GB national grid.
  - Precipitation distributed uniformly across daily model time steps; PE distributed across monthly steps.
  - Temperature downscaled within day using a sine curve.
  - Where PE/temperature data are incomplete, gaps are infilled.
- Supporting spatial data: topography and soil data consistent with Bell et al. (2009).

## Format and File Structure
- Gridded data stored as NetCDF4 files, one file per variable, following CEH conventions.
- Example file names:
  - Monthly mean river flow: G2G_NI_mmflow_obs_1980_2011.nc (Dec 1980–Nov 2011)
  - Annual maxima of daily mean river flow: G2G_NI_amaxflow_obs_1980_2011.nc (Oct 1981–Sep 2011)
  - Annual minima of 7-day mean river flow: G2G_NI_aminflow_obs_1980_2011.nc (Dec 1980–Nov 2011)
- Domain: NI on GB National Grid, 187 km x 170 km, with grid cell centers representing values; non-tidal rivers with catchment area ≥ 50 km² are included; missing values are -9999.
- Time stamps:
  - Monthly flows: days since 1900-01-01; monthly values assigned to the first day of the month.
  - Annual maxima/minima: assigned to the start year of the 12-month period.
- Supporting datasets:
  - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc: catchment areas (km²) draining to each 1 km grid box.
  - UKSCAPE_G2G_NI_LakeGrid.nc: majority lake cells (binary grid; land=1, lake=2, sea=-9999).
  - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv: best NI NRFA gauging station locations mapped to 1 km grid cells.

## Using the Data for Environmental Monitoring
- Compare G2G-derived flows with observed NRFA river flows to assess model performance and detect changes in water quantity.
- Use alongside the UKCP18 Regional (12 km) climate projection-driven G2G dataset for scenario analysis and trend assessment.
- Note model limitations:
  - Does not account for lake/reservoir storage impacts on downstream flows; lake grid cells are treated as rivers.
  - Some discrepancies can occur in small catchments due to discretisation to 1 km grid and potential mismatches with observed catchment areas.
  - Calibration at the catchment level is not performed; results rely on globally applicable parameters.

## Acknowledgements and References
- Funded by Natural Environment Research Council under award NE/R016429/1 (UK-SCAPE programme).
- Acknowledgements to named contributors for guidance.
- Key references include Bell et al. (2009, 2016), Kay et al. (2021), Rudd et al. (2017), and supporting datasets such as CEH-GEAR and Land Cover Map 2015.