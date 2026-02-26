# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-monthly]

- Overview
  - Provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1 km × 1 km grid across Great Britain for 1960–2015.
  - MaRIUS project context: UK NERC-funded research (2014–2017) addressing drought and water scarcity risks and uncertainties.

- Data content
  - Variables produced at monthly means of daily values (09:00–09:00):
    - Flow (m3 s-1)
    - Soil moisture (mm water per m soil)
  - Additional spatial datasets to aid interpretation:
    - Digitally-derived catchment areas on a 1 km grid
    - Estimated locations of flow gauging stations on the grid (1 km grid and CSV)
  - Time period: 1960–2015 (historical)
  - Spatial domain: 700 km × 1000 km GB national grid, land grid boxes only (sea grid boxes set to -9999)
  - Output format: NetCDF4, with variables named 'flow', 'soil', and 'time'

- Model and driving data
  - Model: Grid-to-Grid (G2G), national-scale hydrological model running at 1 km grid with 15-minute time steps
  - Parameterisation: uses digital soil, land-cover, topography data; accounts for urban/suburban land-cover effects on runoff
  - Calibration: primarily data-driven by spatial datasets; no catchment-specific calibration; national parameter values used where needed
  - Snow module: not used in this dataset; precipitation treated as rain
  - Input meteorology:
    - Daily rainfall fields on a 1 km CEH-GEAR grid
    - Monthly potential evapotranspiration (PE) on a 40 km grid (MORECS)
  - Data processing note: PE values are distributed to 1 km boxes and divided across the 15-minute model time-steps

- Use and interpretation
  - Natural flow estimates can be compared with observed river flows (e.g., National River Flow Archive, NRFA)
  - Performance: reasonable for catchments with natural flow regimes; less accurate where artificial abstractions/discharges are significant or sub-surface hydrology is complex
  - Spatial/temporal considerations: flow outputs are monthly averages of daily natural flows; soil moisture represents depth-integrated values for the full soil column
  - Limitations: 1 km discretisation may misrepresent very small catchments; some mismatch between G2G-derived catchment areas and NRFA catchment areas due to discretisation

- Data products and access
  - Primary data file: MaRIUS-G2G-MORECS-monthly 1 km × 1 km gridded data
    - File naming: G2G_MORECS_var_1960_2015.nc
    - var: 'flow' or 'soil'
    - Domain: 700 km × 1000 km GB grid; time units: days since 1900-01-01; calendar: Gregorian
    - Grid: land cells only; missing values indicated by -9999
    - Grid cell centers used for data values
  - Supporting geospatial data:
    - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment area (km2) draining to each 1 km cell
    - MaRIUS_G2G_NRFAStationIDGrid.nc: 1 km grid mapping to NRFA station IDs
    - MaRIUS_NRFAStationIDs.csv: details of the 1285 NRFA stations with corresponding grid cells
  - Visual example: figure showing example outputs, NRFA station locations, and catchment area grid over Wales

- Validation, caveats, and interpretation guidance
  - Validation notes: comparisons to NRFA demonstrate reasonable performance for natural-flow regimes; accuracy decreases with human influence or complex subsurface hydrology
  - Potential pitfalls:
    - NRFA catchment areas may not align perfectly with 1 km G2G grid catchments, especially for small basins
    - Data gaps or provenance issues may arise from discretisation and input data limitations
  - Guidance for data leaders: assess data suitability by cross-referencing NRFA data where available, consider data gaps and metadata clarity, and plan for community validation when integrating with broader data networks

- Acknowledgements and references
  - Funded by the UK Natural Environment Research Council (NE/L010208/1) as part of UK Drought and Water Scarcity programme
  - Acknowledgements to contributors for data provision and assistance
  - Key references detailing model components, input datasets, and prior validation work (Bell et al. 2009, 2016; Davies & Bell 2009; Hough & Jones 1997; Keller et al. 2015; Monteith 1965; Rudd et al. 2017; Tanguy et al. 2016)