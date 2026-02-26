# Supporting information for: Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2

## Data access and citation information
- Data licensed under Open Government Licence v3.
- DOI: https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291
- Citation required: Kay, A.L.; Rudd, A.C.; Davies, H.N.; Lane, R.A.; Bell, V.A. (2022). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291

## Brief dataset summary
- UK-SCAPE program provides Grid-to-Grid (G2G) hydrological model estimates of river flows for Northern Ireland on a 1km x 1km grid, driven by UKCP18 Regional (12km) projections.
- Outputs include:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1) with dates of occurrence
  - Annual minima of 7-day mean river flow (m3 s-1) with dates of occurrence
- Time coverage: December 1980 to November 2080 (water years and Dec–Nov years for minima)
- Domain: Northern Ireland, on a 1km x 1km grid, with a 187 km × 170 km footprint on the GB National Grid (coordinates provided below)
- Ensemble: 12 PPE members derived from the Met Office Hadley Centre Regional Climate Model (RCM) projections under RCP8.5
- Related datasets exist for comparison with observation-based inputs (and for Great Britain) but this NI v2 release focuses on climate-driven NI flows
- Supporting spatial datasets:
  - Digitally-derived catchment areas on 1km x 1km grid
  - 1km x 1km grid identifying majority lake cells
  - Estimated locations of flow gauging stations on a 1km x 1km grid with NRFA station IDs

## Hydrological model overview (Grid-to-Grid, G2G)
- National-scale hydrological model operating on a 1km x 1km grid with a 15-minute time-step
- Configured to NI and sub-catchments draining to NI rivers; aligned with the GB national grid
- Produces natural river flow estimates for gauged and ungauged rivers
- Calibration: no catchment-specific calibration; uses nationally applicable parameter values where needed
- Includes urban/suburban land-cover effects via runoff and downstream flow pathways
- Known performance: generally good across NI; caveat near Lough Neagh where flood regulation suppresses flows

## Model input data and processing
- Meteorological inputs derived from UKCP18 Regional (12km) projections
  - Daily precipitation, daily min and max temperature, daily potential evapotranspiration (PE)
  - 12 PPE ensemble members, 1980–2080, under RCP8.5
- Processing steps:
  - Simple bias correction for precipitation (monthly multiplicative factors)
  - PE calculated with Penman-Monteith, aligned with MORECS approach
  - Spatial downscaling: 12km daily precipitation downscaled to 1km using 1km rainfall-pattern weighting
  - Temporal downscaling: daily PE copied to 1km grid and evenly distributed over model time-steps
  - Temperature downscaling: 1km using elevation-based lapse rates and diurnal sine-curves
- Calibrated inputs are not tuned to individual NI catchments; topographic and soil data follow Bell et al. (2009) as in prior work

## Format of the gridded datasets
- Data are provided as NetCDF4 files, one file per ensemble member and per variable
- File naming conventions (examples):
  - G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc (monthly mean river flow)
  - G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc (annual maxima of daily mean river flow) 
  - G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc (annual minima of 7-day mean river flow)
- Ensemble numbers: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
- Spatial domain: NI on GB National Grid, 187 km × 170 km, lower left corner (-7000, 440000) to top right (180000, 610000) (meters)
- Grid cell centroids: 1km x 1km (center of each cell)
- Data coverage: non-tidal, non-sea river cells with catchment area ≥ 50 km2; other cells set to missing (-9999)
- Calendar: 360-day year (30-day months); time variable uses days since 1900-01-01
- Temporal conventions:
  - Monthly flows assigned to the first day of the corresponding month
  - Annual maxima assigned to the start of the 12-month period (e.g., 1981 max corresponds to 1 Oct 1981–30 Sep 1982)
  - Annual minima assigned to the start year of Dec–Nov period (e.g., 1981 min corresponds to 1 Dec 1981–30 Nov 1982)
  - Dates of occurrence provided as days since 1900-01-01 for min/max files

## Additional datasets to aid use
- UKSCAPE_G2G_NI_CatchmentAreaGrid.nc: catchment area (km2) draining to each 1km cell
- UKSCAPE_G2G_NI_LakeGrid.nc: majority lake cells (≥70% water), with manual adjustments for Lough Erne
- UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv: NRFA gauging station locations and IDs (best NI matches for 43 gauging stations)

## How to use the dataset
- Historical comparisons:
  - Compare G2G NI outputs (driven by UKCP18) with outputs driven by observation-based inputs or NRFA observations statistically over multi-decadal periods; avoid point-by-point time-matching due to non-equivalence of weather features
- Baseline vs future comparisons:
  - Use the same ensemble member across periods for consistency, e.g., member 01 in baseline and corresponding member in future
  - Assess potential climate-change impacts on river flows using ensemble spread
- Interpretation notes:
  - The influence of lakes and reservoirs is not modeled; lake cells are treated as river cells
  - Lake storage/regulation effects on downstream flows are neglected
  - The NRFA gauging-station mapping to 1km G2G cells is approximate; small catchments may show discrepancies between observed catchments and G2G-derived catchments
- Practical GIS considerations:
  - NetCDF4 files per ensemble and per variable facilitate subsetting by area or time
  - Use the provided catchment and lake grids to mask or classify cells and to interpret flow signals in hydrologically meaningful zones
  - Consider the 360-day calendar when aligning time series with other datasets

## Limitations and caveats
- Lake storage and regulation effects are not included; lakes are treated as rivers
- Catchment delineation at 1km resolution may differ from observed NRFA catchments, especially for small basins
- 360-day calendar and 30-day months may affect alignment with other climate or hydrological datasets
- Results are best interpreted statistically over multi-year periods rather than point-by-point temporal matching

## References (key foundational works)
- Bell et al. (2009, 2007, 2016) on high-resolution grid-based river flow modelling and snow/evaporation assumptions
- Kay et al. and Rudd et al. on hydrological model performance and drought analyses
- Murphy et al. (2018) and UKCP18 documentation for regional projections and PPE setup
- Rowland et al. (2017) Land Cover Map 2015 and related spatial data sources
- Monteith (1965) and MORECS-based evaporation methodologies
- Additional methodological references cited in the dataset documentation