# Diffuse agricultural pollution to rivers in Scotland data

## Overview
- Dataset describing diffuse agricultural pollution loads to rivers in Scotland.
- Stored as comma-separated value files (CSV) and designed for GIS mapping to Water Framework Directive (WFD) catchments.

## Data files and structure
- Files:
  - AgLoadsInland_Scotland.csv
  - AgLoadsCoastal_Scotland.csv
- Key purpose: link pollutant loads to WFD catchments via IDs and provide land-use context.

## Key columns and IDs
- INLAND_ID: SEPA ID for inland catchments (from AgLoadsInland_Scotland.csv)
- COASTAL_ID: SEPA ID for coastal catchments (from AgLoadsCoastal_Scotland.csv)
- CATCH_ID: Unique identifier of the WFD river catchment
- Arable_Are: Total arable area (ha)
- Grass_area: Total improved grass area (ha)
- Rough_Area: Total rough grazing area (ha)
- Arable_x: Total load for pollutant x from arable land
- Grass_x: Total load for pollutant x from improved grassland
- Rough_x: Total load for pollutant x from rough grazing land
- Other_x: Total load for pollutant x from other areas (e.g., steadings, tracks and manure storage)

## Pollutants and units
- _P: kg total P per year
- _N: kg NO3-N per year
- _S: kg suspended solids per year
- _F: 10^6 cfu per year
- _N2O: kg N2O per year
- _CH4: kg CH4 per year
- cfu = colony forming units

## GIS integration and mapping
- Pollutant loads can be mapped by joining the CSVs to WFD catchment polygons in a GIS.
- INLAND_ID and COASTAL_ID map to catchment IDs in the WFD catchment feature class or shapefile.

## Data provenance and availability
- WFD catchments dataset not yet published by SEPA, but there is an intention to add it to SEPA’s Environmental data page.

## Reference
- Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.