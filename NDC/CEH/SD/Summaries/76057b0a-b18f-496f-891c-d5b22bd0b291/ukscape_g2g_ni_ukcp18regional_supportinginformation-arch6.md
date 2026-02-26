# Supporting information for: Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2

- Purpose and scope
  - Presents data and usage guidance for Grid-to-Grid (G2G) river flow estimates for Northern Ireland (NI) driven by UKCP18 Regional data.
  - Part of UK-SCAPE program; provides high-resolution hydrological outputs on a 1km × 1km grid for NI, using a 12-member perturbed parameter ensemble (PPE) of the regional climate model.

- Data access and citation
  - Licensed under Open Government Licence v3.
  - Dataset citation required: Kay, A.L.; et al. (2022). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 Regional (12km) data (1980 to 2080) v2. NERC EDS Environmental Information Data Centre. DOI provided.

- Brief dataset summary
  - Outputs:
    - Monthly mean river flow (m3 s-1)
    - Annual maxima of daily mean river flow (m3 s-1) with dates of occurrence
    - Annual minima of 7-day mean river flow (m3 s-1) with dates of occurrence
  - Spatial and temporal coverage:
    - 1km × 1km grid over NI (non-tidal rivers with catchment area ≥ 50 km2)
    - Time period: December 1980 to November 2080 (water years/months as specified)
  - Driving data:
    - UKCP18 Regional (12km) projections, PPE ensemble (12 members)
    - Baseline and future periods allow statistical comparison (not point-for-point)
  - Related datasets:
    - Complementary NI NI-wide G2G dataset driven by observation-based data
    - Similar NI/GB-wide datasets for Great Britain with their DOIs
  - Additional spatial datasets provided:
    - Digitally-derived catchment areas (1km grid)
    - Majority lake cells grid (1km)
    - Estimated locations of flow gauging stations on 1km grid plus a CSV with NRFA IDs

- Grid-to-Grid (G2G) model overview
  - A national-scale hydrological model operating on a 1km × 1km grid with outputs for gauged and ungauged rivers.
  - Uses precipitation, potential evapotranspiration (PE), and daily min/max temperatures (for optional snow module).
  - Generally calibrated with fixed, nationally applicable parameter values; no catchment-specific calibration.
  - Urban/suburban land cover influences runoff accounted for within the model.
  - Known performance: good for natural-flow catchments; limited where artificial regulation or complex subsurface hydrology dominates (notably NI flows downstream of Lough Neagh).

- Input data and processing
  - Meteorological inputs from UKCP18 Regional (12km) projections:
    - Daily precipitation, daily min/max temperature, daily PE (via a MORECS-like method)
    - 12 PPE members; 360-day calendar in climate data
  - Data processing steps:
    - Precipitation bias correction (monthly multiplicative factors)
    - PE derived via Penman–Monteith using baseline stomatal resistance values adjusted for CO2 effects
    - 12km data downscaled to 1km using spatial weighting; temporal downscaling distributes values over model time-steps
    - Temperature downscaled to 1km with elevation-based lapse rate and diurnal sine-based temporal downscaling
  - Domain and data characteristics:
    - Northern Ireland domain on GB National Grid: 187 km × 170 km
    - 30-day months due to 360-day calendar in climate model data
    - NetCDF4 format; one file per ensemble member and variable
    - Time stamps: days since 1900-01-01; monthly data assigned to first day of month; annual maxima/minima assigned to start year of their respective 12-month periods

- Format and file naming
  - NetCDF4 files, one per ensemble member and variable
  - File naming patterns:
    - G2G_NI_mmflow_UKCP18RCM_<ensnum>_1980_2080.nc (monthly flows)
    - G2G_NI_amaxflow_UKCP18RCM_<ensnum>_1980_2080.nc (annual maxima with dates)
    - G2G_NI_aminflow_UKCP18RCM_<ensnum>_1980_2080.nc (annual minima with dates)
  - Ensnum codes: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
  - Grid and data specifics:
    - Domain coordinates defined on GB National Grid; 1km grid cell centers as grid reference
    - Non-tidal river cells with catchment area ≥ 50 km2 included; others set to missing (-9999)
    - Three supplemental datasets aid usage (catchment areas, lake grid, NRFA station locations)

- Usage guidance and caveats
  - Comparison guidance:
    - Historical comparisons can be made statistically against observation-based inputs or NRFA river flow data
    - Do not perform point-by-point time series comparisons; use multi-decadal statistics
    - Baseline vs. future comparisons should use the same ensemble member across periods
  - Limitations and considerations:
    - Lakes and reservoirs not modeled; lake cells treated as rivers; lake storage effects ignored
    - NRFA gauging station mapping to 1km grid cells may have catchment-area discrepancies, especially for small catchments
  - Data integration tips:
    - Use the additional catchment-area, lake, and NRFA station location grids to align modeled flows with observed data and catchment characteristics

- Licensing, citation, and acknowledgements
  - Open Government Licence v3; citation required as detailed above
  - Acknowledgements: NERC award NE/R016429/1; gratitude to contributors

- References and context
  - References cited relate to model development, calibration approaches, and data sources (academic papers and national datasets) relevant to the G2G framework and UKCP18 inputs.