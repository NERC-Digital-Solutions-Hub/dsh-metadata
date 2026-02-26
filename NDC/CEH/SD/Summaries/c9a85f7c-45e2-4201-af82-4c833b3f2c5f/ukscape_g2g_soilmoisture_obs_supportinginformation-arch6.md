# Supporting information for Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by observed data (1980 to 2011)

- Overview
  - UK-SCAPE programme produced Grid-to-Grid (G2G) hydrological estimates of monthly mean soil moisture on a 1km x 1km grid across Great Britain (GB) and Northern Ireland (NI), using observed meteorological data (1980–2011).
  - Complements another dataset driven by UKCP18 regional projections (1980–2080); related river flow datasets for GB and NI are also available.
  - Outputs are intended to support interpretation and analysis of soil moisture patterns and to enable data-driven applications.

- What is included
  - Grid-to-Grid soil moisture estimates (monthly mean) on a 1km grid for GB and NI, driven by observed data.
  - A complementary dataset for soil moisture driven by UKCP18 regional climate projections (1980–2080).
  - Lake-related context datasets identifying majority lake cells to aid interpretation of the grid.

- Hydrological model (Grid-to-Grid, G2G)
  - National-scale hydrological model operating on a 1km x 1km grid with a 15-minute time-step (GB; NI extension includes drainages to NI rivers).
  - Outputs spatially consistent gridded estimates of natural river flows and soil moisture.
  - Uses spatial data for parameters where possible; no catchment-scale calibration; uses globally applicable parameter values where needed.
  - Accounts for urban/suburban land cover effects on runoff; does not model lakes, reservoirs, abstractions, or discharges, treating lakes as rivers for downstream influence.

- Input data used by G2G
  - Precipitation: daily 1km CEH-GEAR dataset.
  - Potential evaporation (PE): monthly 40km MORECS dataset.
  - Temperature: daily 1km HadUK-Grid (Met Office) minimum/maximum temperature.
  - Snow module: optional, driven by daily min/max temperatures.
  - Supporting topography and soil data as in Bell et al. (2009).

- Data format, time frame, and file details
  - Output: monthly mean soil moisture (m water/m soil) for each 1km grid cell.
  - GB: NetCDF4 file named G2G_GB_mmsoil_obs_1980_2011.nc (Dec 1980–Nov 2011).
  - NI: NetCDF4 file named G2G_NI_mmsoil_obs_1980_2011.nc (Dec 1980–Nov 2011).
  - Spatial domains:
    - GB: 700 km × 1000 km domain on GB National Grid from (0,0) to (700000,1000000) metres.
    - NI: 187 km × 170 km domain on GB National Grid from (-7000,440000) to (180000,610000) metres.
  - Time representation: time stamps in days since 1900-01-01; monthly values assigned to the first day of each month.
  - Lake context grids:
    - UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc
    - UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc
    - Grid cells flagged as land (1) or lake (2); sea cells marked as -9999.
    Lakes identified where >85% area is water (per Land Cover Map 2015 data).

- How to use the data
  - Use as updates to MaRIUS-G2G-MORECS monthly soil moisture data; differences include shorter period (1980–2011), land-sea mask changes, and infilling differences.
  - Compare and combine with UKCP18-driven soil moisture dataset (1980–2080) and corresponding river-flow datasets for GB and NI.
  - Suitable for analyses of spatial patterns and for informing data-driven products and decision-making.

- Important limitations and interpretation notes
  - Water bodies and lake storage effects on downstream flows are not modeled; lakes are treated as rivers for flow implications, and lake storage impacts are not captured.
  - Some grid cells within lakes still contain soil moisture estimates; lake grids are provided to aid interpretation.
  - Model performance tends to be strongest in catchments with natural flow regimes and accurate flow records; performance may decrease in heavily regulated or complex subsurface conditions.

- Acknowledgements and references
  - Supported by Natural Environment Research Council grant NE/R016429/1 under UK-SCAPE.
  - Related references include Bell et al. (2009, 2016, 2018), Rudd et al. (2017), Formetta et al. (2018), Hough & Jones (1997), and Tanguy et al. (2016); dataset links and DOIs are provided within the documentation.