# UK gridded population at 1 km resolution for 2021

## Overview
- Delivers a 1 km x 1 km gridded population dataset for the United Kingdom for 2021 (Scotland: 2022) by distributing census-derived populations within a 1 km grid.
- Combines 2021 UK Census population data at Output Areas/Data Zones with Land Cover Map 2021 urban/suburban classes to create a spatially homogeneous population distribution.
- Projection: British National Grid (OSGB36).

## Data sources
- Residential population estimates by OA/DZ (England & Wales, NI, Scotland) from official census/time-series sources (ONS, NISRA, Scotland Census data).
- Land Cover Map 2021 (GB and NI) from UKCEH EIDC at 10 m resolution; urban/suburban classes used as a proxy for residential land cover.
- Census boundary shapefiles for OA/DZ (England & Wales, Scotland, Northern Ireland) from data.gov.uk.
- Final product validated against official 2021/2022 census totals.

## Processing workflow (Methodology)
- Step 1: Create a 1 x 1 km UK target grid in OSGB36.
- Step 2: Download LCM2021 (10 x 10 m) and create an urban/suburban mask; project NI LCM to GB grid via nearest neighbor.
- Step 3: Spatially intersect each OA/DZ with the 1 x 1 km grid; reproject NI OA/DZ to match the grid.
- Step 4: For OA/DZs spanning multiple 1 km cells, intersect with the urban/suburban mask, aggregate urban cells within each OA/DZ, and compute a fractional weighting (Urban/Suburban area fraction of the OA/DZ total).
- Step 5: Distribute OA/DZ populations to 1 km cells using the weightings, sum to produce the final 1 km raster, and reformat as a raster of population density.
- Step 6: Validate by summing the raster and comparing to original OA/DZ totals to ensure consistency with census totals.

## Output details
- Final product: GeoTIFF raster with cell values representing population density (persons per km^2).
- Coverage: United Kingdom at 1 km resolution, based on 2021 Census data (2022 for Scotland) and LCM2021.

## Quality control
- Totals checked at steps 4–6 to ensure alignment with official census totals.
- Reproducible workflow with annotated R code (see below).

## Reproducibility and data structure
- Data processing implemented in R (R 4.4.1) using terra and sf packages; steps are documented for transparency.
- Data validation visuals and tables accompany the process (e.g., example OA in Northern Ireland and associated weighting details).
- Data structure: GeoTIFF (.tif) where each cell encodes population density.

## Data access and attribution
- Data cited as: Carnell, E.; Tomlinson S.J.; Reis, S. (2025). UK gridded population at 1 km resolution for 2021 based on Census 2021/2022 and Land Cover Map 2021. NERC Environmental Information Data Centre. DOI.
- Final dataset is designed to support exploration and analysis by data users, enabling self-serve population data at a consistent spatial scale.

## Key outputs and totals
- UK total population (2021): 66,941,199
  - England: 56,490,284
  - Wales: 3,107,463
  - Scotland: 5,440,284
  - Northern Ireland: 1,903,168
- The dataset is designed to be consistent with official census totals, ensuring reliability for downstream analyses and data products.