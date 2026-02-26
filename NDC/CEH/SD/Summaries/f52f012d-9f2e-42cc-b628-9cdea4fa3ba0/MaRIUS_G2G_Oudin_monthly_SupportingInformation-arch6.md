# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-monthly]

- Purpose and scope
  - Presents the MaRIUS-G2G-Oudin-monthly dataset produced for Grid-to-Grid (G2G) hydrological modeling across Great Britain, covering 1891–2015.
  - Supports drought and water scarcity analysis within the MaRIUS project framework.

- What data are included
  - Grid-to-Grid model outputs on a 1 km x 1 km grid for Great Britain:
    - Flow (m3 s-1)
    - Soil moisture (mm water per m of soil)
  - Outputs are monthly means of daily values (09:00–09:00).
  - Additional spatial data to aid interpretation:
    - Digitally-derived catchment areas (1 km grid)
    - Estimated locations of flow gauging stations on the grid and as a CSV

- Model and methods overview
  - Hydrological model: Grid-to-Grid (G2G) at 1 km x 1 km resolution, 15-minute time-step, parameterised from digital datasets (soil types, land cover).
  - Accounts for urban/suburban land-cover effects on runoff but does not include abstractions or discharges.
  - Calibration relies on spatial datasets with nationally applicable parameter values; no catchment-specific calibration is performed.
  - Snow module not used; precipitation input is rainfall (PE estimated separately).

- Input driving data and processing
  - Meteorological drivers (observation-based):
    - 1 km x 1 km daily rainfall (CEH-GEAR)
    - Monthly potential evaporation (PE) estimates from temperature (5 km x 5 km)
  - Data preparation and limitations:
    - Early-20th-century rainfall gaps were spatially infilled.
    - PE derived from temperature using Oudin et al. (2005) method with long-term mean corrections to align with MORECS references.
  - Data translation to model:
    - PE and rainfall are distributed to the 15-minute model time-step with uniform allocation across grid cells.

- Output data format and structure
  - File: MaRIUS-G2G-Oudin-monthly 1 km x 1 km NetCDF4
  - File name: G2G_Oudin_var_1891_2015.nc (variables: 'flow' or 'soil')
  - Domain: 700 km x 1000 km GB grid; land grid boxes only; sea set to missing (-9999)
  - Time: days since 1891-01-01; monthly values assigned to the first day of each month
  - Additional identification files:
    - MaRIUS_G2G_CatchmentAreaGrid.nc (catchment area in km2 per grid cell)
    - MaRIUS_G2G_NRFAStationIDGrid.nc (NRFA gauge station locations mapped to grid)
    - MaRIUS_NRFAStationIDs.csv (list of NRFA station IDs)

- How to use and interpret
  - Compare G2G natural-flow outputs to observed gauged flows (e.g., NRFA).
  - Performance is strongest for catchments with natural flow regimes and reliable observed data; less accurate where artificial abstractions/discharges or complex subsurface hydrology dominate.
  - The NRFA station mapping provides the best grid cell representation for matching observed gauges, though some small-catchment discretisation errors may occur.

- Known limitations and caveats
  - G2G focuses on natural flows; outputs may be influenced by unrepresented abstractions and discharges.
  - Sub-surface hydrology complexity may cause discrepancies in certain regions.
  - Catchment discretisation to 1 km grid can introduce differences in small catchments between observed NRFA catchments and grid-derived catchments.

- Acknowledgements and references
  - Funded by the UK Natural Environment Research Council (NERC) under MaRIUS (NE/L010208/1) as part of drought and water scarcity research.
  - References include key methodological sources for CEH-GEAR rainfall, PE estimation, and G2G model development and evaluation.