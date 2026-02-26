# 25m raster

- The 25m raster dataset converts land parcels from a vector dataset into a 25-meter grid, recording the dominant land cover using LCM2000 Subclass codes. It covers Great Britain and Northern Ireland, with a detailed metadata table (Table 1) describing resolution, extents, coordinate systems, and datum.

- Dataset dimensions and extents
  - Great Britain: 24,400 columns × 48,400 rows
  - Northern Ireland: 7,600 columns × 7,200 rows
  - Lower left corner coordinates vary by region; pixel size is 25 m
  - Great Britain: British National Grid (OSGB 1936); Northern Ireland: Irish National Grid (Ireland 1965)
  - Projections: Transverse Mercator for both regions; Spheroids: Airy (Great Britain) / Airy Modified 1849 (Northern Ireland)
  - Pixel center offset: add 12.5 m to corner coordinates

- 1km raster
  - The LCM2000 1km raster is created by summarising the 25m raster data within 1km grid cells
  - Great Britain: 700 columns × 1,300 rows; Northern Ireland: 500 × 500
  - Pixel size: 1,000 m
  - Coordinate systems, projection, and datums mirror the 25m dataset (Great Britain: OSGB 1936; Northern Ireland: Ireland 1965)

- Encoding of 25m data
  - LCM2000 Subclass codes (normally floating point with one decimal) are stored as unsigned 8-bit integers by multiplying by 10
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster

- Subclass-to-Aggregate and 1km codes (Table 3)
  - The document provides a correspondence between:
    - LCM2000 Subclasses (25m codes)
    - LCM2000 Subclasses (1km codes)
    - LCM2000 Aggregate classes
  - Examples of mappings:
    - Sea / Estuary (Subclass 25m code 221) → 1km code 10 → Oceanic seas
    - Water (inland) (25m code 131) → 1km code 8 → Standing open water
    - Littoral rock (25m code 201) → 1km code 9 → Coastal
    - Saltmarsh (25m code 212) → 1km code 9 → Coastal
    - Montane habitats (25m code 151) → 1km code 11 → Mountain, heath, bog
    - Broad-leaved / mixed woodland (25m code 11) → 1km code 12 → Broad-leaved / mixed woodland
    - Coniferous woodland (25m code 21) → 1km code 13 → Coniferous woodland
    - Arable cereals (25m code 41) → 1km code 21 → Arable cereals
    - Arable/horticulture (25m code 42) or Arable non-rotational (43) → 1km codes 22 or 23 → Arable and horticulture
    - Suburban / rural developed (25m code 171) → 1km code 24 → Built up areas and gardens
    - Continuous urban (25m code 172) → 1km code 25 → Built up areas and gardens

- Important notes
  - The 25m codes are represented as decimal values and stored as 8-bit integers after scaling by 10
  - For pixel center calculations, add 12.5 m (25 m pixel) or 500 m (1 km pixel) to the lower-left corner values, as indicated in the notes

- Relevance for data use and support
  - Provides a clear pathway to convert between high-resolution (25m) and aggregated (1km) land cover rasters
  - Includes a comprehensive code map to interpret and translate land cover types across resolutions
  - Facilitates data product creation (e.g., dashboards or reports) by enabling consistent aggregation and labeling of land cover classes
  - Highlights data encoding practices and spatial reference details critical for data quality checks, interoperability, and replication across projects