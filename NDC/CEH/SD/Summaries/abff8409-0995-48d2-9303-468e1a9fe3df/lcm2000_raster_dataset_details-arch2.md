# 25m raster

## Purpose and scope
- Describes the 25m land cover raster dataset derived from land parcels, using the LCM2000 Subclasses to represent dominant land cover at each 25m grid cell.
- Supports environmental monitoring by providing a standardized, auditable base for assessing environmental health and policy performance over time.
- Two GB/NI raster products are documented: a 25m raster and a corresponding 1km raster derived from the 25m data.

## 25m raster: dataset details
- Creation: Land parcels in the vector dataset converted to a 25m grid; each cell records the dominant land cover per LCM2000 Subclass.
- Coverage:
  - Great Britain: 24400 columns × 48400 rows; lower-left easting 50000 m, northing 10000 m; pixel size 25 m; coordinate system British National Grid; projection Transverse Mercator; datum OSGB 1936; spheroid Airy.
  - Northern Ireland: 7600 columns × 7200 rows; lower-left easting 180000 m, northing 280000 m; pixel size 25 m; coordinate system Irish National Grid; projection Transverse Mercator; datum Ireland 1965; spheroid Airy Modified 1849.
- Data encoding: LCM2000 Subclass codes (floating point with one decimal) are stored as unsigned 8-bit bytes by multiplying by 10 (0–255). Example: Water (inland) Subclass 22.1 becomes 221 in the raster dataset.
- Metadata notes: Values shown in tables refer to the pixel lower-left corner; for pixel centers, add 12.5 m to each coordinate.

## 1km raster: dataset details
- Creation: Summarised from the 25m raster within 1km grid cells.
- Coverage:
  - Great Britain: 700 columns × 1300 rows; lower-left origin at 0 m; pixel size 1000 m; British National Grid; projection Transverse Mercator; datum OSGB 1936; spheroid Airy.
  - Northern Ireland: 500 columns × 500 rows; origin at 0 m; pixel size 1000 m; Irish National Grid; projection Transverse Mercator; datum Ireland 1965; spheroid Airy Modified 1849.
- Data encoding: Similar 8-bit encoding approach as the 25m raster, with codes reflecting either Subclass or Aggregate class depending on the chosen summarisation method.

## Subclass and Aggregate class mapping (Table 3)
- The 25m raster supports two summarisation schemes:
  - By LCM2000 Subclass (detailed land cover types at 25m and 1km).
  - By LCM2000 Aggregate class (broader land cover groupings).
- The mapping table provides:
  - Correspondence between Subclass codes and their 1km equivalents.
  - Corresponding Aggregate class names and 1km codes.
- Examples:
  - Sea/Estuary: 25m Subclass code 221; 1km code 10 (Aggregate: Oceanic seas; Subclass: Sea/Estuary).
  - Water (inland): 25m Subclass code 131; 1km code 8 (Aggregate: Standing open water; Subclass: Water (inland)).
  - Littoral rock: 25m Subclass code 201; 1km code 9 (Aggregate: Coastal; Subclass: Littoral rock).
  - Arable cereals: 25m Subclass code 41; 1km code 21 (Aggregate: Arable and horticulture; Subclass: Arable cereals).
- The complete table includes many land-cover types across Sea/Estuary, Water, Coastal, Grassland, Woodlands, Arable, Urban, and Mountain categories, with both Subclass and Aggregate coding schemes.

## Practical implications for environment analysts
- Standardised data representation across Great Britain and Northern Ireland enables consistent monitoring and time-series analysis of land cover changes.
- The 25m-to-1km approach supports scalable analysis from detailed to broader contexts, suitable for policy performance reporting, monitoring, and regional assessments.
- Encoding into 8-bit rasters facilitates storage efficiency and compatibility with common GIS workflows and portals.
- Clear documentation of coordinate systems, datums, and pixel-centre adjustments aids reproducibility and data provenance.
- Encourages integration with other datasets by providing explicit codes and a consistent framework for cross-dataset comparisons.

## Notes for data users
- Pixel centre adjustments:
  - 25m dataset: add 12.5 m to lower-left coordinates to locate pixel centers.
  - 1km dataset: add 500 m to locate pixel centers.
- datasets are designed for storage efficiency and GIS compatibility and are intended to support routine monitoring and reporting workflows.