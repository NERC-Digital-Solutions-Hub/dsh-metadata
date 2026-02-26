# Digestate_HF_SoilTemperature_WFPS_v1.csv

## Overview
- Supplement to the supporting documentation for data series referenced in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Data described: Digestate_HF_SoilTemperature_WFPS_v1.csv
- Dataset characteristics: 4 columns, 87,980 rows
- Source: Digestate wheat trial, 2017, Henfaes Research Center, Bangor University
- Spatial context: data cover ten plots; 2.5 cm soil depth
- Purpose for GIS: enable map-based visualization of soil temperature and water-filled pore space by plot over time

## Data structure (columns and units)
- Time: Date and time of day
- Plot numbers: 5, 6, 8, 10, 15, 18, 24, 28, 29, 30
- Soil_temperature_degrees_celcius: soil temperature at 2.5 cm depth (degrees Celsius)
- WFPS_percent: water-filled pore space at 2.5 cm soil depth (percent)

## Temporal and spatial context
- Data are time-series observations corresponding to specific plots
- Depth-specific measurements at 2.5 cm
- Plot identifiers can be linked to plot locations (spatial polygons) for GIS analyses
- Collected during the 2017 digestate wheat trial at Henfaes Research Center

## GIS usage considerations
- Suitable for creating time-enabled maps showing:
  - Spatial variation in soil temperature across plots
  - Spatial variation in WFPS across plots
  - Temporal trends within and between plots
- To map geospatially, link plot numbers to their spatial coordinates or plot polygons
- Consider aggregating or filtering by plot, date/time, and depth if needed

## Data quality and limitations
- Explicit spatial coordinates are not provided; requires reference to plot locations
- Depth is fixed at 2.5 cm; no other depths included
- Units are clearly stated (°C for soil temperature; % for WFPS)
- As a supplement to broader documentation, ensure alignment with the referenced Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf

## Related documentation
- Supplementary data structure details reference the main documentation and dataset naming: Digestate_HF_SoilTemperature_WFPS_v1.csv