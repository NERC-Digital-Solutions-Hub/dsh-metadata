# 25m raster

- The 25m raster dataset is created by converting land parcels from the LCM2000 vector data into a 25-meter grid, with each cell recording the dominant land cover as a LCM2000 Subclass.
- The 1km raster is derived by summarising the 25m raster within 1km grid cells.

## 25m raster: metadata and structure

- Great Britain: 24,400 columns by 48,400 rows; Northern Ireland: 7,600 columns by 7,200 rows.
- Lower left corner coordinates: GB easting 50,000 m, northing 10,000 m; NI easting 180,000 m, northing 280,000 m.
- Pixel size: 25 m (centroid offset of 12.5 m from lower-left corner).
- Coordinate systems and projections:
  - Great Britain: British National Grid, Transverse Mercator, OSGB 1936, Airy spheroid.
  - Northern Ireland: Irish National Grid, Transverse Mercator, Ireland 1965, Airy Modified 1849.
- Purpose: to map land cover at a 25m resolution using LCM2000 Subclasses.

## 1km raster: metadata and structure

- Great Britain: 700 columns by 1,300 rows; Northern Ireland: 500 columns by 500 rows.
- Lower left corner coordinates: GB and NI both start at 0 for easting and northing.
- Pixel size: 1,000 m (1 km).
- Coordinate systems and projections match the 25m dataset (OSGB 1936 for GB; Ireland 1965 for NI).

## Classification and encoding

- The 25m data can be summarised in two ways:
  - By LCM2000 Subclass (fine-grained codes).
  - By LCM2000 Aggregate class (coarser categories).
- Encoding note: LCM2000 Subclass codes (originally floating point with one decimal place) are stored as unsigned 8-bit bytes by multiplying by 10 (e.g., Water (inland) Subclass 22.1 becomes 221).
- The 1km data provides corresponding codes for both Subclass and Aggregate classes (with specific 1km codes).

## Subclass to Aggregate class mapping (Table 3)

- A comprehensive crosswalk links each 25m Subclass to an Aggregate class and provides corresponding 1km codes.
- Example categories included in the mapping:
  - Sea/Estuary; Water (inland); Littoral rock; Littoral sediment; Saltmarsh; Supra-littoral rock/sediment.
  - Land cover groups: Bog, various dwarf/shrub heath and montane habitats; broad-leaved/mixed woodland; coniferous woodland; various grasslands (improved, neutral, setaside, Bracken, calcareous, acid); fen/marsh/swamp; arable and horticulture (cereals, horticulture, non-rotational); suburban/rural developed; continuous urban; inland bare ground.
- Each category has a 25m Subclass code, a 1km code, and an Aggregate class with its 1km code, enabling translation across resolutions.

## Practical implications for analysis

- The datasets enable multi-scale land-cover analyses by providing consistent crosswalks between 25m Subclasses, 25m Aggregates, and 1km aggregates.
- The encoding scheme (0–255 via scaled Subclass codes) facilitates efficient storage and quick lookups in analyses and scripts.
- The metadata supports reproducible analyses across Great Britain and Northern Ireland with aligned coordinate systems, projections, and datums.

## Data provenance and usage notes

- Both rasters share compatible coordinate systems and datums, ensuring integrability with other GB and NI geospatial data.
- The explicit pixel size, grid dimensions, and corner coordinates support precise spatial alignment when combining with other datasets.
- The detailed mapping between classifications supports transparent interpretation of land-cover results and reproducibility of scale-dependent analyses.