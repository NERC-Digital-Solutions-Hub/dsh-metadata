# 25m raster

- Overview
  - Two raster datasets derived from land cover data: a 25m raster recording the dominant LCM2000 Subclass per 25m cell, and a 1km raster summarised from the 25m data.
  - Coverage includes Great Britain and Northern Ireland; designed to convert vector land parcels into a grid for analysis and storage efficiency.

- How the datasets were created
  - 25m raster: created by converting land parcels from the vector dataset into a 25m grid; each cell stores the dominant LCM2000 Subclass.
  - 1km raster: created by summarising the 25m raster within 1km grid cells.

- Metadata and technical details
  - 25m raster
    - Great Britain: 24,400 columns × 48,400 rows; Northern Ireland: 7,600 × 7,200.
    - Lower-left coordinates (easting/northing) and pixel size: 25 m.
    - Coordinate systems: Great Britain — British National Grid; Northern Ireland — Irish National Grid.
    - Projections: Transverse Mercator for both GB and NI.
    - Datums/Spheroids: GB — OSGB 1936 / Airy; NI — Ireland 1965 / Airy Modified 1849.
    - Note: Pixel centre is offset by 12.5 m from the listed lower-left corner.
  - 1km raster
    - Great Britain: 700 × 1,300; Northern Ireland: 500 × 500.
    - Pixel size: 1000 m.
    - Same coordinate systems, projections, and datums as the 25m raster.
    - Note: Pixel centre is offset by 500 m from the listed lower-left corner.

- Data encoding and storage efficiency
  - LCM2000 Subclass codes (floating with one decimal) are multiplied by 10 and stored as unsigned 8-bit bytes (0–255).
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster.

- Subclass to 1km and Aggregate class mapping (Table 3)
  - The document provides a crosswalk linking:
    - 25m Subclass codes
    - 1km codes
    - Aggregate class codes
  - Examples of mappings:
    - Sea / Estuary: 25m code 221 → 1km code 10 → Aggregate class Oceanic seas
    - Water (inland): 25m code 131 → 1km code 2 → Aggregate class Standing open water
    - Littoral rock: 25m code 201 → 1km code 3 → Aggregate class Coastal
    - Saltmarsh: 25m code 212 → 1km code 5 → Aggregate class Coastal
    - Supra-littoral rock: 25m code 181 → 1km code 6 → Aggregate class Coastal
    - Supra-littoral sediment: 25m code 191 → 1km code 7 → Aggregate class Coastal
    - Bog (deep peat): 25m code 121 → 1km code 8 → Aggregate class Mountain, heath, bog
    - Dense/Open dwarf shrub heath, Montane habitats, Woodland types, Grasslands, Arable, Urban, and Bare ground categories are similarly mapped across 25m, 1km, and Aggregate classes.
  - Purpose: enables efficient storage and consistent interpretation across scales, while preserving a detailed subclass taxonomy.

- Practical implications for data governance and use
  - Clear documentation needed for:
    - Coding scheme (how Subclass -> 1km -> Aggregate codes are derived)
    - Coordinate systems, extents, and pixel alignment to support integration with other datasets
    - Pixel center deltas for precise geolocation
  - Data quality and consistency considerations:
    - Cross-border alignment (GB vs NI) due to different datums and grids
    - Consistency of subclass definitions and their cross-walk to aggregated classes
  - Usage considerations:
    - Choose 25m detail for fine-grained analysis; use 1km rasters for broader regional assessments or storage efficiency
    - Ensure user needs are captured and feedback loops established to validate data products (as per the Data Leaders mindset of co-ownership and iterative product development)

- Summary points for Data Leaders
  - The document outlines two linked raster datasets (25m and 1km) with detailed metadata and a comprehensive crosswalk between subclass codes, 1km codes, and aggregate classes.
  - It emphasizes data encoding efficiency (8-bit storage) and the need for thorough metadata to support discoverability, interoperability, and cross-border integration.
  - The materials enable scalable analysis across GB and NI while preserving detailed land-cover taxonomy through a well-documented code mapping.