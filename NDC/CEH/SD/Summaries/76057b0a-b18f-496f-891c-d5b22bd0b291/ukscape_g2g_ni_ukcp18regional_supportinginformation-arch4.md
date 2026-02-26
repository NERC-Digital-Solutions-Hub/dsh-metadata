# Supporting information for: Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2

## Data access and citation information
- Data are available under the Open Government Licence v3.
- Access via https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291.
- When using the data, cite:
  Kay, A.L.; Rudd, A.C.; Davies, H.N.; Lane, R.A.; Bell, V.A. (2022). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291.

## Brief summary of the dataset
- UK-SCAPE program research into climate change impacts on water quantity across Britain; this dataset provides Grid-to-Grid (G2G) hydrological model estimates for Northern Ireland (NI) on a 1km x 1km grid.
- Outputs include:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
  - For non-sea, non-tidal 1km grid boxes with catchment area >= 50 km2
  - Time period: December 1980 to November 2080
  - Driving data: UKCP18 Regional (12km) projections, 12-member perturbed parameter ensemble (PPE), RCP8.5
- NI-specific outputs driven by 12km UKCP18 data; additional complementary NI datasets exist for observation-based driving data.
- Supporting spatial datasets included: catchment areas, majority lake cells, and locations of flow gauging stations on a 1km grid.

## Hydrological model - Grid-to-Grid (G2G)
- National-scale hydrological model calibrated to produce gridded river-flow estimates at 1km x 1km resolution with a 15-minute time-step.
- Configured for NI and adjacent catchments draining to NI rivers; outputs for gauged and ungauged rivers.
- Calibration approach uses nationally applicable parameter values rather than catchment-specific calibration.
- Urban land cover effects accounted for via generalized runoff formulation; model performance is better in natural-flow regimes and where systems are less influenced by abstractions/discharges.
- Preliminary NI assessment shows generally good performance, with lower accuracy downstream of Lough Neagh due to flood regulation.

## G2G model input data
- Meteorological inputs derived from UKCP18 Regional projections (12km grid), including daily precipitation, daily min/max temperature, and daily potential evapotranspiration (PE) derived from other vars.
- Ensemble: 12 PPE members from the Hadley Centre Regional Climate Model (RCM) for 1980-2080 under RCP8.5.
- Downscaling and bias correction:
  - Precipitation: bias-corrected with monthly multiplicative factors; downscaled to 1km using spatial weighting; temporally distributed evenly across model time-steps.
  - PE: downscaled to 1km and allocated evenly across time-steps; PE derived to mirror MORECS methodology with adjustments for future CO2 effects on stomatal resistance.
  - Temperature: 1km downscaling using elevation-based lapse rates; diurnal cycling via sine curve.
- Model domain and supporting data:
  - Spatial data (topography, soils) aligned with Bell et al. (2009).
  - 360-day calendar used by the underlying climate model; 30-day months in data files.

## How to use the dataset
- Historical period comparisons:
  - Compare G2G outputs driven by UKCP18 with those driven by observation-based inputs or observed river flow for statistical assessments over multi-decadal periods (not point-by-point date-for-date comparisons).
- Baseline vs future comparisons:
  - Use ensemble member consistency: compare baseline and future periods using the same ensemble member (e.g., 01 with baseline and future, not 01 with baseline and 04 with future).
- Important caveats:
  - Lake and reservoir effects are not modeled; lake cells are treated as river cells, potentially influencing downstream flows.
  - Some catchments may show discrepancies due to discretization at 1km resolution; NRFA gauging station matching is approximated with checks.
- Outputs and usage:
  - Data provided as NetCDF4 files, one file per ensemble member and variable.
  - File naming conventions indicate data type (mmflow, amaxflow, aminflow), ensemble number, and period coverage (1980-2080).
  - Time stamps use 'days since 1900-01-01' with monthly flows assigned to the first of the month; annual maxima/minima correspond to specific 12-month periods (water years or Dec-Nov years).

## Format of the gridded datasets
- Domain: NI on a 1km x 1km grid within a GB National Grid extent; non-tidal river cells with catchment area >= 50 km2 are populated; others are missing (-9999).
- Temporal characteristics: 30-day months due to the 360-day calendar of the climate model; monthly data assigned to first day of the month.
- File structure:
  - NetCDF4 files per ensemble and variable:
    - G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc — monthly mean river flow
    - G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc — annual maxima of daily mean river flow (with dates of occurrence)
    - G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc — annual minima of 7-day mean river flow (with dates of occurrence)
  - ensnum values correspond to ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15.
- Supporting files:
  - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc — catchment area per 1km cell
  - UKSCAPE_G2G_NI_LakeGrid.nc — majority lake cells (>70% water)
  - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv — NRFA gauging station locations and IDs

## Supporting datasets and references
- Additional datasets for interpretation:
  - Digitally-derived catchment areas, lake cell grids, and NRFA station locations to aid result interpretation and validation.
- Acknowledgements:
  - Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability.
  - Appreciations to individuals for advice.

## Data governance and provenance considerations for Data Leaders
- Licensing and citation:
  - Open Government Licence v3; requires proper citation as specified.
- Provenance and versioning:
  - NI-focused 1km dataset derived from 12km UKCP18 PPE projections, with clearly defined ensemble members and period coverage.
- Data quality and limitations:
  - Model limitations in regions affected by artificial regulation (e.g., near Lough Neagh) and potential catchment discretization errors at 1km resolution.
  Recommends statistical rather than point-by-point comparisons when aligning with observed data.
- Discoverability and interoperability:
  - Data organized with consistent NetCDF4 conventions; accompanying metadata and supporting grids enhance discoverability and cross-dataset analysis.
- Collaboration potential:
  - Facilitates cross-network climate impact assessments and supports governance of data products used for policy and planning related to river flow under climate change.