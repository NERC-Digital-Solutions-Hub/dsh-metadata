# 25m raster

## Overview
- The 25m raster dataset is created by converting land parcels within a vector dataset into a 25m grid.
- Each grid cell records the dominant land cover using LCM2000 Subclasses.
- A crosswalk exists between 25m Subclass codes and 1km Subclass and Aggregate class codes (Table 3).

## Metadata (Great Britain and Northern Ireland)
- Grid dimensions
  - Great Britain: 24,400 columns x 48,400 rows
  - Northern Ireland: 7,600 columns x 7,200 rows
- Lower left origin
  - Great Britain: easting 50,000 m, northing 10,000 m
  - Northern Ireland: easting 180,000 m, northing 280,000 m
- Pixel size
  - 25 m for both Great Britain and Northern Ireland
- Coordinate systems and projection
  - Great Britain: British National Grid; Transverse Mercator
  - Northern Ireland: Irish National Grid; Transverse Mercator
- Spheroid and Datum
  - Great Britain: Airy; OSGB 1936
  - Northern Ireland: Airy Modified 1849; Ireland 1965
- Pixel centre note
  - The listed values refer to the lower-left corner of the lower-left pixel; add 12.5 m to obtain the pixel centre.

## 1km raster
- Created by summarising the 25m raster data within 1km grid cells.
- Grid dimensions
  - Great Britain: 700 columns x 1,300 rows
  - Northern Ireland: 500 columns x 500 rows
- Lower left origin
  - Great Britain: easting 0 m, northing 0 m
  - Northern Ireland: easting 0 m, northing 0 m
- Pixel size
  - 1,000 m (1 km) for both regions
- Coordinate systems and projection
  - Great Britain: British National Grid; Transverse Mercator
  - Northern Ireland: Irish National Grid; Transverse Mercator
- Spheroid and Datum
  - Great Britain: Airy; OSGB 1936
  - Northern Ireland: Airy Modified 1849; Ireland 1965
- Pixel centre note
  - The values refer to the lower-left corner; add 500 m to obtain the pixel centre.

## Subdivision and mapping (Table 3)
- The 25m raster data has two summarisation schemes:
  - By LCM2000 Subclass
  - By LCM2000 Aggregate class
- Cross-scale mapping
  - Table 3 provides the correspondence between 25m Subclass codes (stored as 8-bit bytes by multiplying by 10, e.g., Water (inland) 22.1 becomes 221) and 1km Subclass and Aggregate class codes.
- Example mappings
  - Sea / Estuary (LCM2000 Subclass 22.1) → 25m code 221; 1km code 1; Aggregate class = Oceanic seas
  - Water (inland) → 25m code 131; 1km code 2; Aggregate class = Standing open water
  - Littoral rock/sediment, bog, woodland, grassland, arable categories, urban areas, etc. across many classes
- Encoding detail
  - 25m Subclass codes are floating point with one decimal; stored as unsigned 8-bit bytes (0–255) after multiplying by 10.

## Implications for data governance and use
- Provides a clear, co-ordinated framework for cross-scale data consistency (25m to 1km).
- Enables data discovery and integration through explicit metadata (extents, coordinate systems, datums, projections, and pixel geometry).
- Facilitates efficient storage and cross-scale analyses via the 25m-to-1km crosswalk and encoded subclass codes.