# 25m raster

- The 25m raster dataset was created by converting land parcels within the vector dataset into a 25-meter grid. Each 25m cell records the dominant land cover using LCM2000 Subclasses.
- The dataset covers Great Britain and Northern Ireland, with metadata detailed in Tables 1 and 2 and related notes.

## Dataset specifications and extents

- Great Britain (GB) 25m raster
  - Columns/width: 24,400
  - Rows/height: 48,400
  - Lower left easting: 50,000 m
  - Lower left northing: 10,000 m
  - Pixel size: 25 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936
- Northern Ireland (NI) 25m raster
  - Columns/width: 7,600
  - Rows/height: 7,200
  - Lower left easting: 180,000 m
  - Lower left northing: 280,000 m
  - Pixel size: 25 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965
- Note: For pixel centre, add 12.5 m to each lower-left value.

## 1km raster overview

- The 1km raster is created by summarising the 25m raster within 1km grid cells.
- Great Britain (GB) 1km raster
  - Columns: 700
  - Rows: 1,300
  - Lower left easting: 0 m
  - Lower left northing: 0 m
  - Pixel size: 1,000 m
  - Coordinate system, projection, spheroid, and datum: same as GB 25m (OSGB 1936, Transverse Mercator, Airy)
- Northern Ireland (NI) 1km raster
  - Columns: 500
  - Rows: 500
  - Lower left easting: 0 m
  - Lower left northing: 0 m
  - Pixel size: 1,000 m
  - Coordinate system, projection, spheroid, and datum: same as NI 25m (Ireland 1965, Transverse Mercator, Airy Modified 1849)

## Classification and encoding

- The 25m data are summarised in two ways:
  - By LCM2000 Subclass
  - By LCM2000 Aggregate class
- Table 3 provides the correspondence between Subclasses and Aggregate classes, including the 1km codes for cross-resolution interpretation.
- Encoding for storage efficiency:
  - LCM2000 Subclass codes are floating-point with one decimal place
  - Codes are multiplied by 10 to store as unsigned 8-bit bytes (0–255)
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster dataset

## Cross-resolution mapping (Table 3)

- The document includes a comprehensive mapping between:
  - Subclass 25m codes and their corresponding 1km codes
  - Aggregate class mappings and their 1km codes
- Representative examples include:
  - Sea / Estuary (Water) and related coastal classes
  - Water (inland), Littoral and Supra-littoral categories
  - Vegetation: broad-leaved/mixed woodland, coniferous woodland, various heath and moor types
  - Grasslands: improved, neutral, acid, fen/marsh, etc.
  - Arable and horticulture categories
  - Suburban/rural developed and Continuous urban (built-up areas)
  - Inland bare ground and other land-cover categories
- The full table enables users to translate 25m Subclass codes to their corresponding 1km and Aggregate class codes for analysis and cross-walking between resolutions.

## Practical usage notes

- Pixel centre conventions:
  - 25m raster: add 12.5 m to the lower-left corner to locate the pixel centre
  - 1km raster: add 500 m to the lower-left corner to locate the pixel centre
- Storage approach:
  - Subclass codes scaled to fit into 0–255 range as 8-bit unsigned integers
- Purpose and use:
  - Provides high-resolution 25m land cover information and a summary 1km product
  - Facilitates efficient storage and cross-resolution analysis
  - Supports translating codes across resolutions via the included mappingTable (Table 3) for end-user interpretation and self-service data exploration