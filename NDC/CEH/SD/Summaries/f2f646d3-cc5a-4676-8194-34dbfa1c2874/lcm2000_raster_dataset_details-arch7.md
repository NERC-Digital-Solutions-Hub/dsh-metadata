# 25m raster

- The 25m raster dataset is created by converting land parcels from a vector dataset into a 25m grid. Each cell records the dominant land cover using LCM2000 Subclasses.
- GB and NI metadata (Table 1) includes:
  - GB: 24,400 columns × 48,400 rows; NI: 7,600 columns × 7,200 rows
  - Lower left easting/northing: GB 50,000 m; NI 180,000 m
  - Pixel size: 25 m (both regions)
  - Coordinate systems: GB = British National Grid; NI = Irish National Grid
  - Projections: Transverse Mercator for both
  - Spheroids: GB = Airy; NI = Airy Modified 1849
  - Datums: GB = OSGB 1936; NI = Ireland 1965
  - Pixel centre offset to compute cell centres: +12.5 m in both directions
- Data encoding: LCM2000 Subclass codes are typically floating-point with one decimal place but are stored as unsigned 8-bit bytes by multiplying by 10 (e.g., Water inland 22.1 becomes 221).

- The 25m dataset also provides a crosswalk (Table 3) between Subclass codes and Aggregate classes/codes, enabling interpretation of detailed classes as broader land-cover categories.

- Subclasses and aggregates cover a broad range of land covers, including water bodies, coastal/sea classes, various woodland types, grasslands, arable areas, urban/built-up areas, bare ground, peat bogs, and other habitat types.

- Practical note: The document emphasises the existence of both detailed Subclass classifications (25m) and aggregated classes (1km), with corresponding codes for each.

- The mapping between 25m Subclasses and 1km Aggregate classes provides a consistent framework for translating fine-scale data into coarser summaries.

- The document appears to continue the full crosswalk listing, detailing numerous subclass-to-aggregate relationships and their 1km codes.