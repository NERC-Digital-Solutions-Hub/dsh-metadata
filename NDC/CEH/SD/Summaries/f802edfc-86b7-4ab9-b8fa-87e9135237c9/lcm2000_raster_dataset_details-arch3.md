# 25m raster

- Overview
  - Describes the 25m raster dataset created by converting land parcels (vector data) into a 25m grid.
  - Each 25m cell records the dominant land cover using LCM2000 Subclasses.
  - Provides metadata for Great Britain (GB) and Northern Ireland (NI), including grid dimensions, extents, coordinate systems, projections, and datum.
  - Includes note on pixel-centre calculation (add 12.5 m to lower-left corner values to obtain cell centre).

- 25m raster details (GB and NI)
  - GB metadata
    - Columns: 24,400; Rows: 48,400
    - Lower left easting: 50,000 m; Lower left northing: 10,000 m
    - Pixel size: 25 m
    - Coordinate system: British National Grid; Projection: Transverse Mercator
    - Spheroid: Airy; Datum: OSGB 1936
  - NI metadata
    - Columns: 7,600; Rows: 7,200
    - Lower left easting: 180,000 m; Lower left northing: 280,000 m
    - Pixel size: 25 m
    - Coordinate system: Irish National Grid; Projection: Transverse Mercator
    - Spheroid: Airy Modified 1849; Datum: Ireland 1965

- Data encoding and storage
  - LCM2000 Subclass codes (typically floating point with one decimal place) are stored as 8-bit unsigned integers by multiplying by 10 (e.g., Water (inland) Subclass 22.1 becomes 221).
  - This encoding supports efficient raster storage and retrieval.

- 1km raster: construction and metadata
  - Creation method
    - 1km raster is derived by summarising the 25m raster data within each 1km grid cell.
  - GB metadata
    - Columns: 700; Rows: 1,300
    - Pixel size: 1000 m
    - Coordinate system and projection: GB Irish National Grid? (for GB) — British National Grid; same as 25m for consistency
  - NI metadata
    - Columns: 500; Rows: 500
    - Pixel size: 1000 m
    - Coordinate system and projection: Irish National Grid
  - Note
    - The 1km raster uses the same coordinate systems, projections, and datums as the 25m raster.
    - Pixel-centre offset for 1km cells: add 500 m to the lower-left corner values.

- Table 3: correspondence between Subclasses and Aggregate/1km codes
  - Provides the crosswalk from 25m Subclass codes to 1km codes and to Aggregate class codes, enabling cross-scale interpretation.
  - Examples of mappings (selected):
    - Sea / Estuary (LCM2000 Subclass 25m code 221) → 1km code 1 → Aggregate class: Oceanic seas
    - Water (inland) (25m code 131) → 1km code 2 → Aggregate class: Standing open water
    - Littoral rock (25m code 201) → 1km code 3 → Aggregate class: Coastal
    - Bog (deep peat) (25m code 121) → 1km code 8 → Aggregate class: Mountain, heath, bog
    - Dense dwarf shrub heath (25m code 101) → 1km code 9 → Aggregate class: Mountain, heath, bog
    - Broad-leaved / mixed woodland (25m code 11) → 1km code 12 → Aggregate class: Broad-leaved / mixed woodland
    - Coniferous woodland (25m code 21) → 1km code 13 → Aggregate class: Coniferous woodland
    - Arable cereals (25m code 41) → 1km code 21 → Aggregate class: Arable and horticulture
  - Encoding note
    - The table encodes detailed relationships across the two spatial resolutions (25m and 1km) and the corresponding aggregate categories.

- Implications for monitoring frameworks
  - Cross-scale compatibility: Enables consistent interpretation of land-cover information at 25m and 1km scales for policy scrutiny and decision-making.
  - Data efficiency: 25m to 1km aggregation supports scalable reporting while preserving key land-cover classes.
  - Metadata and governance relevance: Clear metadata (grid dimensions, extents, coordinate systems, projections, datums, and encoding schemes) supports data quality, provenance, and openness requirements.
  - Classification alignment: TheSubclasses-to-aggregate mappings facilitate standardized reporting and comparability across datasets and monitoring outputs.

- Considerations for implementation and governance
  - Ensure metadata completeness, including explicit handling of pixel-centre offset and coordinate transformations between GB and NI grids.
  - Maintain documentation of the 8-bit encoding scheme and the rationale for multiplying Subclass codes by 10.
  - Facilitate data sharing and interoperability by using the provided crosswalk to interpret 25m and 1km classifications across scales.