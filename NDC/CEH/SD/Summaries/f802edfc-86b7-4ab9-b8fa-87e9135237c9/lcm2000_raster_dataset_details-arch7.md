# 25m raster

## Overview
- The 25m raster converts land parcels from the vector dataset into a 25m grid, recording the dominant land cover at each cell using LCM2000 Subclasses.
- Separate metadata and grids exist for Great Britain (GB) and Northern Ireland (NI).

## 25m raster metadata
- GB: 24,400 columns × 48,400 rows; NI: 7,600 columns × 7,200 rows
- Lower left corner (easting/northing): GB 50,000 m / 10,000 m; NI 180,000 m / 280,000 m
- Pixel size: 25 m (GB and NI)
- Coordinate system / projection:
  - GB: British National Grid; Transverse Mercator; Spheroid Airy; Datum OSGB 1936
  - NI: Irish National Grid; Transverse Mercator; Spheroid Airy Modified 1849; Datum Ireland 1965
- Pixel center offset note: add 12.5 m to each coordinate to reach pixel centre

## 1km raster metadata
- The 1km raster is created by summarising the 25m raster within 1km grid
- GB: 700 columns × 1,300 rows; NI: 500 columns × 500 rows
- Lower left corner (easting/northing): GB 0 m / 0 m; NI 0 m / 0 m
- Pixel size: 1,000 m (1 km) for both GB and NI
- Coordinate system / projection:
  - GB: British National Grid; Transverse Mercator; Spheroid Airy; Datum OSGB 1936
  - NI: Irish National Grid; Transverse Mercator; Spheroid Airy Modified 1849; Datum Ireland 1965
- Pixel center offset note: add 500 m to each coordinate to reach pixel centre

## Subclass to Aggregate class and codes (Table 3)
- 25m data uses LCM2000 Subclass codes (floating point with one decimal) scaled by 10 to store as unsigned 8-bit bytes (0–255)
  - Example: Water (inland) Subclass 22.1 becomes 221
- 1km data uses LCM2000 Aggregate class codes
  - Examples (from mappings): Oceanic seas = 10; Standing open water = 8; Coastal categories (Littoral rock/sediment, etc.) = 9; Broad categories for woodland, grassland, arable, urban, etc. with specific codes
- Table 3 provides the full correspondence between 25m Subclass codes, 1km code, and the Aggregate class descriptions
- Purpose: enable efficient raster storage and cross-resolution interpretation by linking fine-scale Subclasses to coarse-scale Aggregate classes

## Practical notes for GIS work
- Data encoding: 25m Subclass codes are stored as 8-bit integers after scaling (code × 10)
- Resolution relationships: 25m grid captures dominant land cover; 1km grid summarises 25m results for broader analyses
- Coordinate and projection awareness: GB and NI datasets use different national grids and datums; ensure correct reprojection when combining data
- Pixel centre adjustments: apply the specified offsets (12.5 m for 25m, 500 m for 1km) to align with pixel centres during spatial analysis
- Refer to Table 3 for precise code-to-class mappings when interpreting raster values across resolutions