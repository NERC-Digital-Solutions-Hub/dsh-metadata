# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by observed data (1980 to 2011)

- What the dataset is
  - Grid-to-Grid (G2G) hydrological model estimates of river flow across Great Britain on a 1 km x 1 km grid, driven by observed meteorological data, for 1980–2011.
  - Variables provided: monthly mean river flow (m3 s-1), annual maxima of daily mean river flow (m3 s-1), and annual minima of 7-day mean river flow (m3 s-1) for non-tidal catchments with area ≥ 50 km2.
  - A complementary dataset provides G2G estimates driven by UKCP18 Regional (12 km) climate projections.
  - Two additional spatial datasets included: digitally-derived catchment areas (1 km grid) and estimated locations of flow gauging stations on a 1 km grid with station information.

- Model overview (Grid-to-Grid, G2G)
  - National-scale hydrological model on a 1 km grid with a 15-minute time-step, designed to produce natural river flows for gauged and ungauged rivers across GB.
  - Uses spatial data rather than catchment-specific calibration; when model parameters are required, nationally applicable values are used (e.g., kinematic wave speeds).
  - Urban/suburban land-cover effects are implicitly accounted for in the model.
  - Previous performance: strongest for natural-flow regimes; less accurate in heavily managed or complex subsurface conditions.

- Model inputs
  - Precipitation: daily 1 km grids (CEH-GEAR)
  - Potential evaporation (PE): monthly 40 km grids (MORECS)
  - Temperature: daily min and max on 1 km grid (Met Office HadUK-Grid)
  - Snow module (optional) uses temperature data

- Data outputs and format
  - Outputs provided for non-tidal river cells with catchment area ≥ 50 km2.
  - Time and space formats:
    - NetCDF4 files per variable with specific naming:
      - Monthly mean flow: G2G_GB_mmflow_obs_1980_2011.nc
      - Annual maxima of daily mean flow: G2G_GB_amaxflow_obs_1980_2011.nc
      - Annual minima of 7-day mean flow: G2G_GB_aminflow_obs_1980_2011.nc
    - Domain: 700 km x 1000 km, GB National Grid, 1 km resolution; grid cell centers are the data points; missing values indicated by -9999.
    - Time stamps: days since 1900-01-01; monthly data nominally assigned to the first day of the month; annual maxima/minima assigned to the start year of the corresponding 12-month period.
  - Spatial coverage excludes tidal areas and sea cells; only cells with catchment area ≥ 50 km2 are populated.

- Related datasets and accessibility
  - Catchment area grid: UKSCAPE_G2G_GB_CatchmentAreaGrid.nc (km2 drained to each 1 km grid cell).
  - Gauging station locations: UKSCAPE_G2G_GB_NRFAStationIDGrid.nc (1 km grid with NRFA station IDs; land = 0, sea = -9999); accompanying NRFAStationIDs.csv provides station details.
  - These datasets facilitate comparison of G2G outputs with observed river flows at NRFA gauges and help contextualize where flows are attributed.

- How to use the datasets
  - Compare G2G outputs with observed NRFA river flows to assess realism and for validation exercises.
  - Use as updates to MaRIUS-G2G-MORECS monthly data (Bell et al. 2018); note period differences (1980–2011 here) and minor model network refinements.
  - Combine with UKCP18 Regional projections (12 km) to explore climate-change scenarios for river flows.
  - For gauging stations, identify the best-matching 1 km grid cell by proximity and catchment area; validate that the G2G flow corresponds to the correct river tributary.
  - Be aware of potential mismatches for small catchments due to 1 km grid discretisation and differences between observed NRFA catchments and grid-derived catchments.

- Specific considerations and caveats
  - Calibration is not tailored to individual catchments; potential discrepancies in areas with artificial water use, abstractions, discharges, or complex subsurface hydrology.
  - Minor differences in land-sea mask and river-network discretisation compared with related datasets; performance varies with regime type.
  - Outputs include missing values outside eligible catchments, and some spatial differences may arise between NRFA catchment definitions and the discretised 1 km grid.

- Acknowledgements and references
  - Funded by Natural Environment Research Council under the UK-SCAPE programme (award NE/R016429/1).
  - Key references include Bell et al. (2009, 2016, 2018), Rudd et al. (2017), Formetta et al. (2018), Davies and Bell (2009), Hough and Jones (1997), Met Office HadUK-Grid (2019).