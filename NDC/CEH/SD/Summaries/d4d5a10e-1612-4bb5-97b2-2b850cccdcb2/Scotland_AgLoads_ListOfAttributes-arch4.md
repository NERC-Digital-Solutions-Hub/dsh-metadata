# Diffuse agricultural pollution to rivers in Scotland data

## Overview
- Data stored as two CSV files: AgLoadsInland_Scotland.csv and AgLoadsCoastal_Scotland.csv
- Designed to be mapped to Water Framework Directive (WFD) catchment polygons for Scotland using ID fields
- WFD catchments dataset is not published by SEPA yet; SEPA plans to add it to its Environmental data page

## Data structure and identifiers
- Files and IDs
  - INLAND_ID: SEPA ID for inland catchments (from AgLoadsInland_Scotland.csv)
  - COASTAL_ID: SEPA ID for coastal catchments (from AgLoadsCoastal_Scotland.csv)
  - CATCH_ID: Unique WFD catchment identifier
- Geography linkage
  - INLAND_ID/COASTAL_ID map to catchment or waterbody IDs in the WFD catchment feature class or shapefile

## Fields and land use metrics
- Land area fields (ha)
  - Arable_Are: Total arable area
  - Grass_area: Total improved grass area
  - Rough_Area: Total rough grazing area
- Load fields by land type
  - Arable_x: Total pollutant load from arable land for pollutant x
  - Grass_x: Total pollutant load from improved grassland for pollutant x
  - Rough_x: Total pollutant load from rough grazing land for pollutant x
  - Other_x: Total pollutant load from other areas (e.g., steadings, tracks, manure storage) for pollutant x

## Pollutants and units
- _P: kg total phosphorus per year
- _N: kg NO3-N per year
- _S: kg suspended solids per year
- _F: 10^6 colony-forming units (cfu) per year
- _N2O: kg N2O per year
- _CH4: kg CH4 per year
- Note: cfu = colony forming units

## Mapping and integration
- Geography: Join the INLAND_ID/COASTAL_ID to the WFD catchment polygons to enable GIS mapping of diffuse pollution loads
- WFD catchments are the linkage to broader regulatory and environmental frameworks

## Publication status and accessibility
- The WFD catchment dataset is not yet published by SEPA
- SEPA intends to publish the catchment dataset on its Environmental data page in the future

## References
- Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.