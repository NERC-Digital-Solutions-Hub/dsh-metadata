# 25m raster

## Overview
- The 25m raster dataset is created by converting land parcels from a vector dataset into a 25m grid.
- Each grid cell records the dominant land cover as a LCM2000 Subclass.
- Two regions are covered: Great Britain and Northern Ireland, with metadata provided for each.

## 25m raster details (Great Britain and Northern Ireland)
- Great Britain: 24,400 columns x 48,400 rows.
- Northern Ireland: 7,600 columns x 7,200 rows.
- Lower left easting/northing: GB = 50,000 m / 10,000 m; NI = 180,000 m / 280,000 m.
- Pixel size: 25 m (GB and NI).
- Coordinate system: GB = British National Grid; NI = Irish National Grid.
- Projection: Transverse Mercator (both regions).
- Spheroid: GB = Airy; NI = Airy Modified 1849.
- Datum: GB = OSGB 1936; NI = Ireland 1965.
- Pixel center reference: for the pixel center, add 12.5 m to each lower-left pixel coordinate.

## 1km raster
- The 1km raster is derived by summarising the 25m raster within 1km grid cells.
- Great Britain: 700 columns x 1300 rows.
- Northern Ireland: 500 columns x 500 rows.
- Lower left easting/northing: GB = 0 m / 0 m; NI = 0 m / 0 m.
- Pixel size: 1000 m (1 km) for both regions.
- Coordinate system, projection, spheroid, and datum are the same as the 25m dataset.
- Pixel center reference: for the 1km cell center, add 500 m to each value.

## Subclass vs Aggregate class and coding
- The 25m raster data are summarised in two ways: by LCM2000 Subclass and by LCM2000 Aggregate class.
- A correspondence table (Table 3) maps:
  - LCM2000 Subclass (25m code) to LCM2000 Subclass (1km code) and to LCM2000 Aggregate class (1km code).
- Coding details:
  - Subclass codes are typically floating-point with one decimal place.
  - For efficient storage in raster format, Subclass codes are multiplied by 10 and stored as unsigned 8-bit integers (0-255). Example: Water (inland) Subclass 22.1 becomes 221 in the raster dataset.
- Examples from the mapping (illustrative; full table contains all entries):
  - Sea / Estuary (LCM2000 Subclass 25m code 221) → Sea/Estuary 1km code 1 → Aggregate class Oceanic seas 1km code 10.
  - Water (inland) (25m code 131) → 1km Subclass code 2 → Aggregate class Standing open water 1km code 8.
  - Littoral rock (25m code 201) → 1km Subclass code 3 → Aggregate class Coastal 1km code 9.
  - Bog (deep peat) (25m code 121) → 1km Subclass code 8 → Aggregate class Mountain, heath, bog 1km code 6.
- The full table provides the complete set of mappings between Subclass, 1km Subclass, and 1km Aggregate class codes.