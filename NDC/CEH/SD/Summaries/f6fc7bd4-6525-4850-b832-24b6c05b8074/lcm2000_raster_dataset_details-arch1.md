# 25m raster

- The 25m raster dataset is created by converting land parcels from the vector dataset into a 25-meter grid. Each cell records the dominant land cover as an LCM2000 Subclass.
- Geographic scope: Great Britain (GB) and Northern Ireland (NI) with separate metadata.

## Datasets and resolution

- 25m raster (primary dataset)
  - GB: 24,400 columns x 48,400 rows
  - NI: 7,600 columns x 7,200 rows
  - Pixel size: 25 m
  - Lower left corner coordinates:
    - GB: easting 50,000 m, northing 10,000 m
    - NI: easting 180,000 m, northing 280,000 m
  - Coordinate systems and projections
    - GB: British National Grid, Transverse Mercator, OSGB 1936, spheroid Airy
    - NI: Irish National Grid, Transverse Mercator, Ireland 1965, spheroid Airy Modified 1849
  - Pixel center offset note: add 12.5 m to lower-left corner values

- 1km raster (derived dataset)
  - GB: 700 columns x 1,300 rows
  - NI: 500 columns x 500 rows
  - Pixel size: 1000 m
  - Lower left corner coordinates:
    - GB: easting 0 m, northing 0 m
    - NI: easting 0 m, northing 0 m
  - Coordinate systems and projections
    - GB: British National Grid, Transverse Mercator, OSGB 1936, spheroid Airy
    - NI: Irish National Grid, Transverse Mercator, Ireland 1965, spheroid Airy Modified 1849
  - Pixel center offset note: add 500 m to lower-left corner values

## 25m code encoding

- Subclass codes (floating point with one decimal place) are stored as 8-bit unsigned integers by multiplying by 10.
  - Example: Water (inland) Subclass 22.1 becomes 221 in the 25m raster.

## Subclass to 1km and Aggregate mappings (Table 3)

- A correspondence table links:
  - LCM2000 Subclass (25m) codes
  - LCM2000 Subclass to 1km codes
  - LCM2000 Aggregate class (land cover categories) to 1km codes
- The 1km codes are grouped into Aggregate classes such as:
  - Oceanic seas
  - Standing open water
  - Coastal categories (littoral rock/sediment, saltmarsh, supra-littoral components)
  - Terrestrial habitats (bog, montane habitats, dwarf shrub heath, various grasslands)
  - Woodlands (broad-leaved/mixed woodland, coniferous woodland)
  - Arable and horticulture (arable cereals, arable horticulture, arable non-rotational)
  - Semi-natural grasslands (neutral/acid, fen/marsh/swamp, setaside)
  - Semi-natural categories like bracken
  - Built-up areas and gardens (suburban/rural developed, continuous urban)
  - Inland bare ground and related mountainous/heath areas
- The table provides specific one-to-one mappings between the 25m Subclass codes and their corresponding 1km codes and Aggregate class codes for each land-cover type (e.g., Sea/Estuary, Water inland, Littoral rock, Inland bare ground, etc.), enabling consistent aggregation from 25m to 1km resolution.

## Key notes for use

- The 25m dataset captures the dominant land cover at fine resolution by subclass, while the 1km raster summarises these into broader Aggregate classes for higher-level analyses.
- The two rasters cover GB and NI with consistent projection frameworks, but distinct coordinate grids and datums:
  - GB: OSGB 1936 (British National Grid)
  - NI: Ireland 1965 (Irish National Grid)
- Data are stored to facilitate efficient raster processing (8-bit encoding for 25m Subclasses; 1km codes provide standardized broad classes).
- The 1km classes are defined to support comparable analysis at a coarser scale, suitable for regional assessments and reporting.