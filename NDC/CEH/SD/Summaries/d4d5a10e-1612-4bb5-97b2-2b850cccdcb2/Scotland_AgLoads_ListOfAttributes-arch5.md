# Data Structure

## Overview
- Data describing diffuse agricultural pollution to rivers in Scotland.
- Stored in two CSV files:
  - AgLoadsInland_Scotland.csv
  - AgLoadsCoastal_Scotland.csv
- Designed to be mappable to GIS by joining with Water Framework Directive (WFD) catchment polygons for Scotland.
- WFD catchments are identified via specific ID columns; SEPA plans to publish the WFD catchment dataset to its Environmental data page.

## Data files and identifiers
- INLAND_ID: SEPA ID for inland catchments (inland file)
- COASTAL_ID: SEPA ID for coastal catchments (coastal file)
- CATCH_ID: Unique WFD river catchment identifier
- These IDs enable linking to WFD catchment features (in a GIS environment)

## Data schema
- Area metrics (hectares):
  - Arable_Are
  - Grass_area
  - Rough_Area
- Pollutant loads by land type:
  - Arable_x, Grass_x, Rough_x, Other_x (total load for pollutant x from each land type)
- Pollutants and units:
  - _P: kg total P per year
  - _N: kg NO3-N per year
  - _S: kg suspended solids per year
  - _F: 10^6 cfu per year
  - _N2O: kg N2O per year
  - _CH4: kg CH4 per year
  - cfu = colony forming units

## GIS mapping and integration
- Data can be joined to WFD catchment polygons using INLAND_ID/COASTAL_ID.
- WFD catchments dataset is not yet published by SEPA; intended to be added to SEPA’s Environmental data page.

## Data publication, metadata and governance
- Files are CSVs with explicit column names, descriptions, and units.
- For data stewardship, ensure:
  - Clear metadata documenting data lineage, units, and the mapping keys (INLAND_ID, COASTAL_ID, CATCH_ID).
  - Consistency of formats across both inland and coastal datasets.
  - Alignment with future WFD catchment publication and any embargoes or dataset availability constraints.

## Practical implications for data stewards
- Prepare for updates: monitor SEPA publication of the WFD catchment dataset to maintain linking capability.
- Maintain provenance and traceability to the 2016 Gooday et al. report (reference) as background for methodology and pollution measures.
- Communicate any limitations due to unpublished WFD data to data users and stakeholders.
- Ensure data quality through validation of IDs, area measures, and pollutant load calculations across both files.

## Challenges and considerations
- Current incomplete picture of user needs regarding how these datasets are consumed within GIS workflows.
- Timely access to data needed for timely mapping and analysis, especially given pending WFD publication.
- Consistency in metadata and alignment between inland and coastal datasets to support interoperable use.

## Reference
- Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.