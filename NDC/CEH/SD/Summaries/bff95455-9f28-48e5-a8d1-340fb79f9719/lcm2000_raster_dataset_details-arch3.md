# 25m raster

- Overview
  - Describes the creation of a 25m raster dataset by converting land parcels into a 25m grid and recording the dominant LCM2000 Subclass per grid cell.
  - Separate metadata for Great Britain and Northern Ireland are provided (referred to as Table 1 in the document).
  - A companion 1km raster is created by summarising the 25m data within 1km grid cells (referred to as Table 2).

- Dataset Details
  - 25m raster
    - Great Britain: 24,400 columns × 48,400 rows
    - Northern Ireland: 7,600 columns × 7,200 rows
    - Lower left corner coordinates (easting/northing) and pixel size: 25 m
    - Coordinate systems and projections
      - Great Britain: British National Grid, Transverse Mercator, Spheroid Airy, Datum OSGB 1936
      - Northern Ireland: Irish National Grid, Transverse Mercator, Spheroid Airy Modified 1849, Datum Ireland 1965
    - Note: Pixel center is 12.5 m offset from the reported lower-left corner
  - 1km raster
    - Great Britain: 700 columns × 1,300 rows
    - Northern Ireland: 500 columns × 500 rows
    - Lower left corner coordinates (easting/northing) and pixel size: 1000 m
    - Coordinate systems and projections
      - Great Britain: British National Grid, Transverse Mercator, Spheroid Airy, Datum OSGB 1936
      - Northern Ireland: Irish National Grid, Transverse Mercator, Spheroid Airy Modified 1849, Datum Ireland 1965
    - Note: Pixel center is 500 m offset from the reported lower-left corner

- Classification, Coding, and Storage
  - 25m data uses LCM2000 Subclass codes (numerical, typically floating point with one decimal place)
  - For efficient raster storage, Subclass codes are stored as 8-bit unsigned integers by multiplying by 10 (e.g., Water (inland) Subclass 22.1 becomes 221)
  - Two parallel representations exist:
    - LCM2000 Subclass (25m and 1km codes)
    - LCM2000 Aggregate class (1km code)
  - The document provides a correspondence table (Table 3) linking Subclasses and their 25m and 1km codes to Aggregate classes
  - Examples of classes mentioned include Oceanic seas, Standing open water, Coastal categories (littoral/supra-littoral rooms), various woodland, grassland, arable, urban, and barren categories

- Subclass-to-Aggregate Mapping (Table 3) Highlights
  - Subclasses are mapped to 1km Aggregate classes with corresponding 25m and 1km codes
  - Examples of categories covered:
    - Sea/Estuary, Water (inland), Littoral littoral/rock/sediment, Saltmarsh
    - Habitat types: Montane, Broad-leaved/mixed woodland, Coniferous woodland
    - Land cover types: Improved grassland, Neutral grassland, Arable and horticulture, Suburban/rural developed, Continuous urban, Inland bare ground
  - This mapping enables consistent cross-scale interpretation from 25m to 1km resolution

- Practical Notes for Monitoring Frameworks
  - The datasets provide standardized land-cover information at two resolutions (25m and 1km) for Great Britain and Northern Ireland
  - Detailed metadata supports reproducibility and quality control (grid dimensions, origins, pixel size, coordinate systems, projections, datums, and pixel-centering conventions)
  - The coding approach (scaling Subclass codes to fit 8-bit storage) facilitates efficient storage and processing in monitoring workflows
  - The explicit mapping between Subclasses, aggregate classes, and their codes supports cross-scale analyses and consistent reporting

- Metadata and Documentation References
  - Table 1: Metadata for the 25m raster (grid dimensions, origins, pixel size, coordinate system, projection, spheroid, and datum)
  - Table 2: Metadata for the 1km raster (grid dimensions, origins, pixel size, coordinate system, projection, spheroid, and datum)
  - Table 3: Correspondence between Subclasses (25m), 1km codes, and Aggregate class codes for efficient cross-scale interpretation