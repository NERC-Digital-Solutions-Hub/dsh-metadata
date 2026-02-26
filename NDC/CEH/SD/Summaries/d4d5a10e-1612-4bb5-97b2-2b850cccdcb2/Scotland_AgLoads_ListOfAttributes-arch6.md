# Data Structure

- The Diffuse agricultural pollution to rivers in Scotland data are stored as two CSV files: AgLoadsInland_Scotland.csv (inland catchments) and AgLoadsCoastal_Scotland.csv (coastal catchments).
- Data can be mapped in GIS by joining these CSVs to Water Framework Directive (WFD) catchment polygons for Scotland.
- Mapping uses the identifiers INLAND_ID (inland catchments) and COASTAL_ID (coastal catchments) to align with WFD catchment IDs; CATCH_ID is the unique WFD river catchment identifier.

## Files and identifiers

- AgLoadsInland_Scotland.csv
- AgLoadsCoastal_Scotland.csv
- INLAND_ID: SEPA ID for inland catchments
- COASTAL_ID: SEPA ID for coastal catchments
- CATCH_ID: Unique WFD river catchment identifier

## Columns and meanings

- Arable_Are: Total arable area (ha)
- Grass_area: Total improved grass area (ha)
- Rough_Area: Total rough grazing area (ha)
- Arable_x: Total pollutant load from arable land (per pollutant)
- Grass_x: Total pollutant load from improved grassland (per pollutant)
- Rough_x: Total pollutant load from rough grazing land (per pollutant)
- Other_x: Total pollutant load from other areas (e.g. steadings, tracks, manure storage) (per pollutant)

## Pollutants and units

- _P: kg total P per year
- _N: kg NO3-N per year
- _S: kg suspended solids per year
- _F: 10^6 cfu per year
- _N2O: kg N2O per year
- _CH4: kg CH4 per year
- cfu = colony forming units

## Using the data

- Join the CSV files to WFD catchment shapefiles to visualize pollutant loads by catchment in GIS.
- Use INLAND_ID/COASTAL_ID to align with catchment data; CATCH_ID provides the WFD catchment reference.
- Data can support environmental reporting, policy analysis, and creation of self-serve data products (dashboards, maps, charts) for stakeholders.

## Data source and notes

- References: Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.
- WFD catchments are not published by SEPA yet; SEPA intends to add the WFD catchment dataset to its Environmental data page (link noted in the document).
- This dataset provides annual pollutant loads by land-use type and area, enabling spatial analysis of diffuse agricultural pollution in Scotland.