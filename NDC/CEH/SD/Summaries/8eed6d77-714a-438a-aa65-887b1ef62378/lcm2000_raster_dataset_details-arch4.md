# 25m raster

## Overview
- The 25m raster dataset records the dominant land cover per 25m grid cell using LCM2000 Subclasses, created by converting land parcels from a vector dataset into a 25m grid.

## 25m raster dataset details (Great Britain and Northern Ireland)
- Dimensions:
  - Great Britain: 24,400 columns x 48,400 rows
  - Northern Ireland: 7,600 columns x 7,200 rows
- Spatial extent references:
  - Great Britain lower left easting: 50,000 m; lower left northing: 10,000 m
  - Northern Ireland lower left easting: 180,000 m; lower left northing: 280,000 m
- Pixel size: 25 m
- Coordinate systems and projections:
  - Great Britain: British National Grid, Transverse Mercator
  - Northern Ireland: Irish National Grid, Transverse Mercator
- Datums and spheroids:
  - Great Britain: OSGB 1936, Airy
  - Northern Ireland: Ireland 1965, Airy Modified 1849
- Pixel centre adjustment: add 12.5 m to corner coordinates to obtain pixel centres

## 1km raster dataset details (derived from 25m data)
- Created by summarising the 25m raster within 1km grid cells
- Dimensions:
  - Great Britain: 700 columns x 1,300 rows
  - Northern Ireland: 500 columns x 500 rows
- Spatial references:
  - Lower left easting/northing: 0 m for both GB and NI
  - Pixel size: 1,000 m
- Coordinate systems and projections:
  - Great Britain: British National Grid, Transverse Mercator
  - Northern Ireland: Irish National Grid, Transverse Mercator
- Datums and spheroids:
  - Great Britain: OSGB 1936, Airy
  - Northern Ireland: Ireland 1965, Airy Modified 1849
- Pixel centre adjustment: add 500 m to corner coordinates to obtain pixel centres

## Data encoding and codes
- Subclass codes (25m) are floating-point with one decimal place; to store efficiently in raster format, they are multiplied by 10 and stored as unsigned 8-bit bytes (0-255)
- Example: Water (inland) Subclass 22.1 becomes 221 in the raster

## Table 3: Subclass to Aggregate class mapping
- Provides the full correspondence between:
  - LCM2000 Subclass 25m codes
  - LCM2000 Subclass 1km codes
  - LCM2000 Aggregate class names
  - Aggregate class 1km codes
- This table links detailed 25m land cover classes to their 1km aggregate representations, enabling cross-scale interpretation and data integration
- Examples (illustrative):
  - Sea / Estuary: 25m code 221 → 1km Aggregate Oceanic seas code 10
  - Water (inland): 25m code 131 → 1km Aggregate Standing open water code 8
  - Littoral rock: 25m code 201 → 1km Aggregate Coastal code 9
  - Various other land cover types (e.g., forests, grasslands, arable, urban) with corresponding 1km codes and names

## Metadata and tables
- Table 1: Metadata information for the 25m raster datasets (Great Britain and Northern Ireland)
- Table 2: Metadata information for the 1km raster datasets (Great Britain and Northern Ireland)
- Table 3: Correspondence between Subclasses and Aggregate classes (as described above)

## Implications for data leadership
- Grounded, traceable data workflow: 25m data serve as the source for 1km summaries, enabling scalable analyses
- Rich metadata support: detailed metadata for both scales enhances discoverability, interoperability, and governance
- Cross-scale usability: explicit subclass-to-aggregate mappings facilitate integration across systems and analyses at different resolutions
- Storage efficiency: 8-bit encoding of subclass codes improves storage and performance for large rasters
- Considerations for data strategy: ensure consistent use of coordinate systems, datums, and encoding schemes; maintain documentation of table mappings to support user needs and reduce interpretation risk