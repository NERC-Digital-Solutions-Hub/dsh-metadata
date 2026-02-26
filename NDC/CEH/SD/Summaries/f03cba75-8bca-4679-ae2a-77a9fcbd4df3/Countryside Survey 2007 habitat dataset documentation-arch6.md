# Broad Habitat Area Estimates by Land Class for Great Britain

- Broad habitat stock estimates for Great Britain for 2007, derived from the 2007 ITE Land Classification, with national totals (in 000s hectares) and 95% confidence intervals. Freshwater habitats were modelled separately.
- Data originates from Countryside Survey (CS) 2007 and is published by CEH; all data use requires appropriate acknowledgment.

## Data Components

- CS007_Broad_Habitat_Stock.csv
  - YEAR: Survey year
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Description of Broad Habitat
  - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)
  - Notes: Mean estimates may be negative due to the statistical model; treat negative values as 0.

- CS2007_Stock.tif
  - 1 km pixel resolution raster; each pixel contains the mean percentage estimate of habitat for that Broad Habitat within the corresponding Land Class strata.
  - Band-to-Broad Habitat mapping (e.g., Band 2 corresponds to Broad Habitat 2 for Coniferous Woodland; Band 3 for Boundary/Linear Features with Broadleaved/Mixed Woodlands, etc.) – detailed band definitions provided.

## Spatial and Format Details

- Spatial resolution: 1 km (1000 m) pixels
- Coordinate system: British National Grid (OSGB36), Transverse Mercator projection
- Extent: Great Britain
- Data rights: Acknowledgement required; Countryside Survey data owned by NERC CEH; copyright applies

## Usage and Interpretation Tips for Data Support

- How to meet the “understand the ask”: use the CSV for country-wide totals and the TIFF for fine-scale, pixel-level mapping within Land Class strata; combine with land_class_area data to contextualize Broad Habitat stock.
- Data integration ideas:
  - Join CS007_Broad_Habitat_Stock.csv with Land_Class metadata to map MEAN_ESTIMATE and confidence intervals to specific Land Classes and Broad Habitats.
  - Use the 1 km TIFF bands to create spatial maps of habitat distribution across GB, aligned to Land Class strata.
- Quality and interpretation considerations:
  - MEAN_ESTIMATE may be negative; treat as 0 for practical area calculations.
  - Freshwater Broad Habitats use a different statistical model; exercise caution when comparing to terrestrial habitats.
  - Outputs include confidence intervals (LOWER/UPPER_ESTIMATE) to quantify uncertainty.
  - Data represent 2007 conditions; consider temporal relevance for current planning or trend analyses.
- Output ideas for end users:
  - Dashboards showing total Broad Habitat stock by Land Class and by Habitat type (with uncertainty).
  - Maps illustrating spatial distribution of key Broad Habitats across GB.
  - Reports summarizing national totals and regional patterns, with notes on data reliability.

## Acknowledgement and Licensing

- Acknowledgement to include: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Countryside Survey ©; all rights reserved.

## References

- Countryside Survey project/materials and UK results reports (Carey et al., 2008) and related technical reports (Scott, 2007) detailing methodology for generating national estimates from 1 km survey squares.
- Land Classification references: Bunce et al. (1996, 1981) for ITE Merlewood Land Classification.
- Biodiversity Broad Habitat Guidance: Jackson (2000), JNCC Report 307.
- CS Technical Reports: Field Mapping Handbook (2007).