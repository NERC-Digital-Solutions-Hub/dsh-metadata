# UK gridded population at 1 km resolution for 2021 based on Census 2021/2022 and Land Cover Map 2021

## Purpose and context
- Produces a consistent 1 km × 1 km gridded population dataset for the UK for 2021 (Scotland 2022) by combining census small-area population data with Land Cover Map 2021 to distribute populations within a uniform grid.
- Designed to support environmental health and policy monitoring by enabling spatially uniform population exposure assessments and trend analyses.
- Uses a British National Grid (OSGB36) framework for alignment with national geographic data.

## Data sources
- Population data (Outputs Areas and Data Zones) from:
  - England and Wales: mid-2021/mid-2022 small-area population estimates (ONS)
  - Northern Ireland: geodatabase for 2021 geography (NISRA)
  - Scotland: 2022 output-area data (Scottish Census)
- Land Cover Map 2021 (LCM2021) for Great Britain and Northern Ireland (10 m × 10 m cells; urban/suburban classes used as residential proxies)
- Boundary shapefiles for OA/DZ:
  - England & Wales Output Areas
  - Scotland Output Areas (Data Zones)
  - Northern Ireland Data Zones
- All sources used to create a 1 km gridded population product with totals consistent to official census figures

## Experimental design
- Purpose: provide spatially homogeneous population distribution by overlaying OA/DZ populations onto a 1 km grid using an urban/suburban land-cover mask.
- Key design features:
  - Create a 1 km grid in OSGB36
  - Project and align LCM2021 to the 1 km grid (nearest-neighbour for NI)
  - Intersect OA/DZ boundaries with the 1 km grid
  - For OA/DZs that intersect a single 1 km cell, assign 100% of population to that cell
  - For OA/DZs spanning multiple 1 km cells, distribute population proportionally using the urban/suburban land fraction within each intersecting cell
  - Ensure each OA/DZ spanning multiple cells contains some urban/suburban land coverage
  - Merge OA/DZ populations with their weighted distributions, sum by 1 km cell, and reformat as a raster
  - Validate that the sum of the final raster equals the original census totals

## Data processing workflow
- Implemented in R (R 4.4.1) using terra and sf packages
- Steps:
  - STEP 1: Generate 1 km target grid (OSGB36)
  - STEP 2: Download and prepare LCM2021 at 10 m resolution; create urban/suburban mask
  - STEP 3: Spatial intersection of OA/DZs with 1 km grid; reproject NI as needed
  - STEP 4: For OA/DZs spanning multiple 1 km cells, intersect with urban/suburban mask, compute weights as fraction of OA/DZ total
  - STEP 5: Multiply OA/DZ totals by weights, distribute to 1 km cells, sum within each cell, reformat as raster
  - STEP 6: Validate totals against official census numbers
- Quality control and reproducibility:
  - Totals checked at each step to ensure consistency with official census totals
  - R code annotated for transparency and reproducibility

## Output product and data structure
- Output format: GeoTIFF (.tif)
- Cell values: persons per square kilometre (population density) for each 1 km grid cell
- Final UK totals (consistent with census data):
  - England: 56,490,284
  - Wales: 3,107,463
  - Scotland: 5,440,284
  - Northern Ireland: 1,903,168
  - UK total: 66,941,199

## Reproducibility and accessibility
- Dataset is documented with detailed processing steps, allowing replication
- Citations and DOI information provided for proper data attribution
- Final product is suitable for uploading to data portals and integration with environmental datasets for monitoring and policy evaluation

## Key considerations for environment-focused use
- Provides a consistent, spatially explicit population layer to pair with environmental exposure data (e.g., land use, pollution, climate variables)
- Facilitates standardized monitoring of environmental health indicators and policy performance over time
- Addresses the challenge of increasing dataset value by enabling cross-dataset analyses and broader data accessibility through a single gridded format