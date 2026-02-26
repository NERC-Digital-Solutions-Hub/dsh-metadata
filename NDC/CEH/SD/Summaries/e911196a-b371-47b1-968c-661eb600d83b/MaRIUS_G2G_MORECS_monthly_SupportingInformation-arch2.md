# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-monthly]

## Overview
- MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) was a UK NERC-funded project (2014–2017) focused on drought and water scarcity risk.
- The MaRIUS-G2G-MORECS-monthly dataset provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1 km × 1 km grid across Great Britain for 1960–2015.
- Variables included: flow (m3 s−1) and soil moisture (mm water per m soil). Monthly means are derived from daily values (09:00–09:00).
- Two supporting spatial datasets are provided: digitally-derived catchment areas on a 1 km grid and estimated NRFA gauging station locations (1 km grid and CSV).

## Model and driving data
- Hydrological model: Grid-to-Grid (G2G), national-scale, 1 km grid, 15-minute time-step, parameterised with soil, land-cover and other spatial datasets.
- The model accounts for urban/suburban land-cover effects on runoff but does not simulate abstractions or discharges; no calibration is performed at the catchment level.
- Outputs are natural flow estimates (monthly averages of daily mean flows) and soil moisture (monthly averages of daily mean soil moisture). Soil moisture values are depth-integrated across the soil column.
- G2G requires input time-series of precipitation and potential evapotranspiration (PE).

## Input data sources
- Meteorological driving data:
  - 1 km × 1 km grids of daily rainfall (CEH-GEAR).
  - Monthly PE data on a 40 km grid (MORECS).
- Snow module is not used in this dataset; precipitation input is treated as rain.

## Data format and structure
- File format: NetCDF4, following CEH gridded dataset conventions.
- File naming: G2G_MORECS_var_1960_2015.nc (Historical).
- Spatial domain: 700 km × 1000 km GB National Grid (0,0) to (700000,1000000) in metres; land grid boxes only (sea set to -9999).
- Temporal domain: 1960–2015; time unit is days since 1900-01-01; monthly values assigned to the first day of each month.
- Variables:
  - flow: monthly mean natural river flow (m3 s−1).
  - soil: monthly mean soil moisture (mm water m−1 soil).
  - time: calendar time index.
- Supporting datasets to identify NRFA gauge alignment:
  - MaRIUS_G2G_NRFAStationIDGrid.nc: 1 km grid with NRFA station IDs (0 = land, -9999 = sea).
  - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment area (km2) draining to each 1 km grid cell.
  - MaRIUS_NRFAStationIDs.csv: details of the 1285 NRFA stations with corresponding grid cells.

## Using the dataset
- Purpose: provide natural-flow and soil-moisture baselines (1960–2015) for comparison with observed river flows (e.g., NRFA).
- Model performance: generally reasonable for catchments with natural flow regimes and accurate observed flows; less accurate where artificial abstractions or discharges dominate or where sub-surface hydrology is complex.
- Gauging station alignment: an NRFA station can be associated with the closest 1 km G2G cell by location and catchment area; caveats remain for small catchments where discretisation to 1 km can introduce errors in catchment delineation.
- Use caution for small catchments and when interpreting results in heavily regulated or altered systems.

## Access and references
- Acknowledgements: MaRIUS project funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
- References include key methodological and validation studies on G2G, CEH-GEAR, and MORECS data sources (Bell et al., 2009; 2016; Davies & Bell, 2009; Hough & Jones, 1997; Keller et al., 2015; Monteith, 1965; Rudd et al., 2017; Tanguy et al., 2016).
- Data accessibility note: dataset is an outcome of MaRIUS and is provided with acknowledgement to contributors and funders.