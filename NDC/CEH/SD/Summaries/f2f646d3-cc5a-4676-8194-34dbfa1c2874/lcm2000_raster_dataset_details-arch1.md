# 25m raster

- The 25m raster is created by converting land parcels from the vector dataset into a 25m grid. Each grid cell records the dominant land cover at that location using LCM2000 Subclasses.
- Great Britain and Northern Ireland have separate metadata and grids with their own dimensions and coordinate systems.

## Dataset details

- Great Britain (GB)
  - Dimensions: 24,400 columns (width) × 48,400 rows (height)
  - Pixel size: 25 m
  - Lower left easting/northing: 50,000 m / 10,000 m
  - Coordinate system / projection: British National Grid / Transverse Mercator
  - Spheroid / Datum: Airy / OSGB 1936
- Northern Ireland (NI)
  - Dimensions: 7,600 columns × 7,200 rows
  - Pixel size: 25 m
  - Lower left easting/northing: 180,000 m / 280,000 m
  - Coordinate system / projection: Irish National Grid / Transverse Mercator
  - Spheroid / Datum: Airy Modified 1849 / Ireland 1965
- Pixel-centre note: add 12.5 m to corner values to obtain the pixel centre.

## 1km raster

- The 1km raster is derived by summarising the 25m raster within 1km grid cells.
- GB: 700 columns × 1,300 rows; NI: 500 × 500
- Pixel size: 1,000 m
- Same coordinate systems, projections, and datums as the 25m data.
- Pixel-centre note: add 500 m to corner values to obtain the pixel centre.

## Coding and classification

- To store the 25m Subclass codes efficiently, Subclass codes (normally floating with one decimal) are multiplied by 10 and stored as unsigned 8-bit bytes (0–255).
  - Example: Water (inland) Subclass 22.1 becomes 221 in the 25m raster.
- The 1km raster uses Aggregate class codes, with mappings provided in the correspondence table.

## Subclass to Aggregate class mapping (Table 3)

- The document provides a correspondence between LCM2000 Subclasses (25m and 1km) and LCM2000 Aggregate classes for both scales.
- Examples (1km codes):
  - Sea / Estuary → Oceanic seas (code 10)
  - Water (inland) → Standing open water (code 8)
  - Littoral rock / Littoral sediment / Saltmarsh / Supra-littoral rock / Sediment → Coastal (codes 3–9)
  - Arable cereals / Arable horticulture / Arable non-rotational → Arable and horticulture (code 3)
  - Suburban/rural developed / Continuous urban → Built up areas and gardens (codes 7–7)
  - Woodland (broad-leaved/mixed, coniferous) → Woodlands (codes 1–2)
  - Various grasslands, bogs, heaths, and other natural habitats mapped to Semi-natural grassland or Mountain, heath, bog (codes 5, 6)

## Metadata and coordinates

- The tables (Table 1 for 25m, Table 2 for 1km) provide full metadata details, including grid size, extents, coordinate systems, projections, datums, and pixel-centre offsets.
- The 25m and 1km datasets are designed to support cross-scale analysis by providing a consistent aggregation framework via the Subclass–Aggregate mappings.

## Practical notes for analysts

- Use the 25m data for fine-scale land cover where local detail is important; use the 1km data for coarser, aggregated analyses.
- When combining with other datasets, ensure consistent scale and the correct mapping between Subclass and Aggregate classes.
- Be mindful of data origin and metadata (coordinate systems, datums, and pixel-centre offsets) to maintain spatial accuracy and reproducibility.
- The Subclass-to-Aggregate mappings enable cross-scale comparisons and trend analyses, but require careful interpretation of the 1km codes versus the 25m Subclass codes.