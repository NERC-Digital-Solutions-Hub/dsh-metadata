# 25m raster

## Overview
- The 25m raster was created by converting land parcels from an underlying vector dataset into a 25-meter grid.
- Each 25m cell records the dominant land cover at that location using LCM2000 Subclasses.

## Dataset Details
- Great Britain (GB)
  - Grid size: 24,400 columns × 48,400 rows
  - Lower left: easting 50,000 m; northing 10,000 m
  - Pixel size: 25 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936
- Northern Ireland (NI)
  - Grid size: 7,600 columns × 7,200 rows
  - Lower left: easting 180,000 m; northing 280,000 m
  - Pixel size: 25 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965
- Note: Values refer to the lower left corner of the lower left pixel; to obtain the pixel centre, add 12.5 m to easting and northing.

## 1km raster
- Created by summarising the 25m raster data within 1km cells.
- GB: 700 columns × 1,300 rows
- NI: 500 columns × 500 rows
- Lower lefts: easting/northing = 0
- Pixel size: 1000 m
- Coordinate systems, projections, and datums match the 25m dataset (GB: OSGB 1936; NI: Ireland 1965)
- Note: For the pixel centre, add 500 m to the lower-left values.

## Coding and storage
- 25m Subclass codes are stored as scaled integers (originally floating point with one decimal place, multiplied by 10 to fit unsigned 8-bit bytes 0–255).
- Example: Water (inland) Subclass code 131 (25m) becomes 1310 in storage? (Note: the document provides an example: 22.1 becomes 221 when stored in raster; interpretation: 22.1 × 10 = 221).

## Subclass to Aggregate mapping (Table 3)
- The 25m Subclasses and 1km Subclasses are linked to Aggregate classes with corresponding 1km codes.
- Example mappings include:
  - Sea/Estuary: 25m Subclass code 221; 1km code 10; Aggregate class Oceanic seas
  - Water (inland): 25m Subclass code 131; 1km code 2; Aggregate class Standing open water
  - Littoral rock / Littoral sediment / Saltmarsh / Supra-littoral rock/sediment: coded similarly with corresponding 1km and Aggregate class values
  - Land cover families include: coastal (littoral), water bodies, bog/peat, various heath and woodland types (broad-leaved/mixed, coniferous, etc.), arable and horticulture, semi-natural grasslands, urban/suburban developments, and bare ground
- This mapping enables translation between 25m detail and 1km generalisations and their associated codes.

## Data governance and use considerations for Data Stewards
- Metadata needs to document:
  - Separate coordinate systems and datums for GB and NI
  - Pixel center offsets (12.5 m for 25m data; 500 m for 1km data)
  - The existence of two summarisation schemes (by Subclass and by Aggregate class) and the corresponding code mappings
- Cross-border harmonisation: GB and NI use different grids, datums, and spheroids; ensure clear provenance and guidance for users transitioning between GB and NI data.
- Storage efficiency: Subclass codes are stored as compact integers; governance should note this encoding for users reinterpreting codes.
- Update and provenance: maintain documentation of the underlying vector data, the rules for deriving the 25m grid, and the rules for aggregating to 1km.
- Accessibility: ensure data portals and catalogs expose both 25m and 1km rasters with consistent metadata and the Subclass-to-Aggregate mappings.
- Usability: provide guidance on how to interpret pixel codes, including pixel-center offsets and how to reproject or resample without misinterpreting class codes.

## Practical implications for implementation
- Users must account for differing coordinate systems, offsets, and datums when integrating GB and NI rasters.
- The dataset supports both detailed (25m Subclass) and generalized (1km Aggregate) views, requiring clear metadata and documentation for appropriate use.
- When storing or transferring, respect the 0–255 encoding range and ensure decoding logic is applied to retrieve the original Subclass values.