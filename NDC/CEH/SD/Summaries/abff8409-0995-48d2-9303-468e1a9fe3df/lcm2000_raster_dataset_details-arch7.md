# 25m raster

## Overview
- Describes a land-cover raster dataset created by converting vector land parcels to a 25-meter grid.
- Each 25m cell stores the dominant land cover using LCM2000 Subclasses.
- Includes metadata for Great Britain (GB) and Northern Ireland (NI), plus a mapping to 1km rasters and aggregate classes.

## 25m raster details (GB vs NI)
- GB grid: 24,400 columns × 48,400 rows; NI grid: 7,600 columns × 7,200 rows.
- Lower left corner coordinates (easting, northing):
  - GB: 50,000 m Easting, 10,000 m Northing
  - NI: 180,000 m Easting, 280,000 m Northing
- Pixel size: 25 m (both GB and NI)
- Coordinate systems:
  - GB: British National Grid; Projection: Transverse Mercator; Spheroid: Airy; Datum: OSGB 1936
  - NI: Irish National Grid; Projection: Transverse Mercator; Spheroid: Airy Modified 1849; Datum: Ireland 1965
- Note: The values refer to the lower-left corner of the lower-left pixel; to obtain the pixel centre, add 12.5 m to each coordinate.

## 1km raster details (GB vs NI)
- Created by summarising the 25m raster data within 1km grid.
- GB 1km raster: 700 columns × 1,300 rows; NI 1km raster: 500 columns × 500 rows.
- Lower left corner coordinates:
  - GB: 0 m Easting, 0 m Northing
  - NI: 0 m Easting, 0 m Northing
- Pixel size: 1,000 m (1 km) for both GB and NI
- Coordinate systems:
  - GB: British National Grid; Projection: Transverse Mercator; Spheroid: Airy; Datum: OSGB 1936
  - NI: Irish National Grid; Projection: Transverse Mercator; Spheroid: Airy Modified 1849; Datum: Ireland 1965
- Note: For the pixel centre in 1km rasters, add 500 m to the lower-left corner values.

## Data coding and storage
- 25m Subclass codes are typically floating point with one decimal place.
- To optimize storage in raster format, codes are multiplied by 10 and stored as unsigned 8-bit bytes (0–255).
- Example: Water (inland) Subclass 22.1 becomes 221 in the raster dataset.

## Subclass and 1km mapping (Table 3)
- The 25m Subclass codes correspond to 1km codes and to Aggregate class codes for efficient storage and analysis.
- The table provides a mapping across categories such as:
  - Sea / Estuary; Water (inland); Littoral rock; Littoral sediment; Saltmarsh; Supra-littoral rock/sediment
  - Terrestrial habitats: Bog (deep peat); Dense/open dwarf shrub heath; Montane habitats; Broad-leaved/mixed woodland; Coniferous woodland
  - Grasslands: Improved, Neutral, Setaside, Bracken, Calcareous, Acid grassland, Fen/marsh/swamp
  - Arable and horticulture: Arable cereals, Arable horticulture, Arable non-rotational
  - Suburban / urban and built-up areas
  - Inland bare ground
- The table links each Subclass 25m code (e.g., 221 for Sea/Estuary) to the corresponding 1km code and the Aggregate class code (e.g., Oceanic seas, 1 km code 10).

## Examples of representative mappings
- Sea / Estuary
  - 25m code: 221
  - 1km code: 1
  - Aggregate class: Oceanic seas
  - 1km code: 10
- Water (inland)
  - 25m code: 131
  - 1km code: 2
  - Aggregate class: Standing open water
  - 1km code: 8
- Broad-leaved / mixed woodland
  - 25m code: 11
  - 1km code: 12
  - Aggregate class: Broad-leaved / mixed woodland
  - 1km code: 1
- Continuous urban
  - 25m code: 172
  - 1km code: 25
  - Aggregate class: Built up areas and gardens
  - 1km code: 7

## Implications for GIS work
- The 25m raster provides high-resolution, land-cover detail suitable for detailed GIS analysis and map production.
- The 1km raster enables broader-scale analyses and more efficient storage/processing.
- The 25m-to-1km mappings (and associated aggregate classes) facilitate consistent classification across scales.
- Data packaging considerations include handling different resolutions and ensuring consistent datums/projections across GB and NI regions.