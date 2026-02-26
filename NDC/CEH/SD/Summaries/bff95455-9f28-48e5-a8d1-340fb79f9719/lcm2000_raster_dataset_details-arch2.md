# 25m raster

- The document describes the creation of a 25m raster dataset by converting land parcels (vector data) into a 25m grid, recording the dominant land cover as LCM2000 Subclasses.
- A 1km raster dataset is also produced by summarising the 25m data within 1km grid cells.

## 25m raster dataset (GB and NI)

- Grid and extent
  - Great Britain: 24,400 columns x 48,400 rows
  - Northern Ireland: 7,600 columns x 7,200 rows
  - Pixel size: 25 m
  - Lower left corner coordinates (easting/northing) provided for both GB and NI
  - Pixel centre offset: add 12.5 m to each lower-left coordinate to obtain the pixel centre

- Coordinate systems and projections
  - Great Britain: British National Grid, Transverse Mercator, Spheroid Airy, OSGB 1936
  - Northern Ireland: Irish National Grid, Transverse Mercator, Spheroid Airy Modified 1849, Ireland 1965

- Content and coding
  - Each 25m cell records the dominant land cover using LCM2000 Subclasses
  - Subclass codes are stored as unsigned 8-bit bytes by multiplying the original value by 10 (one decimal place)
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster

## 1km raster dataset (GB and NI)

- Derivation and grid
  - The 1km raster is created by summarising the 25m raster data within 1km grid cells
  - Great Britain: 700 columns x 1,300 rows
  - Northern Ireland: 500 columns x 500 rows
  - Pixel size: 1000 m
  - Pixel centre offset: add 500 m to lower-left coordinates

- Content and coding
  - Uses LCM2000 data aggregated to 1km classes
  - Correspondence between 25m Subclasses and 1km Subclass/Aggregate classes is defined in Table 3

## Table 3: Subclass to Aggregate class correspondence

- Purpose
  - Provides the mapping between LCM2000 Subclass codes (25m) and their 1km Subclass codes and Aggregate class codes/descriptions
- Examples of the categorisation
  - Sea / Estuary and related coastal/estuary categories
  - Water (inland) and Standing open water
  - Littoral rock and Littoral sediment (coastal)
  - Saltmarsh and Supra-littoral habitats
  - Bog, Montane habitats, various woodlands (Broad-leaved, Coniferous), and grassland types
  - Arable and horticulture (subtypes)
  - Urban/built-up and suburban/rural developed, including Continuous urban
  - Inland bare ground
- Significance
  - Enables consistent translation from detailed 25m Subclasses to higher-level 1km classes for analysis and reporting

## Practical considerations for analysts monitoring the environment

- Standardised datasets
  - 25m and 1km rasters provide a consistent format for monitoring environmental health and policy performance over time
- Data quality and provenance
  - Data derive from established land cover classifications (LCM2000) and are accompanied by explicit metadata (grid dimensions, coordinate systems, projections, and datums)
- Data handling and storage
  - Subclass values are stored as compact 8-bit integers (via scaling), facilitating efficient storage and retrieval
  - The datasets are designed for storage and upload to data portals
- Spatial alignment and integration
  - Be mindful of the different coordinate systems and the pixel-centre offsets when aligning with other layers
  - The 1km raster serves as a summary product suitable for broad-scale analyses and time-series comparisons
- Value addition and data sharing
  - The standardised, dual-resolution rasters enable combining with other data sources and sharing underlying data to support broader analytical use and re-use

## End-to-end relevance to monitoring aims

- The 25m raster provides a detailed, standardized representation of land cover across GB and NI
- The 1km raster offers a higher-level, comparable product for trend analysis and policy evaluation
- Clear mapping between Subclasses and Aggregate classes, with explicit encoding, supports transparent, reproducible analyses and easier data integration across datasets and time periods