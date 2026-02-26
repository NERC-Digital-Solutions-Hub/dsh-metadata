# UK gridded population at 1 km resolution for 2021

## Overview
- A 1 km x 1 km gridded UK population dataset for 2021 (Scotland 2022) created by distributing Census/Output Area (OA) and Data Zone (DZ) populations using Land Cover Map 2021 urban/suburban classes.
- Produces a consistent, spatially homogeneous population distribution suitable for GIS analyses that require map-like population data.

## Data sources
- Population:
  - England & Wales: 2021 Small Area Population Estimates (mid-2021/mid-2022)
  - Northern Ireland: NI Statistics and Research Agency data
  - Scotland: 2021 Census (2022 outputs)
- Land Cover Map 2021 (LCM2021): GB and Northern Ireland, 25 m resolution; urban/suburban classes used as proxies for residential areas
- Boundaries/shapefiles: Output Areas (England & Wales), Scotland Data Zones, Northern Ireland Data Zones
- Projections:
  - GB grid: OSGB36 (EPSG 27700)
  - NI boundaries reprojected to match GB grid (nearest neighbor)

## Processing workflow (Step 1–Step 6)
- Step 1: Create a 1 x 1 km target grid covering the UK in OSGB36.
- Step 2: Obtain LCM2021 (10 x 10 m cells); generate urban/suburban mask; project NI LCM2021 to GB grid.
- Step 3: Spatially intersect OA/DZ boundaries with the 1 km grid; reproject NI boundaries; assign full OA/DZ population to a single 1 km cell if they intersect only one cell; prepare for weighting if they span multiple cells.
- Step 4: For OA/DZs spanning multiple 1 km cells, intersect with the 10 m urban/suburban mask; sum urban/suburban cells within each 1 km cell to create a fractional weighting (relative share of OA/DZ within each cell); ensure each OA/DZ has some urban/suburban land.
- Step 5: Distribute OA/DZ populations to 1 km cells using the weights; sum by 1 km cell; reform into a raster representing population distribution.
- Step 6: Validate by comparing raster totals to official census totals; ensure consistency with census data; appears visually in accompanying figures.

## Output and data structure
- Final product: GeoTIFF raster
- Cell values: population density (persons per square kilometer) per 1 km grid cell

## Quality control and reproducibility
- Consistency checks: raster totals validated against official 2021/2022 census totals at multiple steps
- Transparent, annotated R code using terra and sf for reproducibility

## Key outputs and validation
- Country totals (consistent with census data):
  - England: 56,490,284
  - Wales: 3,107,463
  - Scotland: 5,440,284
  - Northern Ireland: 1,903,168
  - UK total: 66,941,199
- Final product showcased in a dedicated visualization (Figure 2) of the 1 x 1 km gridded UK population for 2021 (Scotland 2022)

## Practical notes for GIS specialists
- Projection and grid: British National Grid (OSGB36); 1 km grid suitable for raster GIS analyses and spatially explicit health and environmental studies
- Data integration: combines authoritative census totals with land-cover-based urban/suburban masks to produce a more homogeneous spatial population surface than administrative units alone
- Accessibility: dataset published via the NERC Environmental Information Data Centre with a formal citation

## Citation
- Carnell, E.; Tomlinson S.J. and Reis, S. (2025). UK gridded population at 1 km resolution for 2021 based on Census 2021/2022 and Land Cover Map 2021. NERC Environmental Information Data Centre. DOI