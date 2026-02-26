# 25m raster

- The raster 25m dataset was created by converting land parcels within the vector dataset into a 25m grid. Each grid cell records the dominant land cover using LCM2000 Subclasses.
- Great Britain (GB) details: 24,400 columns by 48,400 rows; lower left easting 50,000 m, lower left northing 10,000 m; pixel size 25 m; coordinate system British National Grid; projection Transverse Mercator; spheroid Airy; datum OSGB 1936.
- Northern Ireland (NI) details: 7,600 columns by 7,200 rows; lower left easting 180,000 m, lower left northing 280,000 m; pixel size 25 m; coordinate system Irish National Grid; projection Transverse Mercator; spheroid Airy Modified 1849; datum Ireland 1965.
- Pixel center convention: add 12.5 m to lower-left corner coordinates to obtain pixel centers.

## 1km raster

- The LCM2000 raster 1km data were created by summarising the 25m raster within a 1km grid.
- GB details: 700 columns by 1,300 rows; NI details: 500 columns by 500 rows; lower left easting/northing = 0 m; pixel size 1000 m; coordinate systems and projections same as 25m (GB: OSGB 1936, NI: Ireland 1965; Transverse Mercator).
- Pixel center convention: add 500 m to lower-left corner coordinates to obtain pixel centers.

## Classification and encoding

- The 25m data are summarised in two ways: by LCM2000 Subclass and by LCM2000 Aggregate class.
- For efficient storage in raster format, LCM2000 Subclass codes (floating point with one decimal place) are multiplied by 10 and stored as unsigned 8-bit bytes (0–255). Example: Water (inland) Subclass code 22.1 becomes 221.

## Table 3: Subclass to 1km and Aggregate class mappings (highlights)

- Example: Sea / Estuary
  - 25m Subclass code: 221
  - 1km code: 1
  - Aggregate class code: 10 (Oceanic seas)
- Example: Water (inland)
  - 25m Subclass code: 131
  - 1km code: 2
  - Aggregate class code: 8 (Standing open water)
- Example: Littoral rock
  - 25m Subclass code: 201
  - 1km code: 3
  - Aggregate class code: 9 (Coastal)
- Example: Montane habitats
  - 25m Subclass code: 151
  - 1km code: 11
  - Aggregate class code: 6 (Mountain, heath, bog)
- Example: Broad-leaved / mixed woodland
  - 25m Subclass code: 11
  - 1km code: 12
  - Aggregate class code: 1 (Broad-leaved / mixed woodland)

Notes:
- The table provides the correspondence between LCM2000 Subclass codes (25m), their 1km codes, and Aggregate class codes for each land cover type, enabling interpretation across resolutions and classifications.

## Practical considerations

- The 25m raster offers a detailed, dominant-land-cover representation derived from parcel-level data.
- The 1km raster provides a summary suitable for broader-scale analyses.
- The encoding scheme (0–255) facilitates compact storage and transfer, but requires the decoding step (dividing by 10) to recover the original Subclass values.
- Users should apply the pixel center offsets when aligning or overlaying with other spatial datasets.

## Summary for data use

- Two aligned rasters (25m and 1km) cover GB and NI with consistent coordinate systems and projection types, enabling multi-resolution analysis.
- The dataset uses the LCM2000 classification with explicit mappings between Subclass, 1km code, and Aggregate class, supporting both detailed and summary analyses.
- The explicit center-point offsets (12.5 m for 25m, 500 m for 1km) are essential for precise spatial alignment.