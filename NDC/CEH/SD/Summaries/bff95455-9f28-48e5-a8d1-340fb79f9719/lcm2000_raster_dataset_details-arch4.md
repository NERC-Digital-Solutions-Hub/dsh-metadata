# 25m raster

## Overview
- Describes the 25m raster dataset created by converting land parcels within a vector dataset into a 25m grid.
- Each 25m grid cell records the dominant land cover using LCM2000 Subclasses.
- The document includes metadata details, a 1km raster derived from the 25m data, and a mapping table between Subclasses and Aggregates.

## 25m raster details (Great Britain and Northern Ireland)
- Great Britain: 24,400 columns x 48,400 rows
- Northern Ireland: 7,600 columns x 7,200 rows
- Pixel size: 25 m (both GB and NI)
- Lower left easting/northing: GB 50,000 m / 10,000 m; NI 180,000 m / 280,000 m
- Coordinate system and projection:
  - GB: British National Grid, Transverse Mercator, Spheroid Airy, Datum OSGB 1936
  - NI: Irish National Grid, Transverse Mercator, Spheroid Airy Modified 1849, Datum Ireland 1965
- Pixel centre adjustment note: add 12.5 m to lower-left coordinates to obtain pixel centre

## 1km raster details (GB and NI)
- Created by summarising the 25m raster within 1km grid
- Great Britain: 700 columns x 1,300 rows
- Northern Ireland: 500 columns x 500 rows
- Pixel size: 1000 m (1 km) for both GB and NI
- Coordinate system and projection: same as the 25m data (GB National Grid; NI Irish National Grid; Transverse Mercator; corresponding spheroids and datums)
- Pixel centre adjustment note: add 500 m to lower-left coordinates to obtain pixel centre

## Subclass to Aggregate mapping (Table 3)
- The 25m LCM2000 Subclass codes (scaled for storage) map to 1km Subclass codes and to LCM2000 Aggregate class codes and names
- Encoding note: LCM2000 Subclass codes are floating point with one decimal place and stored as unsigned 8-bit integers by multiplying by 10 (0-255)
- Examples of mappings:
  - Sea/Estuary
    - 25m Subclass code: 221 (22.1 × 10)
    - 1km Subclass code: 1
    - Aggregate class: Oceanic seas
    - 1km Aggregate code: 10
  - Water (inland)
    - 25m Subclass code: 131 (13.1 × 10)
    - 1km Subclass code: 2
    - Aggregate class: Standing open water
    - 1km Aggregate code: 8
  - Littoral rock
    - 25m Subclass code: 201
    - 1km Subclass code: 3
    - Aggregate class: Coastal
    - 1km Aggregate code: 9
  - Littoral sediment
    - 25m Subclass code: 211
    - 1km Subclass code: 4
    - Aggregate class: Coastal
    - 1km Aggregate code: 9
  - Saltmarsh
    - 25m Subclass code: 212
    - 1km Subclass code: 5
    - Aggregate class: Coastal
    - 1km Aggregate code: 9
  - Supra-littoral rock
    - 25m Subclass code: 181
    - 1km Subclass code: 6
    - Aggregate class: Coastal
    - 1km Aggregate code: 9
  - Montane habitats
    - 25m Subclass code: 151
    - 1km Subclass code: 11
    - Aggregate class: Mountain, heath, bog
    - 1km Aggregate code: 6
  - Broad-leaved / mixed woodland
    - 25m Subclass code: 11
    - 1km Subclass code: 12
    - Aggregate class: Broad-leaved / mixed woodland
    - 1km Aggregate code: 1
  - Coniferous woodland
    - 25m Subclass code: 21
    - 1km Subclass code: 13
    - Aggregate class: Coniferous woodland
    - 1km Aggregate code: 2
  - Improved grassland
    - 25m Subclass code: 51
    - 1km Subclass code: 14
    - Aggregate class: Improved grassland
    - 1km Aggregate code: 4
  - Neutral grassland
    - 25m Subclass code: 61
    - 1km Subclass code: 15
    - Aggregate class: Semi-natural grassland
    - 1km Aggregate code: 5
  - Arable cereals
    - 25m Subclass code: 41
    - 1km Subclass code: 21
    - Aggregate class: Arable and horticulture
    - 1km Aggregate code: 3
- The table provides full coverage across many land-cover types, establishing cross-resolution consistency between 25m and 1km representations

## Data governance and implementation notes
- The dataset supports cross-resolution analysis (25m vs 1km) and cross-GB/NI coverage
- Metadata and the mapping table are essential for data discovery, integration, and correct interpretation of land-cover classes
- Storage optimization: Subclass codes are scaled to fit 0-255 for efficient raster storage
- Important coordinate considerations:
  - Pixel centre adjustments are required when converting from lower-left corner coordinates to pixel centres (12.5 m for 25m data; 500 m for 1km data)

## Implications for Data Leaders
- Provides a standardized, comparable land-cover dataset across Great Britain and Northern Ireland at two resolutions
- Enables efficient storage and retrieval through bit-packed subclass codes and explicit mapping to aggregate classes
- Facilitates governance of data products through clear metadata (extents, pixel sizes, coordinate systems, projections, datums, and pixel-centre conventions)
- Supports user-centric data products by documenting the relationship between 25m and 1km representations and by offering a structured mapping between subclass and aggregate classifications
- Highlights the need to manage data standards, metadata completeness, and cross-sector coordination when integrating with wider data ecosystems