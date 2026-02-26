# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Overview: This dataset provides Grid-to-Grid (G2G) hydrological model estimates of river flow across Great Britain at 1 km resolution, driven by UKCP18 Regional (12 km) climate projections for 1980–2080 under RCP 8.5. Output supports analysis of climate-change impacts on water quantity, including river flow magnitude and extremes.

- Data products and scope:
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹)
  - Annual minima of 7-day mean river flow (m³ s⁻¹)
  - Coverage on a 1 km × 1 km grid across Great Britain (non-tidal, catchment area ≥ 50 km²)
  - Time period: December 1980 to November 2080
  - Driven by a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model
  - Complementary dataset available for flows driven by observation-based input data

- Model: Grid-to-Grid (G2G) details:
  - National-scale hydrological model with 1 km grid, 15-minute time-step
  - Outputs provide spatially-consistent estimates for gauged and ungauged rivers
  - Calibration is not catchment-specific; uses nationally applicable parameter values
  - Accounts for urban/suburban land-cover effects on runoff
  - Model performance: robust for natural-flow regimes; limitations near heavily regulated or complex subsurface hydrology

- Model inputs and data processing:
  - Meteorological inputs derived from UKCP18 Regional (12 km) projections: daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE)
  - PPE ensemble includes 12 members; 360-day calendar used by climate model data
  - Bias correction: simple monthly multiplicative adjustment to precipitation
  - PE derived via Penman-Monteith, aligned with MORECS methodology
  - Spatial downscaling: 12 km → 1 km grid using location-based rainfall weighting; PE downscaled to 1 km; temperature downscaled with elevation-based lapse rates and diurnal timing via a sine curve
  - G2G inputs also include topography and soil data as per Bell et al. (2009)

- Data format and file organization:
  - 1 km × 1 km gridded data stored in NetCDF4 format, one file per ensemble member and per variable
  - Variables include: monthly mean flow, annual max flow, annual min flow (with dates of occurrence)
  - File naming conventions (examples):
    - G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
    - G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
    - G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
  - Domain: 700 km × 1000 km (GB National Grid: 0–700,000 to 1,000,000 m)
  - Spatial resolution: 1 km × 1 km cells; non-tidal flows only; missing data (-9999) outside catchment ≥ 50 km²
  - Temporal representation:
    - 30-day months (360-day calendar)
    - Monthly mean flows assigned to first day of each month
    - Annual maxima/minima assigned to start year of corresponding 12-month period
  - Supporting datasets:
    - Catchment-area grid (km²) draining to each 1 km cell
    - NRFA gauging station locations grid (1 km), plus a CSV with station IDs
  - Comparable datasets and notes align with MaRIUS G2G family, with updates since earlier versions

- Auxiliary datasets and validation aids:
  - Digitally-derived catchment area grid for each 1 km cell
  - NRFA station location grid to facilitate comparison between modeled flows and observed river flows
  - Station IDs CSV provides NRFA identifiers and grid references for validation purposes

- How to use the data:
  - Historical vs future comparisons should be statistical (multi-decadal) rather than point-by-point time-matching
  - Use the same ensemble member across periods when comparing baseline and future scenarios
  - Datasets enable assessment of climate-change impacts on river flows and extremes in GB
  - Related datasets (MaRIUS-G2G-WAH2-monthly) provide context for alternative driving data

- Data quality, limitations, and caveats:
  - Model performance varies by catchment type and hydrological regime; best for natural regimes, less precise where abstractions or complex subsurface hydrology dominate
  - Differences between G2G outputs and observed weather features mean direct pointwise comparisons are inappropriate; rely on multi-decadal statistical comparisons
  - Small catchments can have discretisation-related discrepancies between NRFA catchments and 1 km G2G cells
  - Downscaling and bias-correction steps introduce uncertainties; results should be interpreted with appropriate caution
  - -9999 used as fill value; some grid cells may be missing or not applicable due to catchment criteria

- Access, provenance, and acknowledgments:
  - Funded by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE programme
  - Status: part of NERC Environmental Information Data Centre and national capability
  - Acknowledgements to contributors and related methodological references are provided

- Key references (selected):
  - Bell, Kay, Davies, Jones, and colleagues (various years) on G2G development, downscaling, and validation
  - Kay and colleagues (2021) on grid-to-grid river flow estimates driven by UKCP18
  - Related MaRIUS, MORECS, and climate-model data papers detailing methodology and validation
  - UKCP18 Regional projections and associated climate-model datasets (Hadley Centre)