# 25m raster

- Overview
  - Describes two raster products derived from land-cover data: a 25m raster created by converting land parcels within a vector dataset into a 25m grid, recording dominant land cover by LCM2000 Subclasses; and a 1km raster summarising the 25m data within 1km grid.
  - Datasets cover Great Britain (GB) and Northern Ireland (NI) with metadata and code mappings to support interoperability.

- Dataset specifications
  - 25m raster
    - GB: 24,400 columns × 48,400 rows
    - NI: 7,600 columns × 7,200 rows
    - Lower left corner: GB easting 50,000 m; NI easting 180,000 m; GB northing 10,000 m; NI northing 280,000 m
    - Pixel size: 25 m
    - Coordinate system / projection: GB – British National Grid / Transverse Mercator; NI – Irish National Grid / Transverse Mercator
    - Datums / spheroids: GB – OSGB 1936 / Airy; NI – Ireland 1965 / Airy Modified 1849
    - Pixel centre reference: add 12.5 m to lower-left values for pixel centre
  - 1km raster
    - GB: 700 columns × 1,300 rows
    - NI: 500 columns × 500 rows
    - Lower left corner: GB easting 0 m; NI easting 0 m; GB northing 0 m; NI northing 0 m
    - Pixel size: 1000 m
    - Coordinate system / projection: GB – British National Grid / Transverse Mercator; NI – Irish National Grid / Transverse Mercator
    - Datums / spheroids: GB – OSGB 1936 / Airy; NI – Ireland 1965 / Airy Modified 1849
    - Pixel centre reference: add 500 m to lower-left values for pixel centre
- Data encoding and class mapping
  - Subclass codes (25m) are stored as scaled integers by multiplying by 10 to fit unsigned 8-bit (0–255). Example: Water (inland) Subclass 22.1 becomes 221.
  - 1km raster has corresponding codes for 1km aggregation.
  - Table 3 provides the crosswalk between LCM2000 Subclasses (25m codes) and Aggregates (1km codes) along with the aggregate class names (e.g., Sea/Estuary, Water/inland, Littoral rock, etc.).
  - This enables both per-subclass analysis and higher-level aggregate analyses.

- Processing and data lineage
  - The 25m raster is generated from the LCM2000 Subclasses; the 1km raster is produced by summarising the 25m raster within 1km grids.
  - There are two summarisation approaches: by LCM2000 Subclass and by LCM2000 Aggregate class, with respective codes.
  - The dataset provides explicit code mappings to support decoding and integration into other systems and analyses.

- Governance, quality, and interoperability considerations for Data Stewards
  - Metadata needs: verify and maintain detailed metadata (extents, pixel sizes, coordinate systems, datums, projections, note on pixel-centre offsets, and the Subclass-to-Aggregate mapping table).
  - Data standards: ensure consistent use of LCM2000 taxonomy, proper scaling of subclass codes to 8-bit storage, and clear documentation of the 25m vs 1km products.
  - Data availability and updates: document provenance (vector-to-raster conversion, summarisation process), track any updates to base land-cover information, and manage updates in both 25m and 1km products.
  - Data sharing and discovery: index both rasters in relevant portals, exposing both the 25m and 1km products and providing the table-based crosswalk for users needing translations between codes and classes.
  - Interoperability challenges: manage differences between GB and NI grids (coordinate systems, datums, projections) and handle large dataset sizes, as well as potential need for bespoke solutions for some workflows.
  - Data quality considerations: ensure quality assurance during conversion (vector-to-raster) and during aggregation, and keep track of the limitations and uncertainty inherent in the aggregation process.

- Practical usage notes
  - The pixel-centre offsets (12.5 m for 25m and 500 m for 1km) are important for precise alignment and spatial analyses.
  - The 25m codes are designed to fit into 0–255 as unsigned bytes, which is important for storage formats and interoperability in raster datasets.
  - The two-resolution setup (25m and 1km) supports both detailed analyses and scalable, aggregated insights, with explicit mappings to facilitate cross-resolution analyses.

- Quick reference points
  - Two products: 25m raster (high-resolution, Subclass level) and 1km raster (coarser, Aggregate level).
  - Two geographic contexts: Great Britain and Northern Ireland, with distinct coordinate systems and datums.
  - Coding scheme: 25m Subclass codes scaled by 10 for 8-bit storage; crosswalk table links Subclasses to 1km Aggregates and codes.