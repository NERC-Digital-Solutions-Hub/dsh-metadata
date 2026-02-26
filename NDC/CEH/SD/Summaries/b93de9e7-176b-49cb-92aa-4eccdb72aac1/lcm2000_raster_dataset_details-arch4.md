# 25m raster

- The 25m raster dataset records the dominant land cover at each 25m grid cell, derived by converting land parcels from a vector dataset into a 25m grid using LCM2000 Subclasses.
- Coverage: Great Britain and Northern Ireland, with detailed metadata provided in the source tables.

- 25m raster details
  - Grid size: Great Britain 24,400 columns × 48,400 rows; Northern Ireland 7,600 columns × 7,200 rows.
  - Lower left origin: Great Britain easting 50,000 m, northing 10,000 m; Northern Ireland easting 180,000 m, northing 280,000 m.
  - Pixel size: 25 m.
  - Coordinate systems and datums: Great Britain uses British National Grid (OSGB 1936), Transverse Mercator, Airy; Northern Ireland uses Irish National Grid (Ireland 1965), Transverse Mercator, Airy Modified 1849.
  - Pixel center alignment note: add 12.5 m to lower-left corner coordinates to obtain the pixel center coordinates.

- 1km raster (summary of 25m data)
  - Created by summarising the 25m raster within a 1km grid.
  - Grid size: Great Britain 700 columns × 1,300 rows; Northern Ireland 500 columns × 500 rows.
  - Lower left origin: 0 m for both GB and NI.
  - Pixel size: 1,000 m.
  - Coordinate systems and datums: same as the 25m raster (GB and NI variants).
  - Pixel center alignment note: add 500 m to lower-left corner coordinates to obtain the pixel center coordinates.
  
- Data encoding and storage
  - Subclass codes (typically floating with one decimal) are stored as unsigned 8-bit bytes by multiplying by 10 (range 0–255).
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster.

- Subclass to aggregate-class mapping (Table 3)
  - The 25m Subclasses are mapped to 1km Aggregate classes, with corresponding 1km codes.
  - The mapping enables cross-scale analyses (25m to 1km) and supports consistent categorisation across GB and NI.
  - The table covers a comprehensive set of land cover types (e.g., Sea/Estuary, Water inland, Littoral/Saline categories, various vegetation, arable, urban, peat/bog, etc.), with explicit numerical codes for both 25m and 1km representations.

- Governance and practical considerations for data leaders
  - Clear, cross-scale metadata (grid geometry, coordinate reference systems, datums, pixel size) supports discoverability and interoperability.
  - Cross-scale consistency is achieved through the explicit 25m-to-1km aggregation mapping.
  - Storage efficiency is enhanced by encoding land cover classes as 8-bit integers after scaling.
  - Documentation of edge-cases and centre-pixel offsets (12.5 m and 500 m adjustments) is essential for accurate spatial alignment in analyses.
  - Useful for planning, policy analysis, and cross-sector collaboration that require harmonised land cover information across the UK.