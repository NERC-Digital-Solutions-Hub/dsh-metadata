# 25m raster

## Overview
- The 25m raster is created by converting land parcels within a vector dataset into a 25m grid.
- Each grid cell records the dominant land cover using LCM2000 Subclasses.

## 25m raster details (Great Britain)
- Columns: 24,400; Rows: 48,400
- Lower left easting: 50,000 m; Lower left northing: 10,000 m
- Pixel size: 25 m
- Coordinate system: British National Grid; Projection: Transverse Mercator
- Spheroid: Airy; Datum: OSGB 1936

## 25m raster details (Northern Ireland)
- Columns: 7,600; Rows: 7,200
- Lower left easting: 180,000 m; Lower left northing: 280,000 m
- Pixel size: 25 m
- Coordinate system: Irish National Grid; Projection: Transverse Mercator
- Spheroid: Airy Modified 1849; Datum: Ireland 1965

## 1km raster
- Created by summarising the 25m raster within a 1km grid.
- Columns x Rows: Great Britain 700 x 1,300; Northern Ireland 500 x 500
- Lower left easting/northing: 0 m (GB and NI respectively)
- Pixel size: 1000 m
- Coordinate system: Great Britain (British National Grid); Northern Ireland (Irish National Grid)
- Projection: Transverse Mercator
- Spheroid: Airy / Airy Modified 1849; Datum: OSGB 1936 / Ireland 1965

> Note: Values refer to the lower left corner of the lower left pixel. To get the pixel centre, add 12.5 m (GB/NI) or 500 m (1 km) to each value.

## Subclass to Aggregate class mapping
- The 25m raster uses LCM2000 Subclass codes (floating point with one decimal place). For efficient storage, codes are multiplied by 10 and stored as unsigned 8-bit bytes (0–255).
- Example: Water (inland) Subclass 22.1 becomes 221 in the raster.
- Table 3 provides the correspondence between LCM2000 Subclasses and LCM2000 Aggregate classes, including:
  - Subclass codes (25m and 1km)
  - Aggregate class names (e.g., Oceanic seas, Standing open water, Coastal, Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Built up areas and gardens, etc.)
  - 1km codes for Aggregate classes

## Practical considerations for GIS work
- The 25m-to-1km aggregation workflow is essential when moving from high-resolution detail to coarser analyses.
- Data may be stored efficiently using 8-bit encoding, but users should reference the 25m Subclass and 1km Aggregate mappings to interpret classes correctly.
- Ensure coordinate alignment across GB and NI when integrating datasets.
- When mapping coordinates to pixel locations, apply the pixel-centre offset (12.5 m for 25m, 500 m for 1km).