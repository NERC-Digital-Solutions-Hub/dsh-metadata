# 25m raster

- What it is: A raster dataset created by converting land parcels in the vector dataset into a 25m grid; each 25m cell records the dominant land cover using LCM2000 Subclasses.

- Spatial coverage and grid details:
  - Great Britain: 24,400 columns x 48,400 rows; lower left easting 50,000 m, lower left northing 10,000 m; pixel size 25 m; coordinate system: British National Grid; projection: Transverse Mercator; datum: OSGB 1936; spheroid: Airy.
  - Northern Ireland: 7,600 columns x 7,200 rows; lower left easting 180,000 m, lower left northing 280,000 m; pixel size 25 m; coordinate system: Irish National Grid; projection: Transverse Mercator; datum: Ireland 1965; spheroid: Airy Modified 1849.
  - Note: values refer to the lower left corner of the lower left pixel; to obtain the pixel centre, add 12.5 m to each coordinate.

- 1km raster (summary of the 25m data):
  - Great Britain: 700 columns x 1,300 rows; lower left easting 0 m, lower left northing 0 m; pixel size 1000 m; same coordinate systems and projections as above.
  - Northern Ireland: 500 columns x 500 rows; lower left origin 0 m; pixel size 1000 m; same coordinate systems and projections as above.

- Subclass vs Aggregate summarisation:
  - The 25m data has been summarised to 1km grids in two ways: by LCM2000 Subclass and by LCM2000 Aggregate class.
  - Table 3 provides the correspondence between Subclasses and Aggregate classes and their attribute codes for each land cover type.

- Encoding and storage details:
  - LCM2000 Subclass codes (normally floating point with one decimal) are multiplied by 10 to store as unsigned 8-bit bytes (0–255).
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster.
  - The mapping includes various land-cover categories (e.g., Sea/Estuary, Water inland, Littoral rock/sediment, Bog, Grasslands, Woodlands, Arable, Urban, etc.) and their 1km and Aggregate class codes.

- Practical implications for Data Support:
  - Facilitates efficient storage and fast lookups while preserving detailed (25m) and aggregated (1km) classifications.
  - Enables integration with other datasets by providing explicit coordinate, projection, and coding conventions.
  - Requires decoding of integer codes to interpret land-cover classes for end users, and attention to the 12.5 m pixel-centre offset when precise geolocation is needed.