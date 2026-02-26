# LCM2000 25m and 1km Raster Datasets Metadata

## Overview
- Documents two raster products derived from LCM2000 land cover data: a 25-meter raster and a 1-kilometer raster.
- 25m raster records the dominant land cover per 25m cell using LCM2000 Subclasses; 1km raster summarizes the 25m data within 1km cells.
- Metadata covers grid dimensions, extents, coordinate systems, projections, datums, and data encoding.

## 25m raster details
- Created by converting land parcels from a vector dataset into a 25m grid; each grid cell contains the dominant land cover (LCM2000 Subclass).
- Great Britain: 24,400 columns × 48,400 rows; Northern Ireland: 7,600 columns × 7,200 rows.
- Lower left corner coordinates: Great Britain easting 50,000 m, northing 10,000 m; Northern Ireland easting 180,000 m, northing 280,000 m.
- Pixel size: 25 m for both GB and NI.
- Coordinate systems: Great Britain – British National Grid; Northern Ireland – Irish National Grid.
- Projections: Transverse Mercator (GB and NI).
- Spheroids: GB – Airy; NI – Airy Modified 1849.
- Datums: GB – OSGB 1936; NI – Ireland 1965.
- Pixel centre convention: add 12.5 m to lower-left corner coordinates to obtain the pixel centre.

## 1km raster details
- Created by summarising the 25m raster within 1km grid cells.
- Great Britain: 700 columns × 1,300 rows; Northern Ireland: 500 columns × 500 rows.
- Lower left corner coordinates: GB and NI both start at 0 for easting and northing.
- Pixel size: 1,000 m (1 km) for both GB and NI.
- Coordinate systems: GB – British National Grid; NI – Irish National Grid.
- Projections: Transverse Mercator (GB and NI).
- Spheroids: GB – Airy; NI – Airy Modified 1849.
- Datums: GB – OSGB 1936; NI – Ireland 1965.
- Pixel centre convention: add 500 m to lower-left corner coordinates to obtain the pixel centre.

## Subclass and Aggregate class mapping
- The 25m raster can be summarised by LCM2000 Subclass or by LCM2000 Aggregate class.
- Table 3 provides the correspondence between LCM2000 Subclasses (25m) and Aggregate classes (1km), including attribute codes for each land cover type.
- Examples of categories included: Sea/Estuary, Water (inland), Littoral rock/sediment, Saltmarsh, Bog, various heath/woodland types, grasslands, arable land, urban areas, bare ground, etc.
- Each category has a 25m code, a 1km code, and an Aggregate class code (1 km code) used for storage and classification.

## Data encoding and storage
- To optimise raster storage, LCM2000 Subclass codes (usually floating with one decimal) are scaled by 10 and stored as unsigned 8-bit bytes (0–255).
- Example: Water (inland) Subclass 22.1 becomes 221 in the raster dataset.

## Relevance for environmental monitoring
- Provides standardized, provable land cover classifications across GB and NI suitable for monitoring environmental health and policy performance over time.
- Outputs are suitable for clear formats (maps, charts, reports) and can be stored/uploaded to appropriate data portals.
- The standardized encoding and cross-compatibility between 25m and 1km rasters support data integration and broader analyses.

## Key metadata at a glance
- 25m raster (Great Britain): 24,400 × 48,400 grid; 25 m pixel; GB coordinate system OSGB 1936 / British National Grid; projection Transverse Mercator; lower-left origin 50,000 m E, 10,000 m N; pixel-centre offset 12.5 m.
- 25m raster (Northern Ireland): 7,600 × 7,200 grid; 25 m pixel; NI coordinate system Ireland 1965 / Irish National Grid; projection Transverse Mercator; lower-left origin 180,000 m E, 280,000 m N; pixel-centre offset 12.5 m.
- 1km raster (Great Britain): 700 × 1,300 grid; 1,000 m pixel; GB origin 0,0; same coordinate system and projection as 25m; pixel-centre offset 500 m.
- 1km raster (Northern Ireland): 500 × 500 grid; 1,000 m pixel; NI origin 0,0; same coordinate system and projection as 25m NI; pixel-centre offset 500 m.
- Code encoding: LCM2000 Subclass codes multiplied by 10 for storage as unsigned 8-bit integers (0–255). Example: 22.1 → 221.