# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-monthly]

## Overview
- MaRIUS-G2G-MORECS-monthly provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1 km x 1 km grid across Great Britain for 1960–2015.
- Variables: Flow (m3 s-1) and Soil moisture (mm water per m of soil), calculated as monthly means of daily values (09:00–09:00).

## Data products and spatial context
- Primary dataset: 1 km x 1 km gridded data stored in NetCDF4, titled G2G_MORECS_var_1960_2015.nc (var is 'flow' or 'soil').
- Coverage: 700 km x 1000 km domain on the GB National Grid; any sea grid cells are set to missing (-9999).
- Output grid cell representation: each grid cell center corresponds to the 1 km x 1 km cell; time variable uses a Gregorian calendar.

## Model framework and methodology
- Hydrological model: Grid-to-Grid (G2G), national-scale, 1 km resolution, 15-minute time-step; parameterised with digital datasets (soil, land-cover, topography).
- Driving data: meteorology is observation-based.
  - Daily rainfall data on 1 km x 1 km CEH-GEAR grid.
  - Monthly potential evapotranspiration (PE) data on a 40 km MORECS grid.
- Snow module is not used in this dataset; precipitation is treated as rain.
- Output values:
  - Flow: monthly averages of daily mean natural flows (m3 s-1).
  - Soil moisture: monthly averages of daily mean soil moisture (mm water per m soil), depth-integrated across the soil column.
- Input data resolution and alignment:
  - Spatial data (topography, soils) aligned with Bell et al. 2009.
  - PE and rainfall distributed to 15-minute time steps for model driving.

## Data formats, structure and related files
- Primary NetCDF file: G2G_MORECS_var_1960_2015.nc
  - Variables: flow, soil, time
  - Time: days since 1900-01-01; values nominally assigned to the first day of each month.
  - Domain coordinates: 0–700000 m (x) by 0–1000000 m (y); land grid only; sea = -9999
- Supporting spatial datasets (for interpretation and alignment with NRFA gauges):
  - MaRIUS_G2G_CatchmentAreaGrid.nc: digitally-derived catchment areas (km2) draining to every 1 km grid box.
  - MaRIUS_G2G_NRFAStationIDGrid.nc: 1 km grid showing best locations corresponding to NRFA gauging stations.
  - MaRIUS_NRFAStationIDs.csv: details of NRFA gauging stations (1285 stations) and associated grid cells.
- Example visualization: figure showing output grids, NRFA gauge locations, and catchment-area grid over Wales.

## Usage, validation and interpretation
- Purpose: enable comparison of G2G natural flow estimates with observed NRFA river flows.
- Validation context:
  - G2G performs well for catchments with natural flow regimes and accurate observed flows.
  - Less accurate in areas with heavy anthropogenic influence (abstractions/discharges) or complex subsurface hydrology.
- Gauging station alignment:
  - Each NRFA gauge is associated with the nearest 1 km G2G cell (with checks to ensure correct tributary assignment).
  - Discrepancies may arise for small catchments due to discretisation at 1 km resolution, potentially altering catchment area drained to the selected grid cell.

## Important considerations for GIS specialists
- Resolution and scale: 1 km grid supports high-resolution spatial analyses across Great Britain; be mindful of potential aggregation errors when comparing to finer-resolution datasets.
- Data formats: NetCDF4 is standard for gridded climate/hydrological data; ensure appropriate libraries/tools are used for reading and processing.
- Units and interpretation:
  - Flow (m3 s-1) and soil moisture (mm water per m soil), with soil moisture interpreted as depth-integrated over the soil column.
- Temporal handling: monthly aggregates derived from daily means; time indexing uses a 1900 origin with the first day of the month representing the monthly value.
- Data quality and caveats:
  - Calibration is not performed; parameters are values applied nationally rather than per-catchment.
  - Possible mismatches between NRFA catchments and discretised 1 km grid representations, especially for small catchments.
  - Outputs reflect natural flows; applicability may be limited in highly managed basins.

## Acknowledgements and references
- Funded by the UK Natural Environment Research Council (MaRIUS project; NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
- Key references include Bell et al. (2009, 2016), Davies and Bell (2009), Hough and Jones (1997), Keller et al. (2015), Monteith (1965), Rudd et al. (2017), Tanguy et al. (2016).