# 25m raster

## Overview
- The 25m raster dataset is produced by converting land parcels from a vector dataset into a 25-meter grid, with each cell recording the dominant land cover as an LCM2000 Subclass.

## Datasets and metadata (Great Britain and Northern Ireland 25m raster)
- Grid dimensions:
  - Great Britain: 24,400 columns × 48,400 rows
  - Northern Ireland: 7,600 columns × 7,200 rows
- Origins:
  - Great Britain lower left easting: 50,000 m; lower left northing: 10,000 m
  - Northern Ireland lower left easting: 180,000 m; lower left northing: 280,000 m
- Pixel size: 25 m (both GB and NI)
- Coordinate systems and projections:
  - Great Britain: British National Grid (OSGB 1936), Transverse Mercator, Spheroid Airy
  - Northern Ireland: Irish National Grid (Ireland 1965), Transverse Mercator, Spheroid Airy Modified 1849
- Pixel centre offset:
  - For GB: add 12.5 m to each coordinate to reach the pixel centre
  - For NI: add 12.5 m to each coordinate to reach the pixel centre

## Datasets and metadata (Great Britain and Northern Ireland 1km raster)
- The 1km raster is created by summarising the 25m raster within 1km cells.
- Grid dimensions:
  - Great Britain: 700 columns × 1,300 rows
  - Northern Ireland: 500 columns × 500 rows
- Pixel size: 1,000 m (1 km) for both GB and NI
- Coordinates, projection, and datums match the 25m dataset:
  - Great Britain: OSGB 1936, British National Grid, Transverse Mercator, Airy spheroid
  - Northern Ireland: Ireland 1965, Irish National Grid, Transverse Mercator, Airy Modified 1849
- Pixel centre offset:
  - For GB: add 500 m to reach the pixel centre
  - For NI: add 500 m to reach the pixel centre

## Subclass and Aggregate class coding and mapping (Table 3)
- The 25m raster uses LCM2000 Subclass codes, typically floating point with one decimal place; to store efficiently in raster format, codes are multiplied by 10 to fit an unsigned 8-bit byte (0–255). Example: Water (inland) Subclass 22.1 becomes 221.
- The 25m data are summarised to the 1km grid in two ways:
  - By LCM2000 Subclass
  - By LCM2000 Aggregate class
- The correspondence table links Subclass codes, 1km Subclass codes, and Aggregate class codes, along with descriptive categories. Examples include:
  - Sea/Estuary
    - 25m Subclass code: 221
    - 1km Subclass code: 1
    - Aggregate class: Oceanic seas
    - Aggregate 1km code: 10
  - Water (inland)
    - 25m Subclass code: 131
    - 1km Subclass code: 2
    - Aggregate class: Standing open water
    - Aggregate 1km code: 8
  - Littoral rock
    - 25m Subclass code: 201
    - 1km Subclass code: 3
    - Aggregate class: Coastal
    - Aggregate 1km code: 9
- The table continues with numerous land-cover types (e.g., saltmarsh, bog, woodland types, various grasslands, arable/crops, built-up areas, etc.), illustrating the cross-scale categorisation scheme and how 25m classes map to 1km classes and to broader aggregate categories.

## Summary of purpose and structure
- The document provides detailed metadata for both 25m and 1km LCM2000 raster datasets covering Great Britain and Northern Ireland.
- It explains the data creation process (conversion from vector to 25m raster and subsequent 1km summarisation), the encoding scheme (scaling Subclass codes for 8-bit storage), and the cross-scale mapping between Subclasses and Aggregate classes.
- This structure supports efficient storage, consistent cross-scale analysis, and clear provenance for environmental monitoring and policy evaluation.