# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock (Habitats 1–21, excluding 15 and 20) for 1978, calculated using the 1990 ITE Land Classification.
- Derived from Countryside Survey data (CEH/CEW) and documented through accompanying data products and references.
- Data intended for GIS and map-based analysis to support landscape-scale habitat interpretation.

## Data products
- CS1978_Estimates_by_LC.csv
  - Contains year (YEAR), ITE Land Class (LAND_CLASS), Broad Habitat code (BROAD_HABITAT), Broad Habitat name (BROAD_HABITAT_NAME), Land Class area (LAND_CLASS_AREA in 000s ha), mean area estimate (MEAN_ESTIMATE in 000s ha), lower estimate (LOWER_ESTIMATE), and upper estimate (UPPER_ESTIMATE) with 95% confidence intervals.
  - National estimates of Broad Habitat stock by Land Class for 1978.

- CS78_BH1_17.tif
  - A 1 km resolution raster containing per-pixel percentages for Broad Habitat classes.
  - Each band corresponds to a Broad Habitat class (bands 1–17, excluding band 15 for Inland Rock and excluding 20; see band mapping in documentation).
  - Method: for each Land Class, totals for the area of each Broad Habitat are converted to percentages per 1 km pixel by dividing the Broad Habitat area by the total Land Class area.
  - Pixel size: 1 km; Coordinate system: British National Grid; Projection: Transverse Mercator Great Britain; Extent: OSGB36.

## Data fields and band mapping
- CSV fields (sample): YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha).
- TIFF bands (example mappings): 
  - Band 1 = Broadleaved Mixed and Yew Woodland
  - Band 2 = Coniferous Woodland
  - Band 3 = Boundary and Linear Features
  - Band 4 = Arable and Horticulture
  - Band 5 = Improved Grassland
  - Band 6 = Neutral Grassland
  - Band 7 = Calcareous Grassland
  - Band 8 = Acid Grassland
  - Band 9 = Bracken
  - Band 10 = Dwarf Shrub Heath
  - Band 11 = Fen, Marsh, Swamp
  - Band 12 = Bog
  - Band 13 = Standing Open Waters and Canals
  - Band 14 = Rivers and Streams
  - Band 15 = Inland Rock
  - Band 16 = Urban
  - Note: Bands correspond to Broad Habitat classes; 15 and 16 inclusion aligns with file documentation.

## Spatial properties
- Pixel/grid: 1 km resolution; each pixel represents percentage share of a Broad Habitat within its Land Class context.
- Coordinate system: British National Grid (OSGB36); Projection: Transverse Mercator Great Britain.

## Usage, attribution, and limitations
- All Countryside Survey data must be acknowledged in outputs.
- Acknowledgement text to use: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © CEH. All rights reserved.”
- Data relates to 1978 estimates using the 1990 ITE Land Classification; suitable for historical spatial analyses and cross-wdataset comparisons with care taken for classification differences and temporal gaps.

## References and publications
- Countryside Survey project homepage and methodology resources.
- Wood et al. (2012) Countryside Survey: Measuring Habitat Change Over 30 Years. 1978 Data Rescue – Final Report (CEH/NEC03689).
- Scott (2007) CS Technical Report No.4/07: Statistical methods for generating national estimates from 1 km survey squares.
- Bunce et al. (1996, 1981) ITE Merlewood Land Classification documents and user descriptions.
- Jackson (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- Field mapping and habitat classification methodologies (CS Technical Reports 1/07).