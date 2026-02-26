# UK gridded population at 1 km resolution for 2021

## Overview
- Provides a 1 km x 1 km gridded map of UK population for 2021 (Scotland 2022) at OSGB36 datum.
- Combines Census population data at Output Areas/Data Zones with Land Cover Map 2021 to create a spatially uniform distribution suitable for analyses requiring grid-level population.
- Output: a GeoTIFF raster with cell values representing persons per square kilometre.

## Data sources
- Population by Output Area/Data Zone from:
  - England and Wales: ONS mid-2021/mid-2022 small area population estimates
  - Scotland: 2022 Output Area data
  - Northern Ireland: Geodatabase with DZ data
- Land Cover Map 2021 (GB and NI) at 25 m resolution, used to define urban/suburban land covers
- Boundary data for OA/DZ:
  - England & Wales OA boundaries
  - Scotland OA boundaries (Data Zones)
  - Northern Ireland Data Zones

## Experimental design
- Objective: produce a spatially homogeneous population distribution by allocating OA/DZ populations within a 1 km grid using urban/suburban land as a distribution proxy.
- Urban/suburban mask derived from LCM2021 informs how populations are distributed within OA/DZs, with greater weighting to urban/suburban cells.
- NI LCM2021 reprojected to GB grid using nearest neighbour to maintain consistency.

## Processing steps
1. Create a UK-wide 1 x 1 km target grid in British National Grid (EPSG 27700).
2. Generate urban/suburban mask from LCM2021 (10 x 10 m grid) and prepare fraction-based weightings for each OA/DZ.
3. Spatial intersection of each OA/DZ with the 1 x 1 km grid; reproject NI OA/DZs to match the target grid.
4. For OA/DZs spanning multiple 1 km cells, intersect with urban/suburban mask and compute weighting fractions; ensure each OA/DZ intersects some urban area.
5. Distribute OA/DZ populations to 1 km cells using weight fractions; sum to produce per-cell totals; reformat to raster.
6. Validate: ensure raster totals match official 2021/2022 census totals at country level; total UK population aligns with census totals.

## Quality control
- Totals checked at each processing step to ensure consistency with official census totals.
- R code annotated for transparency and reproducibility of the data pipeline.

## Data structure and output
- Output format: GeoTIFF raster.
- Cell values: persons per square kilometre (population density per grid cell).
- Final product validated to be consistent with UK 2021 census totals.

## Reproducibility, access, and provenance
- Implemented in R (v4.4.1) using terra and sf packages; steps clearly documented for reproducibility.
- Dataset published by NERC Environmental Information Data Centre (EIDC); citation provided (Carnell, Tomlinson, Reis, 2025).
- Data sources and processing steps transparent to enable audit and reuse in policy, public health, and planning analyses.