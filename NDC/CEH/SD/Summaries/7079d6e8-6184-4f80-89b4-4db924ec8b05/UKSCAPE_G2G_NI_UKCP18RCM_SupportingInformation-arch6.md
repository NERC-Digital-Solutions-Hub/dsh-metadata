# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Data accessibility and citation
  - Data available under the Open Government Licence at the provided DOI.
  - Citation requirement: Kay et al. (2021) NERC EDS dataset; include DOI when using the data.

- Brief dataset summary
  - UK-SCAPE program WP2 focus: impacts of climate change on water quantity (river flow) in Britain.
  - Grid-to-Grid (G2G) hydrological model outputs for Northern Ireland on a 1km x 1km grid.
  - Variables provided: monthly mean river flow (m3 s-1), annual maxima of daily mean river flow (m3 s-1), and annual minima of 7-day mean river flow (m3 s-1), for non-tidal catchments with at least 50 km2 area.
  - Temporal coverage: December 1980 to November 2080, driven by UKCP18 Regional (12km) projections using a 12-member perturbed parameter ensemble (PPE), under RCP8.5.
  - Output context: NI data generated with a 12-member PPE and a complementary dataset driven by observation-based inputs for comparison.
  - Additional spatial datasets provided: catchment areas (1km grid), majority lake cells (1km grid), and estimated NRFA gauging station locations.

- Hydrological model overview (Grid-to-Grid, G2G)
  - National-scale, 1km x 1km grid with 15-minute time steps; configured to cover NI and some ROI catchments draining to NI rivers.
  - Produces spatially consistent river-flow estimates for gauged and ungauged rivers.
  - Calibration: uses globally applicable parameter values; no catchment-specific calibration; accounts for urban/suburban land-cover via model structure.
  - Performance notes: generally good for natural-flow-dominated catchments; limitations downstream of large regulated lakes (e.g., flood regulation at Lough Neagh).

- G2G input data and processing
  - Meteorological drivers: daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE) from UKCP18 Regional 12km PPE ensemble (12 members) for 1980–2080 under RCP8.5.
  - Data handling: bias-corrected precipitation (monthly multiplicative factors); PE derived via Penman-Monteith; downscaled to 1km using spatial weighting and elevation-based temperature downscaling; temporal downscaling performed to match model time steps.
  - Calendar: 360-day year in model data; months treated as 30-day periods; dates of annual maxima/minima provided.
  - Domain and inputs: outputs cover non-tidal 1km grid cells with catchment area ≥50 km2; urban and soil data sources follow established CEH datasets.

- How to use the dataset
  - Historical comparisons: compare G2G NI outputs driven by UKCP18 data to those driven by observation-based inputs or NRFA observations; avoid point-for-point comparisons; use multi-decadal statistical comparisons.
  - Future assessments: compare baseline and future periods statistically to explore climate-change impacts on river flows; use the same ensemble member across periods for consistency.
  - Ensemble specifics: ensemble numbers are 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (excluding 02, 03, 14).

- Data format and structure
  - Output files: NetCDF4, one file per ensemble member and per variable.
  - File naming: G2G_NI_mmflow_UKCP18RCM_ ensnum _1980_2080.nc; G2G_NI_amaxflow_UKCP18RCM_ ensnum _1980_2080.nc; G2G_NI_aminflow_UKCP18RCM_ ensnum _1980_2080.nc.
  - Spatial domain: Northern Ireland on GB National Grid; 1km x 1km cells; non-tidal river cells with catchment area ≥50 km2; missing data marked -9999.
  - Temporal details: 30-day months due to 360-day calendar; time stamps in NetCDF as days since 1900-01-01; maxima/minima occurrence dates provided in days since 1900-01-01.
  - Timing conventions: annual maximum assigned to the start of the water-year; annual minimum assigned to the start of the Dec–Nov year; dates of occurrence included as additional variables.

- Supporting datasets
  - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc: catchment area (km2) per 1km cell.
  - UKSCAPE_G2G_NI_LakeGrid.nc: majority lake cells (≥70% water); used to identify lake-influenced pathways.
  - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv: approximate NRFA gauging station locations on the 1km grid and their IDs for comparison.

- Limitations and caveats
  - Lakes and reservoirs: water bodies not explicitly modeled; lake areas treated as river cells, potentially affecting downstream flows.
  - NRFA catchment matching: small catchments may have discrepancies between derived 1km grid catchments and observed NRFA catchments due to discretisation.
  - Comparative cautions: statistical rather than point-wise comparisons advised when evaluating against observations or other data sources.

- Acknowledgements and references
  - Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability.
  - Acknowledgement of contributors and key references detailing model development, data sources, and methodology.