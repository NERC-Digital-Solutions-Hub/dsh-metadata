# 25m raster

- The 25m raster dataset was created by converting land parcels within a vector dataset into a 25m grid, with each cell recording the dominant land cover as an LCM2000 Subclass.
- Great Britain (GB) and Northern Ireland (NI) datasets are described with detailed metadata (grid dimensions, extents, pixel size, coordinate system, projection, spheroid, and datums).

## 25m raster dataset details

- Great Britain (GB)
  - Columns/width: 24,400
  - Rows/height: 48,400
  - Lower left easting: 50,000 m
  - Lower left northing: 10,000 m
  - Pixel size: 25 m
  - Coordinate system: British National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy
  - Datum: OSGB 1936
- Northern Ireland (NI)
  - Columns/width: 7,600
  - Rows/height: 7,200
  - Lower left easting: 180,000 m
  - Lower left northing: 280,000 m
  - Pixel size: 25 m
  - Coordinate system: Irish National Grid
  - Projection: Transverse Mercator
  - Spheroid: Airy Modified 1849
  - Datum: Ireland 1965
- Pixel center reference: add 12.5 m to each lower-left value to locate the pixel centre.

## 1km raster

- The 1km raster is produced by summarising the 25m raster within a 1km grid.
- Great Britain (GB)
  - Columns: 700
  - Rows: 1,300
  - Pixel size: 1,000 m
  - Lower left coordinates: 0 (easting/northing)
- Northern Ireland (NI)
  - Columns: 500
  - Rows: 500
  - Pixel size: 1,000 m
  - Lower left coordinates: 0 (easting/northing)
- Coordinate system, projection, spheroid, and datums match the corresponding 25m datasets (GB: OSGB 1936; NI: Ireland 1965; Transverse Mercator).

## Subclass vs Aggregate class and coding

- The 25m data can be summarised in two ways: by LCM2000 Subclass or by LCM2000 Aggregate class.
- To store efficiently in a raster, LCM2000 Subclass codes (normally floating with one decimal place) are multiplied by 10 to store as unsigned 8-bit bytes (0–255). Example: Water (inland) Subclass code 22.1 becomes 221 in the raster.
- The 1km raster uses corresponding codes (e.g., Sea/Estuary Subclass 25m code 221 maps to 1km Subclass code 1). Aggregate class codes are also provided (e.g., Oceanic seas code 10 for 1km).
- Table 3 provides the detailed correspondence between:
  - Sea/Estuary, Subclass
  - Water (inland), Subclass
  - Littoral rock/sediment, Supra-littoral rock/sediment
  - Bog, Heath, Woodland, Grassland, Arable, Urban, etc.
- Examples from the correspondence:
  - Sea/Estuary – 25m Subclass code 221; 1km Subclass code 1; Aggregate class “Oceanic seas” 1 km code 10.
  - Water (inland) – 25m Subclass code 131; 1km Subclass code 2; Aggregate class “Standing open water” 1 km code 8.
  - Littoral rock – 25m Subclass code 201; 1km Subclass code 3; Aggregate class “Coastal” 1 km code 9.
- The full mapping covers a wide range of land cover types, down to specific classes such as bog, dwarf shrub heath, arable crops, urban areas, and various woodland types.

## Metadata, data quality, and organisation

- The dataset uses explicit metadata to define grid dimensions, extents, pixel size, coordinate systems, projections, spheroids, and datums for both GB and NI.
- The encoding scheme (8-bit integers with scaled Subclass codes) supports compact storage and cross-scale consistency between 25m and 1km rasters.
- The mapping between Subclass and Aggregate classes enables flexible reporting at different thematic resolutions (detailed Subclasses or broader Aggregate classes).

## Relevance for monitoring and policy evaluation

- Provides a consistent, cross-regional (GB and NI) land cover framework suitable for environmental health monitoring and trend analysis.
- Facilitates integration within monitoring frameworks by supplying:
  - Clear spatial resolution options (25m and aggregated 1km) for habitat and land-cover indicators.
  - A well-documented code scheme and explicit cross-scale mappings to support dashboards, reports, and policy evaluation.
  - A standardized basis for data fusion with other environmental datasets through consistent coordinate systems and metadata.

## Considerations for use

- Data transformation and interpretation require awareness of the encoding: Subclass codes are stored as scaled integers (0–255) and must be decoded using the provided mapping.
- The level of detail (25m Subclass vs Aggregate) should be chosen based on the monitoring objective and reporting needs.
- Metadata completeness and clarity are essential to enable external data sharing, reproducibility, and governance of the monitoring outputs.