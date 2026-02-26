# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-monthly]

- Purpose and scope
  - Provides observed driving data for the Grid-to-Grid (G2G) hydrological model to produce monthly mean flow and soil moisture across Great Britain (GB) for 1960–2015.
  - Supports interpretation and use of G2G outputs (flow and soil moisture) by enabling comparison with observed river flows and evaluation of drought-related analyses.

- MaRIUS project context
  - MaRIUS stands for Managing the Risks, Impacts and Uncertainties of drought and water Scarcity (UK NERC-funded, 2014–2017).
  - The dataset is part of the MaRIUS-G2G-MORECS-monthly product and is connected to broader MaRIUS activities.

- Dataset contents
  - Grid-to-Grid model outputs on a 1 km x 1 km grid for GB:
    - Flow (m3 s-1) – monthly means of daily values (09:00–09:00)
    - Soil moisture (mm water per m soil) – monthly means of daily values
  - Temporal coverage: 1960–2015 (historical period)
  - Spatial coverage and resolution: 1 km x 1 km grid, GB national grid; land grid boxes only (sea set to -9999)
  - Additional interpretive data:
    - Digitally-derived catchment areas on a 1 km x 1 km grid
    - Estimated locations of flow gauging stations (NRFA) on the 1 km x 1 km grid and as a CSV

- Grid-to-Grid (G2G) model details
  - A national-scale hydrological model operating on a 1 km x 1 km grid with a 15-minute time-step.
  - Parameterised using spatial datasets (soil, land cover) and accounts for urban/suburban land-cover effects on runoff.
  - Calibrations are not performed at the catchment level; spatial datasets provide model parameters where needed.
  - Snow module not used here; precipitation input is treated as rain (input is observation-based and does not explicitly model snow processes).
  - Outputs are monthly averages of daily natural flows and soil moisture; explicit flows represent natural (unabstraacted/discharged) conditions.

- Meteorological driving data and spatial data inputs
  - Daily areal rainfall at 1 km x 1 km resolution (CEH-GEAR)
  - Monthly potential evaporation (PE) at 40 km resolution (MORECS)
  - PE values are copied to corresponding 1 km x 1 km boxes and split equally down to 15-minute model timesteps
  - Additional spatial data include topography and soil data as used in Bell et al. (2009)

- File formats, naming, and domain
  - Data stored as NetCDF4 (CEH gridded dataset conventions)
  - File naming: G2G_MORECS_var_1960_2015.nc (historical period)
  - Variables: flow or soil
  - Spatial domain: 700 km x 1000 km GB grid (coordinates 0–700000, 0–1000000 m)
  - Time: calendar days since 1900-01-01; first day of each month used for monthly values
  - Data quality flags: land grid boxes only; sea grid boxes set to -9999

- How to use the dataset
  - Compare G2G natural-flow estimates to observed river flows (e.g., NRFA data)
  - Use performance assessments (e.g., Bell et al. 2009; Rudd et al. 2017) to gauge reliability, with best performance in catchments with natural flow regimes and accurate observed records
  - NRFA gauging station integration:
    - MaRIUS_G2G_NRFAStationIDGrid.nc provides best-matched 1 km grid cells for NRFA stations
    - MaRIUS_NRFAStationIDs.csv contains NRFA station details for which a corresponding grid cell is defined
  - Awareness of potential mismatches in small catchments due to 1 km discretisation and catchment-area misalignment

- Related datasets and outputs
  - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment area (km2) drained by each 1 km grid box
  - MaRIUS_G2G_NRFAStationIDGrid.nc and MaRIUS_NRFAStationIDs.csv: NRFA station alignment data
  - Example outputs illustrating flow and soil moisture across GB and NRFA station locations (Figure 1 in the documentation)

- Limitations and caveats
  - G2G does not account for artificial abstractions or discharges; performance may be reduced in heavily managed systems
  - Sub-surface hydrology complexity can affect accuracy in some regions
  - Gauging-station mapping to 1 km grid boxes may introduce catchment-area differences for small basins
  - The snow module is not engaged; precipitation input uses rainfall-only assumptions, which may influence drought characterization

- Acknowledgements and references
  - Dataset produced under the MaRIUS project; thanks to contributors including Nuria Bachiller-Jareno, Matt Fry, and Maliko Tanguy
  - Key references include Bell et al. (2009, 2016), Davies & Bell (2009), Hough & Jones (1997), Keller et al. (2015), Monteith (1965), Rudd et al. (2017), Tanguy et al. (2016)