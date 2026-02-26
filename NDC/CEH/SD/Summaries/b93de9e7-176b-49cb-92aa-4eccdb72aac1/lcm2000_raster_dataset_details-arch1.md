# 25m raster

- The raster 25m dataset was created by converting land parcels within a vector dataset into a 25m grid. Each grid cell records the dominant land cover at that location as an LCM2000 Subclass.

- Great Britain metadata
  - Columns: 24,400; Rows: 48,400
  - Lower left easting: 50,000 m; Lower left northing: 10,000 m
  - Pixel size: 25 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936

- Northern Ireland metadata
  - Columns: 7,600; Rows: 7,200
  - Lower left easting: 180,000 m; Lower left northing: 280,000 m
  - Pixel size: 25 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965

- Pixel centre note
  - For pixel centres, add 12.5 m to each lower-left corner value.

- 1km raster overview (summary of how it’s derived)
  - The LCM2000 raster 1km data is created by summarising the 25m raster within a 1km grid.

- Great Britain 1km raster metadata
  - Columns: 700; Rows: 1,300
  - Lower left easting/northing: 0
  - Pixel size: 1000 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936

- Northern Ireland 1km raster metadata
  - Columns: 500; Rows: 500
  - Lower left easting/northing: 0
  - Pixel size: 1000 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965

- Pixel centre note for 1km raster
  - For pixel centres, add 500 m to each lower-left corner value.

- Subclass and Aggregate class mapping (Table 3)
  - The 25m raster can be summarized by two schemes: by LCM2000 Subclass or by LCM2000 Aggregate class.
  - A crosswalk exists between 25m Subclass codes and 1km Subclass codes, and between Subclass codes and Aggregate class codes.
  - Encoding detail: Subclass codes are floating-point numbers with one decimal place and have been scaled by 10 to store as unsigned 8-bit bytes (0–255). Example: Water (inland) 25m Subclass code 131 becomes 1 km code 2; Sea / Estuary 25m Subclass code 221 becomes 1 km code 1; Oceanic seas (Aggregate class) 1 km code 10.
  - The table lists numerous land-cover categories (e.g., Sea/Estuary, Water inland, Littoral/Coastal types, Bog, various forest and woodland types, grasslands, arable and horticulture, semi-natural and built-up areas) with their corresponding 25m and 1km codes and Aggregate class codes.

- Practical implications for analysis
  - Provides two spatial resolutions (25m and 1km) for land-cover analysis in Great Britain and Northern Ireland.
  - Enables conversion between detailed 25m classifications and broader 1km classifications via the explicit crosswalk.
  - The 8-bit encoding and scaling by 10 facilitate storage efficiency while preserving the precision of subclass labels.