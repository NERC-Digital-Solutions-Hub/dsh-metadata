# Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE programme outputs providing gridded river-flow estimates across Britain using a Grid-to-Grid (G2G) hydrological model.
- Focus on climate-change impacts on water quantity (river flow) for 1km x 1km grid cells with catchment area ≥50 km².
- Driven by UKCP18 Regional (12km) projections under RCP8.5, spanning December 1980 to November 2080, using a 12-member perturbed parameter ensemble (PPE).

## Data content and variables
- Variables (monthly and annual extremes):
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹) and dates of occurrence
  - Annual minima of 7-day mean river flow (m³ s⁻¹) and dates of occurrence
- Spatial and temporal resolution
  - 1 km x 1 km grid across Great Britain (non-tidal, non-sea cells)
  - 700 km × 1000 km domain (grid indices 0–700000, 0–1000000 m)
  - 30-day model months (360-day calendar)
  - Values center of each 1 km grid cell; dates stored as days since 1900-01-01
- Ensemble and timing
  - 12 PPE ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
  - Baseline (1980–1990s) and future (up to 2080) periods use the same ensemble member for comparisons

## Model, inputs, and processing
- G2G model characteristics
  - National-scale hydrological model; calibrated with general, not catchment-specific parameters
  - Simulates natural river flows; accounts for urban/suburban land-cover effects on runoff
- Input data and bias correction
  - Meteorological inputs from UKCP18 Regional (12 km) projections: daily precipitation, daily min/max temperature, daily PE
  - Simple bias correction for precipitation using monthly multiplicative factors
  - Potential evaporation derived via Penman-Monteith (MORECS-based adjustments for CO₂)
  - 12 km data downscaled to 1 km:
    - Precipitation downscaled spatially using 1 km rainfall-pattern weighting; temporally divided evenly across model steps
    - PE downscaled to 1 km and evenly distributed across steps
    - Temperature downscaled to 1 km using elevation-based lapse rates and day-time variation via sine curve
- Data domain and output scope
  - Outputs for non-tidal river cells with catchment area ≥50 km²
  - Annual maxima/minima include dates of occurrence
- Additional interpretation aids
  - Complementary dataset with G2G estimates driven by observation-based data
  - Digitally-derived catchment-area grid and NRFA station location grid (for comparing model flows against observed NRFA data)

## Data format and organization
- File format
  - NetCDF4, one file per ensemble member and variable
  - File naming:
    - Monthly flows: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual max flows: G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual min flows: G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
- Metadata and conventions
  - CEH gridded dataset conventions followed
  - Values outside domain set to missing (-9999)
  - “Days since 1900-01-01” time coordinate; first day of month assigned for monthly flows
  - 360-day calendar due to climate model data
- Ancillary datasets
  - UKSCAPE_G2G_GB_CatchmentAreaGrid.nc (catchment area per 1 km cell)
  - UKSCAPE_G2G_GB_NRFAStationIDGrid.nc and NRFAStationIDs.csv (NRFA gauging-station mapping)

## How to use the dataset
- Comparisons and interpretation
  - Historical comparisons to observation-based inputs or observed river flow are possible but should be statistical (multi-decadal) rather than point-by-point; exact weather features may not map directly to a given date in the PPE
  - Future-period comparisons can be used to assess climate-change impacts on river flows, using the same ensemble member across periods
- Practical considerations
  - Data are provided for non-tidal river cells with adequate catchment area; caution for small-catchment discretisation errors
  - Ensemble management: compare like-for-like by using identical ensemble members for baseline and future

## Provenance, governance, and accessibility
- Provenance
  - Part of the UK-SCAPE programme; funded by the Natural Environment Research Council
  - Associated with prior MaRIUS-G2G datasets; methodological lineage detailed in referenced literature
- Access notes
  - Dataset includes supporting materials and references to related datasets for context and validation

## Limitations and caveats
- Potential mismatches for small or complex catchments due to 1 km discretisation
- G2G parameters are not catchment-specific calibrated; model performance varies with natural vs anthropogenically influenced regimes
- Calendar simplifications (360-day year) and 30-day months influence temporal alignment with observed records

## Related datasets and references
- Complementary observation-driven dataset (flow driven by observation-based inputs)
- NRFA and NRFAStationID data for gauging-station comparisons
- Key references include Bell et al. (2009, 2007, 2016, 2018), Kay et al. (2021), Lane & Kay (2021), Guillod et al. (2017, 2018), among others

## Acknowledgements
- Supported by NERC award NE/R016429/1; UK-SCAPE programme
- Contributions and advice from listed collaborators acknowledged