# 25m raster

- Overview
  - The 25m raster was created by converting land parcels within the vector dataset into a 25m grid, with each cell recording the dominant land cover as a LCM2000 Subclass.

- Dataset details
  - Great Britain (GB): 24,400 columns (width) × 48,400 rows (height)
  - Northern Ireland (NI): 7,600 columns × 7,200 rows
  - Lower-left coordinates (pixel corner): GB easting 50,000 m; GB northing 10,000 m; NI easting 180,000 m; NI northing 280,000 m
  - Pixel size: 25 m for both GB and NI
  - Coordinate systems and datums:
    - GB: British National Grid, Transverse Mercator, Airy spheroid, OSGB 1936
    - NI: Irish National Grid, Transverse Mercator, Airy Modified 1849
  - Pixel center adjustment: add 12.5 m to corner coordinates to get pixel centers

- 1km raster
  - Summary of the 25m data within 1km grid
  - GB: 700 columns × 1,300 rows
  - NI: 500 columns × 500 rows
  - Pixel size: 1,000 m
  - Coordinate systems and datums mirror the 25m raster (GB: OSGB 1936; NI: Ireland 1965)

- Encoding and storage
  - LCM2000 Subclass codes (floating point with one decimal) are stored as unsigned 8-bit bytes by multiplying by 10 (e.g., Water (inland) 22.1 → 221)

- Class mappings (Table 3)
  - The document provides a correspondence between:
    - LCM2000 Subclass codes (25m) and LCM2000 Aggregate class codes (1km)
    - Subclass/1km codes and Aggregate class 1km codes
  - Examples include:
    - Sea/Estuary (25m code 221) → 1km code 1 → Aggregate: Oceanic seas
    - Water (inland) (25m code 131) → 1km code 2 → Aggregate: Standing open water
    - Littoral rock (25m code 201) → 1km code 3 → Aggregate: Coastal
    - Arable cereals (25m code 41) → 1km code 21 → Aggregate: Arable and horticulture
    - Continuous urban (25m code 172) → 1km code 25 → Aggregate: Built up areas and gardens
  - The table covers many land-cover classes, including woodland types, grasslands, peatlands, arable lands, urban areas, and bare ground
  - Purpose: to support efficient storage and cross-scale interpretation of land-cover information

- Practical considerations for Data Stewards
  - Cross-border data integration requires careful handling of two coordinate systems (GB: OSGB 1936; NI: Ireland 1965) and their respective grids
  - Understanding the 25m-to-1km aggregation and the corresponding codes is essential for interoperability, querying, and metadata consistency
  - Data workflows should document the encoding scheme (8-bit byte with values derived from 10×Subclass codes) and the pixel-centre adjustments
  - Maintain and provide access to the mapping table (Table 3) to support accurate interpretation and re-use across systems

- Notes
  - The lower-left corner notes indicate how to compute pixel-centre coordinates (add 12.5 m for 25m cells; add 500 m for 1km cells)