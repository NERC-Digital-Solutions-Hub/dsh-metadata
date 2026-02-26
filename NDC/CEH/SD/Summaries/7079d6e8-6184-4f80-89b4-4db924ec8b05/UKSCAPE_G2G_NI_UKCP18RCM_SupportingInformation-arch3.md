# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Summary
- Provides Grid-to-Grid (G2G) hydrological model outputs for Northern Ireland (NI) driven by UKCP18 Regional projections (1980–2080, 12km driver, 12 PPE members, RCP8.5).
- Outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow on a 1km x 1km grid over NI; data support comparisons to observations or alternative drivers in a statistical sense (not point-by-point).
- Additional supporting spatial datasets accompany the main outputs (catchment areas, majority-lake cells, and estimated NRFA gauging station locations).

## Data accessibility and citation
- Open Government Licence: data accessible at the specified DOI.
- Primary citation required when using the dataset: Kay et al. (2021) NERC EDS Environmental Information Data Centre dataset.
- Acknowledges NERC UK-SCAPE programme and associated researchers.

## What the dataset contains
- Grid-to-Grid river flow estimates for NI:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1) with dates of occurrence
  - Annual minima of 7-day mean river flow (m3 s-1) with dates of occurrence
  - Outputs on a 1km x 1km grid for non-tidal river cells with catchment area ≥ 50 km2
  - Time period: December 1980 to November 2080; 30-day months (360-day calendar)
  - NI spatial domain on the GB National Grid (187 km x 170 km)
  - Ensemble members: 12 PPE members (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15)
- Auxiliary spatial datasets:
  - Digitally-derived catchment area (km2) draining to each 1km cell
  - 1km grid identifying majority lake cells
  - Estimated locations of NRFA river flow gauging stations (1km grid and CSV with NRFA IDs)

## Model and inputs
- Grid-to-Grid (G2G) hydrological model:
  - National-scale, 1km x 1km grid; 15-minute time-step
  - Configured to NI (and some cross-border catchments) aligned with GB grid
  - Outputs natural river flows for gauged and ungauged rivers; no calibration per catchment
  - Urban/suburban land cover effects included via parameterization of runoff
- Forcing data and downscaling:
  - UKCP18 Regional projections (12km grid) for daily precipitation, daily min/max temperature, and daily potential evapotranspiration (PE)
  - 12 PPE ensemble members for Dec 1980–Nov 2080 under RCP8.5
  - Bias correction applied to precipitation (monthly multiplicative factors)
  - PE derived via Penman-Monteith, with stomatal resistance adjustments for future CO2
  - 12km outputs downscaled to 1km using spatial weighting; daily PE downscaled to 1km; temperature downscaled using elevation-based lapse rates and diurnal sine curves
- Model limitations:
  - Lake and reservoir storage not accounted; lake cells treated as rivers (affects downstream flows, notably near Lough Neagh and Lough Erne)
  - NRFA gauging station locations approximated on a 1km grid; some catchment area discrepancies may occur for small basins
  - 360-day calendar (three 30-day months) used in climate driver data

## Data format and structure
- NetCDF4 format for each ensemble member and variable:
  - Monthly mean river flow: G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual maxima of daily mean river flow: G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual minima of 7-day mean river flow: G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc
- Spatial and temporal details:
  - NI domain: 187 km x 170 km on GB National Grid; 1km grid cells; non-tidal river cells with catchment area ≥ 50 km2
  - Time stamps: days since 1900-01-01; monthly means assigned to month-start; annual min/max assigned to start year of 12-month period
  - Missing values: -9999
  - 30-day months due to 360-day calendar used by driving climate model
- Ancillary datasets:
  - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc
  - UKSCAPE_G2G_NI_LakeGrid.nc
  - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv

## How to use the dataset
- Historical comparisons:
  - Compare G2G outputs (driven by UKCP18) with those driven by observation-based inputs or observed river flow, using statistical comparisons over multi-decadal periods rather than point-by-point time matching
- Baseline vs future analysis:
  - Use the same ensemble member to compare across periods to assess potential climate-change impacts on river flows
- Caution on interpretation:
  - Do not attempt exact temporal point-wise matches between observed weather and PPE dates
  - Consider the non-accounted effects of lakes/reservoirs when interpreting downstream flow changes
- Data access notes:
  - The 12 PPE ensemble members correspond to driving GCM PPE members; ensure consistency when aggregating or comparing periods

## Usage guidance for monitoring frameworks
- This dataset demonstrates key monitoring considerations:
  - Availability of high-resolution, openly accessible climate-driven hydrological outputs for policy appraisal
  - Detailed metadata and clear file-naming conventions to support reproducibility
  - Explicit limitations (lakes, calendar, calibration scope) to inform governance and risk assessment
  - Necessity of ensemble-based interpretation to capture uncertainty in future river flows
  - Complementary datasets (catchment, lake, NRFA station locations) to aid interpretation and integration with observed data

## Citing and acknowledgements
- Data usage citation: Kay, A.L.; Rudd, A.C.; Davies, H.N.; Lane, R.A.; Bell, V.A. (2021). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080). NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/7079d6e8-6184-4f80-89b4-4db924ec8b05
- Acknowledges UK-SCAPE programme and NERC support; mentions contributors and related methodological references

## References (selected)
- Bell et al. 2009, 2016; Kay et al. 2021; Lane & Kay 2021; Robinson et al. 2021; Murphy et al. 2018; Rowland et al. 2017; and others cited in the dataset documentation.