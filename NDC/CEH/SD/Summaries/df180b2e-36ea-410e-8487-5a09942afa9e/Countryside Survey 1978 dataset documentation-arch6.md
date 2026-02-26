# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- Version: 1: 1-2-2012
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology
- Purpose: National estimates of Broad Habitat stock by Land Class for 1978, derived using the 1990 ITE Land Classification; plus a PNG-like raster representation of habitat proportions per 1 km pixel.

## Datasets

- CS1978_Estimates_by_LC.csv
  - Contents: National estimates of Broad Habitat stock (Habitats 1-21, excluding 15, 20) for 1978, by Land Class, using the 1990 ITE Land Classification.
  - Key columns:
    - YEAR: Survey year
    - LAND_CLASS: ITE Land Class code
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat name
    - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% CI (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI (000s ha)

- CS78_BH1_17.tif
  - Contents: 1 km pixel raster of Broad Habitat proportions within each Land Class for 1978.
  - Bands (examples):
    - Band 1: Broadleaved Mixed and Yew Woodland
    - Band 2: Coniferous Woodland
    - Band 3: Boundary and Linear Features
    - Band 4: Arable and Horticulture
    - Band 5: Improved Grassland
    - Band 6: Neutral Grassland
    - Band 7: Calcareous Grassland
    - Band 8: Acid Grassland
    - Band 9: Bracken
    - Band 10: Dwarf Shrub Heath
    - Band 11: Fen, Marsh, Swamp
    - Band 12: Bog
    - Band 13: Standing Open Waters and Canals
    - Band 14: Rivers and Streams
    - Band 15: Inland Rock
    - Band 16: Urban
  - Pixel size: 1 km
  - Coordinate system: British National Grid (OSGB36), Transverse Mercator GB

## Data Provenance and Licensing
- Data origin: Countryside Survey (CS) datasets, owned by NERC - Centre for Ecology & Hydrology.
- Acknowledgement required on all copies, publications, and presentations:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Technical Details
- Timeframe: Estimates based on 1978 survey using 1990 ITE Land Classification.
- Formats:
  - CSV: tabular national estimates by Land Class and Broad Habitat.
  - TIFF: geospatial raster with 1 km pixels representing Broad Habitat proportions per Land Class.
- Spatial context:
  - Raster bands map to Broad Habitat classes; each pixel expresses proportion of a Land Class covered by a Broad Habitat.
  - Projections and extent aligned to British National Grid (OSGB36).

## Data Quality and Considerations
- Historical data caveats:
  - 1978 data tied to 1990 Land Classification; potential harmonisation issues with newer classifications.
  - National estimates include 95% confidence intervals (lower/upper estimates) to reflect sampling uncertainty.
- Data interpretation:
  - CSV provides aggregated area estimates (000s ha) by Land Class and Broad Habitat.
  - TIFF provides spatial distribution of Broad Habitat proportions within each Land Class, enabling map-based analyses and visualization.

## How to Use and Integrate
- Potential uses:
  - Spatial mapping of Broad Habitat distribution across Great Britain.
  - Aggregating to total Broad Habitat area by region, policy area, or administrative unit.
  - Combining with other spatial datasets to assess habitat change, habitat connectivity, or policy impacts.
- Data integration tips:
  - Join CSV and TIFF via LAND_CLASS and BROAD_HABITAT where applicable.
  - Convert units from 000s ha to ha or km2 as needed.
  - Align to GB coordinate systems when overlaying with other layers.
- Data quality workflow:
  - Verify LAND_CLASS mappings against the ITE classification references.
  - Use the 95%CI fields (LOWER_ESTIMATE, UPPER_ESTIMATE) for uncertainty analyses.

## References and Further Reading
- Countryside Survey Website (general project overview and methodologies)
- Wood et al. 2012: Countryside Survey: Measuring Habitat Change Over 30 Years. 1978 Data Rescue - Final Report
- Scott 2007: CS Technical Report No.4/07 – Statistical methods for national estimates
- Bunce et al. 1996/1981: ITE Merlewood Land Classification of Great Britain and related preliminaries
- Jackson 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification