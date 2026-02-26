# 25m raster

## Overview
- The 25m raster dataset is created by converting the land parcels from a vector dataset into a 25-meter grid, recording the dominant land cover at each cell using LCM2000 Subclasses.
- A companion 1km raster is derived by summarising the 25m data within 1km grid cells.

## Dataset details: Great Britain and Northern Ireland
- 25m raster specifications
  - Great Britain: 24,400 columns x 48,400 rows
  - Northern Ireland: 7,600 columns x 7,200 rows
  - Lower left easting/northing: GB 50,000; NI 180,000 (easting); GB 10,000; NI 280,000 (northing)
  - Pixel size: 25 m (GB and NI)
  - Coordinate systems: GB = British National Grid; NI = Irish National Grid
  - Projection: Transverse Mercator for both GB and NI
  - Spheroid: GB = Airy; NI = Airy Modified 1849
  - Datum: GB = OSGB 1936; NI = Ireland 1965
  - Note: Values shown refer to the lower-left corner of the lower-left pixel; add 12.5 m to reach pixel centre
- 1km raster specifications
  - Great Britain: 700 columns x 1,300 rows
  - Northern Ireland: 500 columns x 500 rows
  - Lower left easting/northing: GB = 0; NI = 0
  - Pixel size: 1000 m
  - Coordinate systems, projections, spheroids, and datums as above
  - Note: Values shown refer to the lower-left corner of the lower-left pixel; add 500 m to reach pixel centre

## Subclass vs Aggregate classification
- The 25m data are summarised in two ways: by LCM2000 Subclass codes and by LCM2000 Aggregate class codes.
- Table 3 (mapping) provides the correspondence between Subclasses and Aggregate classes and shows the attribute codes for each land cover (examples below).
- Encoding approach for storage
  - LCM2000 Subclass codes are floating point numbers with one decimal place
  - To store efficiently in raster format, codes are multiplied by 10 and stored as unsigned 8-bit bytes (0–255)
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster dataset

## Examples of mappings (Sample)
- Sea / Estuary
  - 25m code: 221
  - 1km code: 10
  - Aggregate class: Oceanic seas
- Water (inland)
  - 25m code: 131
  - 1km code: 2
  - Aggregate class: Standing open water
- Littoral rock / Littoral sediment / Saltmarsh / Supra-littoral rock / Supra-littoral sediment
  - Various 25m codes (e.g., 201, 211, 212, 181, 191)
  - Corresponding 1km codes (e.g., 3, 4, 5, 6, 7)
  - Aggregate class: Coastal
- Habitat and land cover categories (examples)
  - Montane habitats, various woodlands (Broad-leaved/mixed, Coniferous), grasslands (Improved, Neutral, Calcareous, Acid), arable and horticulture, urban/suburban developed
  - Each category has a 25m code, a 1km code, and an Aggregate class

## Practical notes
- The 25m to 1km raster derivation supports multi-resolution analysis and efficient storage while preserving classification details through the Subclass and Aggregate mappings.
- The full mapping table provides comprehensive coverage of land cover types and their codes across both resolutions.

## Relevance for data strategy (Data Leaders)
- Demonstrates end-to-end data lineage: from vector land parcels to a 25m raster, with a 1km aggregated raster for broader analyses.
- Highlights metadata completeness: grid dimensions, extents, coordinate systems, projections, datums, and pixel centroid adjustments, essential for data discoverability and reuse.
- Shows encoding decisions to balance storage efficiency and class detail (8-bit encoding of scaled Subclass codes).
- Illustrates the need for clear, consistent mappings between fine-grained subclasses and higher-level aggregate classes to support interoperability across systems and user needs.
- Emphasises governance considerations: handling multiple coordinate systems, ensuring metadata clarity, and documenting coding schemes to reduce ambiguity and duplication of effort.