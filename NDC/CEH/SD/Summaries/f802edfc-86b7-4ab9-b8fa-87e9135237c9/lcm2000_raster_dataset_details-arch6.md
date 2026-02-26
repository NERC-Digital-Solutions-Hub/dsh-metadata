# 25m raster

## Overview
- The raster 25m dataset is created by converting land parcels within the vector data set into a 25m grid, recording the dominant land cover as LCM2000 Subclasses.
- Separate Great Britain (GB) and Northern Ireland (NI) datasets; details summarized across Tables 1–3.

## 25m raster metadata (Table 1)
- Columns / Width (pixels): GB 24,400; NI 7,600
- Rows / Height (pixels): GB 48,400; NI 7,200
- Lower left easting (m): GB 50,000; NI 180,000
- Lower left northing (m): GB 10,000; NI 280,000
- Pixel size (m): GB 25; NI 25
- Coordinate system: GB = British National Grid; NI = Irish National Grid
- Projection: GB = Transverse Mercator; NI = Transverse Mercator
- Spheroid: GB = Airy; NI = Airy Modified 1849
- Datum: GB = OSGB 1936; NI = Ireland 1965
- Note: To obtain the pixel centre, add 12.5 m to each lower-left value.

## 1km raster (Table 2)
- The LCM2000 raster 1km data are produced by summarising the 25m raster within a 1km grid.
- Columns / Width (GB): 700; (NI): 500
- Rows / Height (GB): 1,300; (NI): 500
- Lower left easting (m): GB = 0; NI = 0
- Lower left northing (m): GB = 0; NI = 0
- Pixel size (m): GB = 1000; NI = 1000
- Coordinate system: GB = British National Grid; NI = Irish National Grid
- Projection: Transverse Mercator for both
- Spheroid: GB = Airy; NI = Airy Modified 1849
- Datum: GB = OSGB 1936; NI = Ireland 1965
- Note: To obtain the pixel centre, add 500 m to each value.

## Subclass to Aggregate mapping (Table 3)
- The 25m LCM2000 Subclass codes (typically floating with one decimal) are stored as unsigned 8-bit bytes by multiplying by 10 (0–255).
- Example: Water (inland) subclass 22.1 becomes 221 in the raster.
- The table provides a crosswalk from 25m Subclass codes to:
  - 1km Subclass codes
  - 1km Aggregate class
  - Aggregate class code (1km)
- Examples:
  - Sea / Estuary: 25m code 221 -> 1km code 1 -> Oceanic seas
  - Water (inland): 25m code 131 -> 1km code 2 -> Standing open water
  - Littoral rock: 25m code 201 -> 1km code 3 -> Coastal
  - Saltmarsh: 25m code 212 -> 1km code 5 -> Coastal
  - Supra-littoral rock: 25m code 181 -> 1km code 6 -> Coastal
  - Various other classes include bog, heath, woodland, grassland, arable, urban, bare ground, etc.
- The mapping enables consistent interpretation across the 25m and 1km representations.

## Encoding rationale
- Subclass codes (with decimal) are scaled by 10 to fit into an unsigned 8-bit raster (0–255) for efficient storage.
- Example transformation demonstrates compact storage and cross-scale interpretation.

## Practical implications for data use and data support
- The 1km raster is a coarser summary of the 25m data, facilitating broader analyses while retaining class semantics through the crosswalk.
- Table 3 enables translating detailed 25m subclasses to coarser 1km subclasses and aggregate classes, supporting multi-scale analysis and dashboard design.
- Users must be mindful of coordinate reference systems, projections, and pixel-centre offsets when aligning datasets or performing spatial joins.
- The datasets are applicable to GB and NI contexts, supporting data products, reporting, and planning that rely on land-cover classifications.