# UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015

- Purpose: Produce a 1 km x 1 km gridded population dataset for the UK, with separate residential and workday populations, suitable for map-based analysis and spatial visualization.
- Core approach: Combine 2011 Census Output Area population data with 2015 Land Cover Map land-use classes (Urban/Suburban) to distribute population across a uniform grid, preserving total counts.

## Data sources

- Census 2011 population data for England, Wales, Northern Ireland, and Scotland (downloaded as CSV from ONS).
- Land Cover Map 2015 vector data (Urban and Suburban classes) from CEH.
- Output Area geography extents for England & Wales, Northern Ireland, and Scotland.
- Mapping framework: British National Grid (OSGB36) for initial processing; final clipping to 1 km grid using OSGB63.

## Experimental design and collection

- Goal: Achieve spatially homogeneous population distribution for environmental and health-related analyses by gridding Census data onto a 1 km grid.
- Population types: Residential and workday populations, with workday defined as usual residents aged 16+ at work in the area plus non-working residents in the area.
- Data formats: OA-level population data, land-use polygons, and grid geometry outputs designed for GIS use (SHAPE, CSV, ASCII Grid).

## Processing workflow (FME-based, with ArcGIS for visualization)

- Step 1: Aggregate Census 2011 population data from OA geography (CSV) to OA geography shapefiles; generate QC CSV.
- Step 2: Extract Urban and Suburban land-use types from Land Cover Map 2015 (vector data); output SHP.
- Step 3: Clip land-use polygons to OA geographies; compute clipped polygon areas; store area shares in CSV.
- Step 4: Merge clipped land-use parcels with population data; distribute population by relative area weight of land-use polygons; perform distribution at OA level and then onto 1 km grid cells.
- Step 5: Apply equal weight to land-use types during distribution; assess potential density differences during final 1 km grid aggregation.
- Step 6: Clip Step 4 shapefile to 1 km × 1 km grid (OSGB63); calculate per-cell areas, aggregate land-use polygons within each cell, and compute final population per grid cell. Scale totals to match the UK Census 2011 total, then round results. Outputs: shapefile, ASCII raster, and CSV.

## Calibration, validation, and quality control

- Consistency checks against official 2011 totals performed at each processing step.
- Acknowledged discrepancies due to geography clipping and Land Cover Map timing (LCM 2015 created from pre-2011 data).
- Overall discrepancy: final 1 km grid totals differ from Census total by ~0.47%.
- Scaling factor: applied at Step 5 to align grid total with 63,185,612 UK population (2011), then rounding. Residential-workday difference is small (0.107%), and a uniform scaling factor was applied.
- Quality control: visual inspections and summary statistics at each step; workflow documented for reproducibility.

## Data structure and outputs

- Outputs: ASCII Grid (.asc), ESRI Shapefile, ESRI ASCII Raster, CSV.
- Each grid cell: unique grid_ID, row, column, residential population, and workday population (as integers; final totals scaled to Census values).
- Coordinate system: initial processing with OSGB36; final products aligned to 1 km grid; clipping performed in OSGB63.
- Data products suitable for GIS-based mapping and spatial analyses.

## Practical notes for GIS specialists

- Useful for mapping population exposure, service access, or policy impact analyses at a uniform 1 km resolution.
- The workflow demonstrates a robust approach to reconciling multi-resolution census data with land-use data, including area-weighted distribution and careful calibration to national totals.
- Limitations to consider: land-use data dated 2015 vs. 2011 census, potential emergence of new residential areas not captured by LCM 2015, and minor discrepancies due to boundary and geography clipping.

## Data access and provenance

- Data citation: Reis, S.; Liska, T.; Steinle, S.; Carnell, E.; Leaver, D.; Roberts, E.; Vieno, M.; Beck, R.; Dragosits, U. (2017). UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/0995e94d-6d42-40c18ed4-5090d82471e1

- Nature of the dataset: Population counts per 1 km grid cell (residential and workday), with a transparent, reproducible processing workflow using FME and ArcGIS.