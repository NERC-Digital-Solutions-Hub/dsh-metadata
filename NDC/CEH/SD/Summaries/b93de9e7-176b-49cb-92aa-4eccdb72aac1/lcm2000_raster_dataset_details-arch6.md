# 25m raster

## Overview
- Presents the 25m raster dataset created by converting land parcels within a vector dataset into a 25m grid.
- Each grid cell records the dominant land cover using LCM2000 Subclasses.
- Provides metadata for Great Britain (GB) and Northern Ireland (NI), plus a crosswalk to 1km rasters and codes.

## 25m raster details (Great Britain and Northern Ireland)
- GB
  - Columns/Width: 24,400
  - Rows/Height: 48,400
  - Lower left easting: 50,000 m
  - Lower left northing: 10,000 m
  - Pixel size: 25 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936
- NI
  - Columns/Width: 7,600
  - Rows/Height: 7,200
  - Lower left easting: 180,000 m
  - Lower left northing: 280,000 m
  - Pixel size: 25 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965
- Note: Pixel centre coordinates are offset by 12.5 m from the lower left corner.

## 1km raster details (summary)
- The 1km raster is derived by summarising the 25m raster data within 1km grid cells.
- GB
  - Columns/Width: 700
  - Rows/Height: 1,300
  - Pixel size: 1000 m
- NI
  - Columns/Width: 500
  - Rows/Height: 500
  - Pixel size: 1000 m
- Coordinate systems, projections, and datums match the 25m rasters (GB OSGB 1936 / NI Ireland 1965; Transverse Mercator; Spheroid Airy / Airy Modified 1849).

## Coding and storage
- LCM2000 Subclass codes (25m) are floating-point numbers with one decimal place but stored as unsigned 8-bit bytes by multiplying by 10.
  - Example: LCM2000 Subclass code for Water (inland) 25m = 131 (stored as 131).
  - Example: LCM2000 Subclass code for Water (inland) in the 25m example 22.1 becomes 221 when stored.
- 1km codes are provided separately for crosswalks to the 1km raster and the Aggregate class.

## Subclass to Aggregate crosswalk (Table 3)
- A correspondence table links:
  - LCM2000 Subclass 25m codes to
  - LCM2000 Subclass 1km codes, and
  - LCM2000 Aggregate class 1km codes.
- This crosswalk enables translation between 25m detail and 1km aggregation, including the following representative categories:
  - Sea / Estuary
  - Water (inland)
  - Littoral rock / Littoral sediment
  - Saltmarsh
  - Supra-littoral rock / sediment
  - Bog / Montane / Heath (various types)
  - Woodland (Broad-leaved/mixed, Coniferous)
  - Grasslands (Improved, Neutral, Calcareous, Acid, Fen/marsh/swamp)
  - Arable and horticulture (cereals, horticulture, non-rotational)
  - Suburban/rural developed
  - Continuous urban
  - Inland bare ground
- Each 25m Subclass code maps to a specific 1km code and to a corresponding Aggregate class code for 1km-wide categorisation.

## Additional notes and implications for data use
- The 25m data is created to capture dominant land cover at a fine resolution and is summarised to 1km for broader analyses.
- The crosswalks allow users to compare or combine analyses at 25m and 1km resolutions.
- Offsets for pixel centres and coordinate system specifics are essential for accurate georeferencing and integration with other datasets.

## Practical implications for data support work
- Facilitates building data products (e.g., land cover maps, dashboards) that enable self-service at both 25m and 1km resolutions.
- Supports data integration across GB and NI with consistent projection and coding schemes.
- Enables verification and transformation of land cover data via the explicit encoding scheme and crosswalks to higher-level aggregates.