# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-monthly]

- Purpose and scope
  - MaRIUS project (2014–2017) developed a risk-based approach to drought and water scarcity.
  - Provides Grid-to-Grid (G2G) model estimates of monthly mean flow (m3 s-1) and soil moisture (mm water/m soil) on a 1 km x 1 km grid across Great Britain for 1891–2015.
  - Outputs are monthly means of daily values (09:00–09:00).

- Datasets included
  - MaRIUS-G2G-Oudin-monthly: 1 km x 1 km gridded flow and soil moisture (NetCDF4). Variables: flow or soil, time.
  - Two spatial context layers:
    - Digitally-derived catchment areas (1 km grid).
    - Estimated locations of flow gauging stations on the 1 km grid (and a CSV file).
  - Additional NRFA-related files:
    - MaRIUS_G2G_NRFAStationIDGrid.nc: 1 km grid mapping to NRFA stations.
    - MaRIUS_NRFAStationIDs.csv: NRFA station IDs with corresponding grid boxes.

- Meteorological drivers and modelling approach
  - Driving data (input):
    - Rainfall: CEH-GEAR, 1 km x 1 km daily grids.
    - Potential evaporation (PE): estimated from temperature, 5 km x 5 km grid (Oudin et al. 2005), with long-term corrections to fit MORECS baselines.
    - Early 20th century rainfall gaps are spatially infilled (to improve continuity in 1891–2015).
  - Model: Grid-to-Grid (G2G) hydrological model (1 km grid, 15-minute time-step) parameterised with soil and land-cover data.
  - Key assumptions:
    - Snow module not used; precipitation treated as rain.
    - Calibration is not performed per catchment; uses spatial datasets for parameters.
    - Focus on natural flow regimes; abstractions and discharges are not explicitly represented.
    - Outputs are daily-mean-like within monthly composites (monthly averages of daily means).

- Data format and accessibility
  - Primary file: G2G_Oudin_var_1891_2015.nc (NetCDF4), variables: flow or soil; domain 700 km x 1000 km; time as days since 1891-01-01; values missing over sea.
  - Grid indexing: each value represents the center of a 1 km x 1 km grid cell; land cells only.
  - Supporting datasets (catchments and NRFA stations) aid interpretation and validation against observed data.

- How to use and interpret
  - Use G2G flows to compare with observed gauged flows (e.g., NRFA) to assess natural-flow performance.
  - Performance tends to be best for catchments with natural flow regimes and accurate gauged records; less accurate where artificial abstractions/discharges or complex subsurface hydrology are prevalent.
  - For matching observations, use the NRFA station location grid and catchment-area grids to identify the most representative 1 km G2G cell for a given station.
  - Be aware of potential mismatches in small catchments where discretisation to 1 km introduces catchment-area differences.

- Strengths and limitations
  - Strengths:
    - Consistent, national-scale, long historical coverage (1891–2015).
    - Standardised, grid-based outputs suitable for cross-catchment analyses.
  - Limitations:
    - Not calibrated per catchment; uses globally applicable parameters.
    - Does not model anthropogenic abstractions/discharges.
    - PE estimation method differs from prior MORECS-based approaches for pre-1960 data.
    - Soil-depth and other properties vary spatially; soil moisture is depth-integrated over the soil column.
    - Some small-catchment NRFA comparisons may be affected by grid-catchment discretisation.

- Provenance and acknowledgements
  - Dataset produced under the MaRIUS project, funded by the UK Natural Environment Research Council (NE/L010208/1), part of the UK Drought and Water Scarcity programme.
  - Acknowledgements to contributors for data provision and guidance.

- References (selected)
  - Bell et al. 2009; Bell et al. 2016; Davies & Bell 2009; Hough & Jones 1997; Kay et al. 2018; Keller et al. 2015; Monteith 1965; Oudin et al. 2005; Perry & Hollis 2005; Rudd et al. 2017; Tanguy et al. 2016.