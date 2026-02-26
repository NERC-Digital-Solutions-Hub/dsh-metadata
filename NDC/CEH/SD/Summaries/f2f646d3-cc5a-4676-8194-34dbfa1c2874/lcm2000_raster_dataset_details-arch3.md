# 25m raster

## Overview
- The 25m raster converts land parcels within the vector dataset into a 25-metre grid, recording the dominant land cover per cell according to LCM2000 Subclasses.
- Separate metadata provided for Great Britain and Northern Ireland datasets.
- A 1km raster product is derived by summarising the 25m data within 1km grid cells.

## Dataset details
- 25m raster metadata (Great Britain):
  - Columns: 24,400; Rows: 48,400; lower left easting: 50,000 m; lower left northing: 10,000 m.
  - Pixel size: 25 m.
  - Coordinate system: British National Grid (OSGB 1936); Projection: Transverse Mercator; Spheroid: Airy; Datum: OSGB 1936.
- 25m raster metadata (Northern Ireland):
  - Columns: 7,600; Rows: 7,200; lower left easting: 180,000 m; lower left northing: 280,000 m.
  - Pixel size: 25 m.
  - Coordinate system: Irish National Grid; Projection: Transverse Mercator; Spheroid: Airy Modified 1849; Datum: Ireland 1965.
- 1km raster metadata (Great Britain):
  - Columns: 700; Rows: 1,300; lower left easting: 0 m; lower left northing: 0 m.
  - Pixel size: 1,000 m.
  - Coordinate system and projection same as 25m GB (OSGB 1936, Transverse Mercator).
- 1km raster metadata (Northern Ireland):
  - Columns: 500; Rows: 500; lower left easting: 0 m; lower left northing: 0 m.
  - Pixel size: 1,000 m.
  - Coordinate system and projection same as 25m NI (Ireland 1965, Transverse Mercator).
- Pixel center reference: for 25m, add 12.5 m to lower-left values to obtain the pixel centre; for 1km, add 500 m.

## Data encoding and storage
- 25m Subclass codes are typically floating point with one decimal place but stored as unsigned 8-bit bytes by multiplying by 10 (0-255). Example: Water (inland) Subclass 22.1 becomes 221 in the raster dataset.

## Subclass to Aggregate and 1km coding (Table 3)
- The 25m raster provides a correspondence between LCM2000 Subclasses and LCM2000 Aggregate classes, plus their 1km codes.
- The 1km codes enable efficient storage of the 1km raster.
- Land-cover categories include Sea/Estuary, Water (inland), Littoral rock/sediment, Saltmarsh, Supra-littoral rock/sediment, various vegetation types (bog, heath, woodland, grassland), arable and horticulture classes, urban and built-up areas, and bare ground, among others.
- Example relationships:
  - Sea/Estuary (25m Subclass code 221) maps to Oceanic seas (1km code 10) and Sea/Estuary aggregate class (1km code 9 for coastal categories).
  - Water (inland) (25m 131) maps to Standing open water (1km code 8) and corresponding Aggregate class codes.
  - Land-cover subclasses such as broad-leaved/mixed woodland, coniferous woodland, various grasslands, arable types, and urban areas have defined 1km codes and aggregate-class mappings.
- This table provides the full detailed mapping for both the 25m subclass codes and their 1km equivalents, enabling cross-resolution analyses.

## Data products and usage for monitoring
- Two primary raster products:
  - 25m raster by LCM2000 Subclass (and by LCM2000 Aggregate class).
  - 1km raster summarised from the 25m data, using the provided Subclass-to-Aggregate-to-1km mappings.
- The mappings support consistent reporting and dashboards across Great Britain and Northern Ireland, enabling policy scrutiny and decision-making processes in environmental monitoring.

## Implications for monitoring and governance (practical considerations)
- Data granularity: 25m resolution provides detailed land-cover information; 1km raster offers a coarser, summary view suitable for broader policy assessment.
- Encoding efficiency: 25m codes stored as 8-bit bytes (0-255) via multiplication by 10; decode step needed for interpretation.
- Metadata accessibility: detailed metadata is provided for both GB and NI datasets, including grid dimensions, extents, coordinates, and projection details, which is essential for data governance and reproducibility.
- Cross-resolution consistency: Table 3 enables reliable translation between subclass codes, aggregate classes, and 1km codes, facilitating integration with other datasets and monitoring frameworks.
- Data integration considerations: users should account for coordinate system differences (GB versus NI grids) and the pixel-centre offset when overlaying with other spatial layers.