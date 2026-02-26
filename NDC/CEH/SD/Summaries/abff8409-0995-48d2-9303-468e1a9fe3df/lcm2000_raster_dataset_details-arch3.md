# 25m raster

## Overview
- The 25m raster dataset is created by converting land parcels into a 25-meter grid, with each cell recording the dominant land cover using LCM2000 Subclasses.

## 25m raster metadata (Great Britain and Northern Ireland)
- Great Britain: 24,400 columns × 48,400 rows; Northern Ireland: 7,600 columns × 7,200 rows.
- Pixel size: 25 m for both regions.
- Coordinate systems: Great Britain uses British National Grid; Northern Ireland uses Irish National Grid.
- Projection: Transverse Mercator for both regions.
- Datums/Spheroids: OSGB 1936 (Great Britain); Ireland 1965 / Airy Modified 1849 (Northern Ireland).

## Pixel origin notes
- The values in tables refer to the lower-left corner of the lower-left pixel.
- To obtain the pixel centre, add 12.5 m to each coordinate for 25m pixels.

## 1km raster (LCM2000 raster at 1 km)
- 1km raster created by summarising the 25m raster data within 1km grid cells.
- Great Britain: 700 columns × 1,300 rows; Northern Ireland: 500 columns × 500 rows.
- Pixel size: 1000 m for both regions.
- Coordinate systems, projections, and datums match the 25m dataset (British National Grid and Irish National Grid; Transverse Mercator; OSGB 1936 and Ireland 1965).

## 25m to 1km correspondence and codes
- To storage efficiency, LCM2000 Subclass codes (floating point with one decimal place) are scaled by 10 and stored as unsigned 8-bit bytes (0–255).
- Example: Water (inland) Subclass 22.1 becomes 221 in the raster.
- The 25m Subclass codes, 1km Subclass codes, and 1km Aggregate class codes are linked in a correspondence table (Table 3).

## Table references and classifications (Table 1–Table 3)
- Table 1: Metadata for the 25m raster dataset (Great Britain and Northern Ireland).
- Table 2: Metadata for the 1km raster dataset (Great Britain and Northern Ireland).
- Table 3: Correspondence between LCM2000 Subclass (25m) codes, LCM2000 Subclass (1km) codes, and LCM2000 Aggregate class codes (e.g., Oceanic seas, Standing open water, Coastal categories, various woodland and grassland classes, arable and urban classes, etc.).

## Data handling and preparation notes
- The raster 25m data have two summarisation pathways: by Subclass and by Aggregate class.
- The mapping enables cross-scale analyses and efficient storage while preserving descriptive land-cover information.

## Relevance for monitoring frameworks
- Provides high-resolution (25m) and aggregated (1km) land-cover representations suitable for environmental health monitoring and policy evaluation.
- Clear metadata structure (extents, coordinate systems, projections, datums) supports data provenance and reproducibility.
- The encoding approach (scaling to 0–255) balances storage efficiency with detailed classification.
- The explicit Subclass-to-1km-to-Aggregate mappings facilitate consistent reporting across scales.
- Notes on pixel origin and coordinate adjustments aid accurate geospatial analyses and alignment with other datasets.