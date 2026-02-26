# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-daily]

- Purpose and scope
  - Provides driving data and context for Grid-to-Grid (G2G) model estimates of daily mean river flow for gauged catchments across Great Britain (1960–2015).
  - Part of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity).

- Dataset focus
  - Daily river flow estimates (m3 s-1) at 260 NRFA gauging stations, represented by the nearest 1 km G2G grid cell.
  - Time period: 1960–2015; flows are daily means from 09:00 to 09:00 the following day.
  - Output file: G2G_MORECS_flow_1960_2015.csv (CSV format; one column per catchment, first column date).

- Model and driving data (Grid-to-Grid)
  - G2G is a national-scale hydrological model running on a 1 km x 1 km grid with a 15-minute time-step.
  - Parameterisation relies on spatial datasets (soil, land-cover); calibration is not performed for individual catchments.
  - Model uses observed meteorological inputs:
    - Daily rainfall: 1 km CEH-GEAR grid
    - Potential evaporation (PE): 40 km MORECS grid
  - Snow module not used in this dataset; precipitation treated as rain.

- Data inputs and sources
  - Rainfall: CEH-GEAR 1 km daily precipitation estimates (Keller et al., 2015; Tanguy et al., 2016).
  - Evapotranspiration: MORECS monthly PE estimates (Hough & Jones, 1997) regridded to the 1 km G2G grid cells.
  - Spatial data: topography and soil data as per Bell et al. (2009).

- How to use the dataset
  - Compare G2G natural flow outputs to observed NRFA gauged flows for validation and drought/water scarcity analyses.
  - Best performance for catchments with natural flow regimes and reliable flow records; less accurate where abstractions/discharges or complex subsurface hydrology are significant.
  - Flows correspond to the G2G grid cell that best matches each NRFA station’s location and catchment area, with checks to ensure correct river tributary assignment.

- Data format and related files
  - MaRIUS-G2G-MORECS-daily flow data: G2G_MORECS_flow_1960_2015.csv
    - Structure: header line, first column = date, subsequent columns = flows for each catchment.
  - Related file: MaRIUS_NRFAStationInfo.csv
    - Contains NRFA station details: station ID, river name, location, G2G coordinates, catchment area, data issues.

- Limitations and caveats
  - Catchment areas derived from 1 km grid may differ from NRFA catchments; differences are generally within 8% but can be larger for small catchments due to discretisation.
  - No catchment-specific calibration of G2G parameters; model emphasizes spatial datasets over per-catchment calibration.
  - Artificial influences (abstractions, discharges) and complex subsurface hydrology are not explicitly represented; performance is best for natural-flow conditions.

- Acknowledgements
  - Funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
  - Recognises contributions from Nuria Bachiller-Jareno, Matt Fry, and Maliko Tanguy.

- References (selected)
  - Bell et al. (2007, 2009, 2016)
  - Hough & Jones (1997)
  - Keller et al. (2015)
  - Monteith (1965)
  - Rudd et al. (2017)
  - Tanguy et al. (2016)