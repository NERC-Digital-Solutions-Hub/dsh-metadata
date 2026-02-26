# Supporting information for: Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- Provides Grid-to-Grid (G2G) hydrological model outputs for Great Britain (GB) rivers driven by UKCP18 Regional (12km) projections.
- Outputs are on a 1km x 1km grid covering non-tidal rivers with catchments ≥50 km², for December 1980 to November 2080 (water years Oct-Sep; Dec-Nov for minima), under RCP8.5.
- Variables include monthly mean river flow, annual maxima of daily mean flow, and annual minima of 7-day mean flow, plus dates of extrema.

## Data content
- Grid-to-Grid river flow estimates driven by UKCP18 Regional data (12km PPE; 12 ensemble members). Outputs:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1) and dates of occurrence
  - Annual minima of 7-day mean river flow (m3 s-1) and dates of occurrence
- Spatial resolution: 1km x 1km grid across GB; domain size approximately 700 km x 1,000 km.
- Temporal coverage: 1980–2080 (with 30-day months and a 360-day calendar used in the climate model data).
- Only non-tidal river cells are included; missing values (-9999) used outside catchment criteria.

## Model and inputs
- Hydrological model: Grid-to-Grid (G2G), national-scale, 1km grid, 15-minute time-step; calibrated nationally, not per-catchment calibration.
- Inputs required: daily precipitation, daily potential evapotranspiration (PE), daily min/max temperature (for optional snow module).
- UKCP18 Regional (12km) projections provide the driving inputs, transformed to 1km grid through downscaling:
  - Precipitation: bias-corrected monthly factors, downscaled spatially and temporally
  - PE: derived via Penman-Monteith using updated stomatal resistance parameters
  - Temperature: downscaled with elevation-based lapse rate and diurnal sine-based temporal distribution
- Ensemble structure: 12 PPE members (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15); purpose is multi-model uncertainty representation.

## Data format and file structure
- Format: NetCDF4, one file per ensemble member and per variable, using CEH gridded dataset conventions.
- File naming:
  - Monthly mean flow: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual maxima: G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual minima: G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
- Spatial indexing: 700 km x 1,000 km GB domain; grid cell centers at (500,500) to (700000,1000000) in metres.
- Valid data: non-tidal river cells with catchment area ≥50 km²; other cells set to -9999.
- Time metadata:
  - Time units: days since 1900-01-01
  - Monthly values nominally assigned to first day of month
  - Annual maxima/minima assigned to start year of respective 12-month period
  - Dates of occurrence provided as days since 1900-01-01
- Auxiliary grids:
  - CatchmentAreaGrid.nc: catchment area (km²) draining to each 1km cell
  - NRFAStationIDGrid.nc and NRFAStationIDs.csv: estimated NRFA gauging station locations mapped to 1km grid cells

## Additional datasets and gauging information
- UKSCAPE_G2G_GB_CatchmentAreaGrid.nc: digitised catchment areas for GB at 1km resolution
- UKSCAPE_GB_NRFAStationIDGrid.nc: NRFA station locations aligned to 1km grid
- NRFAStationIDs.csv: accompanying station metadata; some stations provided as additional cells

## How to use the dataset
- Historical period: compare UKCP18-driven G2G outputs with outputs driven by observation-based inputs or observed river flow, using statistical comparisons over multi-decadal periods (not point-by-point time matching).
- Baseline vs future: assess potential climate-change impacts on river flows by statistical comparisons across the defined periods; ensure the same ensemble member is used for both periods.
- Ensemble usage: use the same ensemble member across periods to maintain consistency in comparison.
- Comparability: outputs are analogous to MaRIUS-G2G-WAH2-monthly datasets, enabling cross-dataset comparisons.

## Data provenance and caveats
- Model strengths: G2G is best for natural-flow-dominated catchments; performs less well in heavily managed or highly anthropogenically influenced regimes.
- Calendar and months: 30-day months and 360-day calendar reflect the driving climate model structure.
- Downscaling and bias correction: precipitation bias correction and downscaling to 1km introduce uncertainties; PE calculation follows established methods with historical stomatal resistance adjustments.
- Catchment discretisation: some smaller catchments may have discrepancies between observed NRFA catchments and discretised 1km grid catchments due to gridding.
- Calibration: site-specific calibration not performed; results are model-based estimates driven by climate projections.

## Access and acknowledgments
- Source: NERC Environmental Information Data Centre (UK-SCAPE project)
- Acknowledgements: UK-SCAPE programme and support from NERC award NE/R016429/1; contributors listed in the dataset description
- References: Bell et al. (2016, 2009, 2007, 2018), Kay et al. (2021), Lane & Kay (2021), and related methodological papers on UKCP18 and MaRIUS datasets