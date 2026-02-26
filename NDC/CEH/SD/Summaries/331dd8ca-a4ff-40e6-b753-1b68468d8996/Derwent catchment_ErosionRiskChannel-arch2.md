# Fine-grained sediment diffuse pollution risk mapping scenarios for the Yorkshire Derwent catchment

## Overview
- Addresses fine-grained sediment (diffuse pollution) in the River Derwent, Yorkshire.
- Highlights limitations of traditional erosion risk mapping: lack of seasonal variability, bare land not captured by standard land-use maps, and limited incorporation of future rainfall/climate change.
- Demonstrates how erosion risk varies under different data and climate scenarios using SCIMAP.

## Data inputs and methods
- SCIMAP framework requires: elevation (DEM), rainfall, and land use data.
- Data sources used:
  - Elevation: 5 m Ordnance Survey DEM
  - Land use:
    - Traditional: CEH 2015 land use map
    - Seasonal satellite-derived land use (captures bare land): Sentinel-2 data
  - Rainfall:
    - Monthly 2016 rainfall data (Met Office)
    - Long-term average rainfall
  - Additional inputs:
    - Artificial drainage network (integrated by burning into the DEM)
    - UKCP09 projections for future climate (Winter only for certain runs)
- All scenarios produce erosion risk concentrations within River Derwent channels.

## Scenarios
- Data are produced for seasonal erosion risk mapping (Summer, Spring, Autumn, Winter) across 13 scenarios:
  - 1) Traditional CEH 2015 land use map
  - 2) Seasonal satellite-derived land use (captures bare land)
  - 3) Long-term rainfall averages
  - 4) Integrated artificial drainage network
  - 5–13) Winter climate change scenarios (High/Medium/Low emissions) across 90th, 50th, and 10th quartiles; model runs tested only for winter
- Scenario naming (as provided):
  - 1 - traditional land use map
  - 2 - Satellite derived land use maps
  - 3 - Long term average rainfall
  - 4 - artificial drainage network
  - 5–13 - Winter climate change (High/Medium/Low Emissions; 90th/50th/10th quartile)

## Outputs and units
- Output value range: 0 to 1, where 1 indicates the highest erosion risk.
- SCIMAP measures relative risk within the analysed catchment.

## Data structure and interpretation
- Results are organized by seasonal maps (Summer, Spring, Autumn, Winter) and by the 13 scenarios listed above.
- For winter climate-change scenarios (5–13), results are presented specifically for winter.

## Visualization and display notes
- When displaying shapefiles with graduated colors, increase the sampling size in the layer symbology to show all data.