# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-monthly]

## Overview
- MaRIUS is a UK NERC-funded project (2014-2017) that developed a risk-based approach to drought and water scarcity.
- This dataset provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1km x 1km grid across Great Britain for 1960–2015.
- Variables included: 
  - Flow (m3 s-1)
  - Soil moisture (mm water per m of soil)
- Outputs are monthly means of daily values (11:00? 09:00–09:00 in description) and are driven by observed meteorological data.

## What’s included
- Primary variables:
  - Flow (m3 s-1)
  - Soil moisture (mm water/m soil)
- Two supporting spatial datasets:
  - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment areas (km2) draining to each 1km grid box
  - NRFA gauging station locations mapped to the 1km grid (MaRIUS_G2G_NRFAStationIDGrid.nc) and a CSV with NRFA station details (MaRIUS_NRFAStationIDs.csv)
- Coverage and accessibility:
  - 1km x 1km land grid boxes; sea grid boxes are set to missing (-9999)
  - Data described as natural-flow-focused; some catchments may be influenced by abstractions/discharges in reality

## Model and inputs
- Hydrological model: Grid-to-Grid (G2G)
  - National-scale, 1km grid, 15-minute time-step
  - Parameterised from soil and land-cover data; accounts for urban/suburban land-cover effects on runoff
  - Emphasis on natural flow regimes; calibration is dataset-driven rather than catchment-specific
- Driving meteorological data:
  - Daily rainfall on 1km CEH-GEAR grids
  - Monthly potential evapotranspiration (PE) on a 40km MORECS grid
  - PE values are copied to 1km boxes and downscaled to 15-minute time-steps
- Outputs:
  - Monthly averages of daily mean flows and soil moisture
  - Historical period: 1960–2015
- Snow module not used in this dataset; precipitation treated as rain

## Data format and structure
- Primary data file: MaRIUS-G2G-MORECS-monthly NetCDF4
  - File naming: G2G_MORECS_var_1960_2015.nc
  - var is either 'flow' or 'soil'
  - Spatial domain: 700 km × 1000 km GB national grid (0,0 to 700000,1000000 meters)
  - Grid cell values: center of each 1km x 1km cell; sea cells are missing
  - Time: days since 1900-01-01; monthly values assigned to the first day of the month
- Grid metadata:
  - 1km x 1km grid cells represent land; NRFA comparison and catchment mapping use the provided 1km grids
- Additional NRFA/catchment data:
  - MaRIUS_G2G_NRFAStationIDGrid.nc: 1km grid with NRFA station IDs mapped to grid cells
  - MaRIUS_NRFAStationIDs.csv: details of the 1285 NRFA gauging stations with corresponding grid mappings
- Figure examples show output grids, NRFA station locations, and catchment area overlays (for Wales)

## How to use
- Validation and comparison:
  - Compare G2G natural-flow outputs with observed NRFA river flows (e.g., NRFA database)
- Model performance considerations:
  - G2G performs well for catchments with natural flow regimes and reliable observed flow records
  - Less accurate where flows are heavily influenced by abstractions, discharges, or complex sub-surface hydrology
- Spatial and temporal considerations:
  - Be aware of potential catchment-area discrepancies for small catchments due to 1km discretisation
  - Use the NRFA-station mapping grid to identify the most representative G2G grid cell for comparison with observed data

## Limitations and caveats
- Calibration is not catchment-specific; parameter values are nationally applicable
- The model does not incorporate certain artificial influences in some catchments, which may affect accuracy in those areas
- Catchment area and NRFA mapping may introduce mismatches in small-scale basins

## Acknowledgements and references
- Dataset outcome of the MaRIUS project funded by the UK Natural Environment Research Council (NE/L010208/1)
- Acknowledgements to contributors for advice and data availability
- Key references include:
  - Bell et al. (2009, 2016)
  - Davies and Bell (2009)
  - Hough and Jones (1997)
  - Keller et al. (2015)
  - Monteith (1965)
  - Rudd et al. (2017)
  - Tanguy et al. (2016)

## Figure
- Example outputs include 1km x 1km flow and soil moisture grids, NRFA station locations, and catchment-area overlays (e.g., Wales region)