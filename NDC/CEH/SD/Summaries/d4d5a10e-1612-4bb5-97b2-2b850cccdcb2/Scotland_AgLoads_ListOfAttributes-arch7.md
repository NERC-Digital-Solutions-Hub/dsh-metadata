# Data Structure

- The Diffuse agricultural pollution to rivers in Scotland data are stored as comma-separated values in two CSV files: AgLoadsInland_Scotland.csv and AgLoadsCoastal_Scotland.csv.
- GIS mapping approach: join the CSVs to Water Framework Directive (WFD) catchment polygons for Scotland to visualize pollution loads spatially.
- Key identifiers:
  - INLAND_ID: SEPA ID for inland catchments (from AgLoadsInland_Scotland.csv)
  - COASTAL_ID: SEPA ID for coastal catchments (from AgLoadsCoastal_Scotland.csv)
  - CATCH_ID: Unique WFD river catchment identifier
  - Note: WFD catchments dataset is not published by SEPA yet; SEPA intends to add it to its Environmental data page in the future.

- File/columns overview:
  - Arable_Are: Total arable area (ha)
  - Grass_area: Total improved grass area (ha)
  - Rough_Area: Total rough grazing area (ha)
  - Arable_x: Total pollutant load from arable land (per pollutant)
  - Grass_x: Total pollutant load from improved grassland (per pollutant)
  - Rough_x: Total pollutant load from rough grazing land (per pollutant)
  - Other_x: Total pollutant load from other areas (e.g., steadings, tracks, manure storage)

- Pollutants and units:
  - _P: kg total P per year
  - _N: kg NO3-N per year
  - _S: kg suspended solids per year
  - _F: 10^6 cfu per year
  - _N2O: kg N2O per year
  - _CH4: kg CH4 per year
  - cfu = colony forming units

- Data use notes for GIS specialists:
  - Use INLAND_ID and COASTAL_ID to link to corresponding WFD catchment features.
  - When WFD catchments become available, these IDs will provide the crosswalk for accurate spatial joins.
  - Data can be used to create thematic maps of pollutant loads by land type and overall loads across catchments. 

- Reference:
  - Gooday, R.; Anthony, S.; Calrow, L.; Harris, D.; Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.