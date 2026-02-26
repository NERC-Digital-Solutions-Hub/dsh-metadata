# 25m raster

## Overview
- The 25m raster records the dominant land cover per grid cell, derived by converting land parcels from a vector dataset into a 25m grid using the LCM2000 Subclasses.
- Two regional datasets are described: Great Britain and Northern Ireland, with metadata detailing grid dimensions, coordinate systems, and pixel geometry.
- A 1km raster is created by summarising the 25m raster within 1km grid cells.

## 25m raster metadata

- Great Britain
  - Columns: 24,400; Rows: 48,400
  - Lower left easting: 50,000 m; Lower left northing: 10,000 m
  - Pixel size: 25 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936
  - Note: Values refer to the lower-left corner of the lower-left pixel; add 12.5 m to get the pixel centre

- Northern Ireland
  - Columns: 7,600; Rows: 7,200
  - Lower left easting: 180,000 m; Lower left northing: 280,000 m
  - Pixel size: 25 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965
  - Note: Values refer to the lower-left corner of the lower-left pixel; add 12.5 m to get the pixel centre

## 1km raster metadata

- Great Britain
  - Columns: 700; Rows: 1,300
  - Lower left easting: 0 m; Lower left northing: 0 m
  - Pixel size: 1,000 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936
  - Note: Values refer to the lower-left corner of the lower-left pixel; add 500 m to get the pixel centre

- Northern Ireland
  - Columns: 500; Rows: 500
  - Lower left easting: 0 m; Lower left northing: 0 m
  - Pixel size: 1,000 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965
  - Note: Values refer to the lower-left corner of the lower-left pixel; add 500 m to get the pixel centre

## Encoding of codes

- To optimise storage, the LCM2000 Subclass codes (normally floating with one decimal place) are multiplied by 10 and stored as unsigned 8-bit bytes (0–255).
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster

## Table 3: Subclass and Aggregate class mappings

- The 25m Subclasses and the 1km codes are linked to corresponding 1km codes and Aggregate class codes for efficient aggregation.
- Examples of mappings:
  - Sea / Estuary (LCM2000 Subclass 25m code 221) maps to 1km code 1 and Aggregate class Oceanic seas (code 10)
  - Water (inland) (25m code 131) maps to 1km code 2 and Aggregate class Standing open water (code 8)
  - Littoral rock (25m code 201) maps to 1km code 3 and Aggregate class Coastal (code 9)
  - Lindet of various habitat types (e.g., bog, heath, woodland) have corresponding 1km codes and Aggregate class mappings (e.g., Mountain, heath, bog; Broad-leaved / mixed woodland; Coniferous woodland; Semi-natural grassland; Built up areas)

- The table establishes the correspondence between the 25m Subclass codes, their 1km equivalents, and the higher-level Aggregate classes, enabling consistent cross-resolution interpretation.

## Data governance and stewardship notes

- Provenance: The 25m dataset is derived from an existing vector dataset by rasterising land parcels to assign a dominant LCM2000 Subclass per 25m cell; the 1km raster is subsequently derived by summarising the 25m raster within 1km cells.
- Metadata scope: Metadata covers grid dimensions, coordinate systems, projections, datums, spheroids, and pixel-centred offsets, ensuring traceability and proper use across platforms.
- Encoding considerations: Subclass values are stored as 8-bit integers after scaling, which is essential for storage efficiency and interoperability; documentation must accompany the dataset to avoid misinterpretation of codes.
- Versioning and updates: While not detailed in the text, the workflow implies the need to document changes in the underlying vector data or classification schemes and to update the rasters accordingly.
- Interoperability: Clear definitions of coordinate systems (GB and NI-specific grids) and pixel-centre offsets facilitate accurate data integration with other geospatial datasets and portals.