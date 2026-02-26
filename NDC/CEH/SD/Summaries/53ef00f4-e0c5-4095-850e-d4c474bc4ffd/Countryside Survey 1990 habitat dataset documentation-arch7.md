# Broad Habitat Area Estimates by Land Class for Great Britain 1990 Version: 1: 20-1-2014 C. Wood, CEH Lancaster Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- Presents Countryside Survey 1990 estimates of Broad Habitat areas in Great Britain, separated by Land Class (ITE Land Classification) and Broad Habitat (BH) codes (1–17).
- Data are provided as both national stock estimates (CSV) and 1 km raster maps (TIFF), with accompanying metadata.
- Note on scope: freshwater habitats analyzed with a different statistical model; there was no separate Montane (BH15) class in 1990.

## Data resources

- CSV stock data: CS1990_Broad_Habitat_Stock.csv
  - Contents: national estimates of Broad Habitat stock by Land Class (000s ha) and BH (1–17)
  - Columns:
    - YEAR: survey year
    - LAND_CLASS: ITE Land Classification
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: description
    - LAND_CLASS_AREA: total area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: mean area for Broad Habitat by Land Class (000s ha) (may include negative values; treat as 0)
    - LOWER_ESTIMATE: lower 95% CI (000s ha)
    - UPPER_ESTIMATE: upper 95% CI (000s ha)

- Raster stock data: cs1990_stock.tif
  - 1 km pixel resolution; each pixel band represents a Broad Habitat class
  - Bands mapping (example): 
    - Broad Habitat 2, Broad Habitat 1 = Coniferous Woodland (Band 2), etc.
    - Note: No Montane class in 1990; Band 15 = BH16, Band 16 = BH17
  - Pixel values reflect mean percentage estimates of habitat presence within each 1 km square
  - Based on means from 1 km survey squares sampled within each Land Class strata

## Spatial information

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain
- Data use requires acknowledgement of Countryside Survey data owned by NERC-CEH

## Data interpretation and caveats

- MEAN_ESTIMATE values in CSV may be negative due to the statistical model; treat negative values as 0
- Freshwater habitats were modeled separately; caution when comparing across habitat groups
- No 1990 Montane (BH15) class; mapping adjustments: Band 15 corresponds to BH16, Band 16 to BH17
- Data come from combining datasets with different resolutions; when creating products, consider appropriate aggregation or disaggregation strategies

## Usage for GIS specialists

- Map-based analysis: visualize Broad Habitat distribution across Great Britain for 1990 by combining the 1 km raster bands with land-class stratification
- Data integration: join the CSV stock data with raster data for enriched analyses (e.g., linking total stock by Land Class and BH to spatial distribution)
- Uncertainty: incorporate LOWER_ESTIMATE and UPPER_ESTIMATE to convey confidence intervals in map products or in derived statistics
- Data handling: be mindful of potential negative MEAN_ESTIMATE values; set to zero before visualization or analysis
- Classification considerations: use the BH definitions and band mappings to ensure consistent interpretation across datasets

## Data provenance and references

- Acknowledgement and copyright: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © NERC-Centre for Ecology & Hydrology
- Relevant publications and references provided for methodologies and background (e.g., 1990 Countryside Survey reports, ITE Land Classification references, and 2000s technical reports)

## Practical notes for analysts

- Before map production, verify alignment between CSV records and raster bands (ensuring Land Class and BH codes are correctly matched)
- Consider documenting any decisions made when handling negative MEAN_ESTIMATE values or when interpreting 1990-specific band mappings
- Use the cited references to understand the statistical methodologies and any limitations when interpreting 1990 Broad Habitat estimates

## File details at a glance

- CSV: CS1990_Broad_Habitat_Stock.csv
  - Year, Land Class, Broad Habitat, Broad Habitat Name, Land Class Area, Mean Estimate, Lower Estimate, Upper Estimate
- Raster: cs1990_stock.tif
  - 1 km pixel bands, each band corresponds to a Broad Habitat class
  - Band-to-BH mapping includes adjustments for 1990 data (e.g., no BH15)