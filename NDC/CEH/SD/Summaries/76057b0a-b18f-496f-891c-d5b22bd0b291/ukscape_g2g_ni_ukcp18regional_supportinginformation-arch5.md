# Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2

## Overview
- Provides Grid-to-Grid (G2G) hydrological model outputs for Northern Ireland (NI) driven by UKCP18 Regional (12km) projections.
- Outputs are on a 1km x 1km grid across NI, covering 1980–2080 under RCP 8.5 with a 12-member perturbed parameter ensemble (PPE).
- Enables statistical comparisons of baseline vs future river flows and assessment of climate-change impacts on water quantity.

## What the dataset contains
- G2G river flow outputs on a 1km x 1km grid for NI, including:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1), with dates of occurrence
  - Annual minima of 7-day mean river flow (m3 s-1), with dates of occurrence
- Time periods:
  - Monthly data for 1980–2080 (with 360-day calendar; 30-day months)
  - Annual maxima/minima corresponding to defined water years (e.g., Oct–Sep for maxima, Dec–Nov for minima)
- Spatial and data scope:
  - Non-tidal river cells with catchment area ≥ 50 km²
  - Lake and sea handling noted (lakes treated as rivers; lake-withdrawal effects not modeled)
  - Output available for 187 km × 170 km NI domain on GB National Grid
- Ensemble details:
  - 12 PPE members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15

## Model and inputs
- Hydrological model: Grid-to-Grid (G2G), a high-resolution, grid-based rainfall–runoff model with no catchment-specific calibration; parameters are nationally consistent.
- Forcing data:
  - UKCP18 Regional (12km) projections: daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE)
  - Bias correction: monthly multiplicative factors applied to precipitation
  - Downscaling: 12km data downscaled to 1km (spatial weighting); PE downscaled to 1km; temperatures downscaled using elevation-based lapse rates and diurnal sine curves
- Land-surface and auxiliary inputs:
  - Topography and soil data aligned with prior CEH G2G configurations
  - Urban/land-cover effects incorporated via model structure

## Data format and file structure
- File format: NetCDF4 (one file per ensemble member and variable)
- Naming conventions:
  - Monthly flows: G2G_NI_mmflow_UKCP18RCM_ ensnum _1980_2080.nc
  - Annual maxima: G2G_NI_amaxflow_UKCP18RCM_ ensnum _1980_2080.nc
  - Annual minima: G2G_NI_aminflow_UKCP18RCM_ ensnum _1980_2080.nc
- Metadata and units:
  - Time units: days since 1900-01-01
  - Calendar: 360-day year (per model input)
  - Missing values: -9999
  - Each file covers NI on a 187 × 170 grid; grid cell centers represent 1km pixels
- Additional datasets to aid use:
  - CatchmentArea grid (drainage area per 1km cell)
  - LakeGrid (majority lake cells)
  - NRFAStationID grid and NRFAStationIDs.csv for gauging station locations and comparisons

## How to use the data
- Comparisons and analysis:
  - Compare G2G outputs driven by UKCP18 PPE with those from observation-based inputs or NRFA observations using statistical (multi-decadal) approaches, not point-by-point time matching
  - Evaluate baseline vs future periods to assess climate-change impacts on river flows
  - Use the same ensemble member across periods for comparisons (e.g., 01 baseline with 01 future)
- Interpretation notes:
  - Do not expect exact temporal alignment with observed weather features; ensemble members capture a range of possible futures
  - The effect of lakes and reservoirs is not represented; lake cells may show river-like flows
  - Some catchments (especially small ones) may exhibit discrepancies due to discretisation or mismatches between observed NRFA catchments and 1km grid drainage areas
- Practical considerations:
  - Water-body storage and regulation effects are neglected; RCM PPE variability drives uncertainty
  - The dataset provides maximum and minimum flow dates as separate variables for temporal context

## Licensing, citation, and provenance
- Access and licensing:
  - Data are available under Open Government Licence v3
  - Access details at the provided DOI: 10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291
- Citation:
  - Kay, A.L.; Rudd, A.C.; Davies, H.N.; Lane, R.A.; Bell, V.A. (2022). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291
- Acknowledgements:
  - Supported by NERC award NE/R016429/1 as part of the UK-SCAPE programme

## Limitations and considerations for data governance
- Model limitations:
  - No calibration per individual catchment; parameters are nationally applicable
  - No lake/reservoir storage effects; rivers passing through lakes may be misrepresented
  - Potential catchment-area and flow-path discrepancies at small catchments due to 1km discretisation
- Data management and stewardship:
  - Large, multi-file NetCDF datasets per ensemble require robust storage and cataloging
  - Clear metadata, documentation, and cross-links to catchment and gauging station data essential for discoverability and reuse
  - Users should reference the specific ensemble member and period to ensure consistent comparisons across studies