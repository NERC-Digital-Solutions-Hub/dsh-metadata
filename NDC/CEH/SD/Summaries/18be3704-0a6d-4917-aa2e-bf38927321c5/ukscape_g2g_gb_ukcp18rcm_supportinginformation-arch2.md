# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Overview
  - Provides Grid-to-Grid (G2G) hydrological model estimates of Great Britain river flows driven by UKCP18 Regional (12km) projections.
  - Outputs are on a 1km x 1km grid across GB for December 1980 to November 2080 under RCP8.5, using a 12-member perturbed parameter ensemble (PPE).
  - Key outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow, with corresponding dates of occurrence.

- Datasets and spatial-temporal scope
  - Spatial resolution and domain: 1km x 1km grid covering non-tidal river cells with catchment area ≥ 50 km² (GB national grid domain: 700 km × 1000 km).
  - Variables produced (per grid cell):
    - Monthly mean river flow (m³ s⁻¹)
    - Annual maxima of daily mean river flow (m³ s⁻¹)
    - Annual minima of 7-day mean river flow (m³ s⁻¹)
  - Timeframe: December 1980 – November 2080 (water years for daily maxima; Dec–Nov for annual minima).
  - Additional datasets:
    - Digitally-derived catchment areas (1 km grid)
    - Estimated NRFA gauging station locations (1 km grid) and station IDs

- Hydrological model (Grid-to-Grid, G2G)
  - A national-scale, 1 km × 1 km grid-based model with 15-minute time steps.
  - Outputs natural river flows for gauged and ungauged rivers; calibrated values are not catchment-specific, using nationally applicable parameters where needed.
  - Accounts for urban/suburban land-cover effects on runoff.
  - Input requirements: precipitation, potential evapotranspiration (PE), daily minimum and maximum temperature (for optional snow module).
  - Performance: best for natural-flow-dominated catchments; less accurate where artificial abstractions/discharges or complex subsurface hydrology prevail.

- Forcing data and processing
  - Forcing data: UKCP18 Regional (12km) PPE from the Met Office Hadley Centre (12 ensemble members), 1980–2080, RCP8.5.
  - Bias correction and downscaling:
    - Precipitation bias-corrected using monthly multiplicative factors.
    - PE derived via Penman–Monteith, aligned with MORECS methodology.
    - Downscaling:
      - Precipitation and PE from 12 km to 1 km using spatial weighting; temporal downscaling by equal distribution over model time-steps.
      - Temperature downscaled to 1 km using elevation-based lapse rates; diurnal timing adjusted with a sine curve.
  - Calendar: 360-day year used by the climate model data.

- Data formats and file structure
  - File format: NetCDF4, one file per ensemble member and per variable.
  - Naming conventions:
    - Monthly mean river flow: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual maxima of daily mean river flow: G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual minima of 7-day mean river flow: G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
  - Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 excluded).
  - Domain and grid details: 700 km × 1000 km domain; grid cell center coordinates; non-tidal river cells with catchment area ≥ 50 km² have data; others set to missing (-9999).
  - Time conventions:
    - Monthly mean flows assigned to first day of the month.
    - Annual maxima assigned to the start of the corresponding water year; annual minima assigned to the start of the Dec–Nov period.
    - Dates of occurrence provided as days since 1900-01-01.
  - Supporting grids:
    - Catchment area grid (UKSCAPE_G2G_GB_CatchmentAreaGrid.nc)
    - NRFA station grid (UKSCAPE_G2G_GB_NRFAStationIDGrid.nc) and accompanying CSV (NRFA station IDs)

- How to use the dataset for monitoring
  - Historical comparisons:
    - Compare G2G outputs driven by UKCP18 Regional data with outputs driven by observation-based inputs or observed river flow using statistical methods (not point-by-point), suitable for multi-decadal analyses.
  - Climate-change impact assessment:
    - Use baseline and future period ensembles to statistically assess potential impacts on river flows.
    - Compare across the same ensemble member to ensure consistency across periods.
  - Context and comparability:
    - Outputs are analogous to MaRIUS-G2G-WAH2 datasets (driven by different climate model ensembles); cross-dataset comparisons should consider model and forcing differences.
  - Gauging station comparisons:
    - The NRFA-station-aligned grid enables comparing modeled flows to observed gauged data, with caveats about potential catchment discretisation differences for small catchments.

- Considerations and caveats
  - Observational comparisons should be statistical rather than point-by-point due to differences in weather features between observed data and model PPE dates.
  - Some small catchments may exhibit discrepancies because 1 km grid discretisation can misalign catchments with observed NRFA catchment areas.
  - Model performance varies with natural versus anthropogenically influenced regimes; results are most reliable for natural-flow-dominated catchments.

- Data access and acknowledgments
  - Data are part of UK-SCAPE (UK Status, Change And Projections of the Environment) Work Package 2, funded by the Natural Environment Research Council.
  - Acknowledgements to individuals and references provided for methodology and prior developments.
  - Supporting information and datasets deposited with the NERC Environmental Information Data Centre; specific references and related datasets cited.