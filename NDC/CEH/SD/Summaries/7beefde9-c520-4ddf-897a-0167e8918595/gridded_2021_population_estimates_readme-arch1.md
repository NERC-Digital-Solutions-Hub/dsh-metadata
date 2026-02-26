# UK gridded population at 1 km resolution for 2021 based on Census 2021/2022 and Land Cover Map 2021

- Purpose: Produce a consistent 1 km × 1 km gridded population dataset for the UK by spatially distributing census population counts (Output Areas and Data Zones) within a 1 km grid using land-cover-based urban/suburban masking.
- Product: A GeoTIFF raster at 1 km resolution with population counts (persons per grid cell) for the UK for the 2021 census year (2022 for Scotland).

## Data sources

- Population inputs (Output Areas/Data Zones):
  - England and Wales: Office for National Statistics 2021/2022 small-area population estimates
  - Northern Ireland: NISRA geography/geodatabase
  - Scotland: Scotland census outputs (2022 data)
- Land Cover Map 2021 (LCM2021):
  - Great Britain: 25 m grid of land cover classes (urban/suburban used as residential proxy)
  - Northern Ireland: 25 m LCM2021
- Boundaries for OA/DZ:
  - England & Wales OA boundaries
  - Scotland Data Zones
  - Northern Ireland Data Zones
- Tools: R (version 4.4.1) with terra and sf packages

## Methods (step-by-step)

- Step 1: Create a 1 × 1 km target grid across the UK in the British National Grid (OSGB36, EPSG 27700).
- Step 2: Download and prepare LCM2021 at 10 × 10 m, identify urban/suburban cells to form an urban/suburban mask; project NI LCM2021 to GB grid using nearest neighbor.
- Step 3: Spatially intersect each OA/DZ boundary with the 1 × 1 km grid; reproject Northern Ireland OA/DZs to match the target grid.
- Step 4: For OA/DZs spanning multiple 1 × 1 km cells (majority of cases), intersect OA/DZ boundaries with the 10 m × 10 m urban/suburban mask, aggregate urban/suburban counts to 1 × 1 km cells, and compute the fractional weighting for each intersecting grid cell.
- Step 5: Distribute OA/DZ populations across 1 × 1 km grid cells using the computed weights, then sum by 1 × 1 km cell to create the gridded product.
- Step 6: Validate by ensuring the sum of the gridded population matches the original OA/DZ totals and official census totals; provide transparent, annotated R code for reproducibility.

## Quality control and validation

- Totals checked at each step to ensure consistency with official 2021/2022 census totals.
- Final product demonstrated to be consistent with UK census totals; detailed QC checks and annotated code provided to enable auditability.

## Data structure and format

- Output format: GeoTIFF (.tif)
- Cell value: persons per square kilometer (population density per grid cell)
- Spatial reference: 1 km × 1 km grid on OSGB36 (British National Grid)

## Key outputs and notes

- The dataset combines census population data (OA/DZ) with Land Cover Map 2021 urban/suburban classes to achieve spatially homogeneous population distribution.
- Totals by country (for cross-checking):
  - England: 56,490,284
  - Wales: 3,107,463
  - Scotland: 5,440,284
  - Northern Ireland: 1,903,168
  - UK total: 66,941,199
- The approach ensures alignment with official census totals at each processing stage and emphasizes reproducibility through documented processing steps and code.