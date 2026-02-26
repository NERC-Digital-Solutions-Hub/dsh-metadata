# 25m raster

## Overview
- The 25m raster dataset was created by converting land parcels from a vector dataset into a 25m grid.
- Each grid cell records the dominant land cover as an LCM2000 Subclass.
- The dataset includes Great Britain and Northern Ireland extents, and a separate 1km raster derived by summarising the 25m data.
- Two representations exist for storage efficiency: 25m by Subclass and 25m by Aggregate class, with a comprehensive mapping to 1km codes.

## Dataset structure and coverage
- 25m raster (Great Britain)
  - Columns: 24,400; Rows: 48,400
  - Lower left: easting 50,000 m; northing 10,000 m
  - Pixel size: 25 m
  - Coordinate system / Projection / Datum: British National Grid, Transverse Mercator, OSGB 1936
  - Spheroid: Airy
- 25m raster (Northern Ireland)
  - Columns: 7,600; Rows: 7,200
  - Lower left: easting 180,000 m; northing 280,000 m
  - Pixel size: 25 m
  - Coordinate system / Projection / Datum: Irish National Grid, Transverse Mercator, Ireland 1965
  - Spheroid: Airy Modified 1849
- 1km raster (Great Britain)
  - Columns: 700; Rows: 1,300
  - Lower left: easting 0 m; northing 0 m
  - Pixel size: 1000 m
  - Coordinate system / Projection / Datum: British National Grid, Transverse Mercator, OSGB 1936
- 1km raster (Northern Ireland)
  - Columns: 500; Rows: 500
  - Lower left: easting 0 m; northing 0 m
  - Pixel size: 1000 m
  - Coordinate system / Projection / Datum: Irish National Grid, Transverse Mercator, Ireland 1965

## Data encoding and coding
- 25m Subclass codes are floating point with one decimal; to store efficiently as raster, codes are multiplied by 10 and stored as unsigned 8-bit values (0–255).
- Example: LCM2000 Subclass code 22.1 (Water inland) becomes 221 in the 25m raster.
- 1km codes are the aggregated class equivalents for the corresponding 25m data.

## Mapping and metadata
- A correspondence table (Table 3) provides:
  - Mapping between LCM2000 Subclasses (25m) and Aggregate classes (1km)
  - Attribute codes for both 25m and 1km representations
- Examples of mappings (illustrative, not exhaustive):
  - Sea/Estuary: 25m code 221 → 1km code 10 (Aggregate: Oceanic seas)
  - Water (inland): 25m code 131 → 1km code 8 (Aggregate: Standing open water)
  - Littoral rock: 25m code 201 → 1km code 9 (Aggregate: Coastal)
  - Arable cereals: 25m code 41 → 1km code 21 (Aggregate: Arable and horticulture)
- The tables enable cross-resolution interoperability between the 25m Subclass, 25m by Aggregate, and 1km codes.

## Data lineage and derivation
- 25m raster derived by converting land parcels from the vector dataset to a 25m grid and assigning the dominant LCM2000 Subclass per cell.
- 1km raster derived by summarising the 25m raster data within 1km grid cells (aggregation of the 25m data).

## Practical considerations for Data Stewards
- Metadata accuracy:
  - Ensure recording of extent, grid resolution (25 m and 1 km), coordinate systems, projections, datums, and pixel-centre calculation notes.
  - Document the note about pixel centre: for 25m, add 12.5 m to lower-left corner values to obtain the pixel centre; for 1km, add 500 m.
- Data interoperability:
  - The 8-bit encoding (0–255) requires careful handling when exchanging data with systems expecting broader value ranges.
  - Maintain the explicit mapping between Subclass, Aggregate class, and 1km codes to prevent misinterpretation across tools.
- Data quality and update:
  - Consider the completeness and timeliness of the underlying vector parcels used for the 25m conversion.
  - Track any changes in LCM2000 classifications or re-derivations that would affect the 25m and 1km representations.
- System and format considerations:
  - Be aware of potential format limitations when storing or transferring large 25m rasters, especially given regional extents (GB vs NI) and dual-resolution outputs.
  - Maintain separation of formats for 25m Subclass vs 25m Aggregate vs 1km to avoid confusion.
- Governance posture:
  - Capture provenance, processing steps, and any assumptions used during conversion and aggregation.
  - Ensure updates to mappings (Table 3) and unit conventions are version-controlled.

## Potential challenges for Data Stewards
- Ensuring a complete picture of user needs and alignment with diverse downstream applications across GB and NI.
- Obtaining timely input from data creators to maintain standardization of metadata and classification schemes.
- Managing multiple systems and formats (25m Subclass, 25m Aggregate, 1km) and maintaining consistent cross-resolution mappings.
- Handling large datasets and potential format interoperability issues when transferring between platforms.
- Keeping legacy or outdated databases aligned with the current encoding and classification schemes.