# 25m raster

- What it is: The raster 25m dataset is created by converting land parcels within a vector dataset into a 25-meter grid. Each grid cell records the dominant land cover, represented by LCM2000 Subclasses.

- Coverage and resolution:
  - Great Britain: 24,400 columns × 48,400 rows
  - Northern Ireland: 7,600 columns × 7,200 rows
  - Pixel size: 25 meters
  - Lower left corner coordinates provided in meters (specific to GB and NI)

- Coordinate systems and projection:
  - Great Britain: British National Grid, Transverse Mercator, OSGB 1936, Spheroid Airy
  - Northern Ireland: Irish National Grid, Transverse Mercator, Ireland 1965, Spheroid Airy Modified 1849

- Pixel centre reference:
  - For the pixel centre, add 12.5 meters to each of the lower-left corner values.

- Data coding and storage:
  - LCM2000 Subclass codes are typically floating point with one decimal place.
  - For efficient raster storage, codes are multiplied by 10 and stored as unsigned 8-bit bytes (0–255). Example: Water (inland) Subclass 22.1 becomes 221.

- Subclass to code mapping (summary):
  - The dataset provides a mapping between Subclasses and Aggregate classes, with corresponding 1km codes. Examples include:
    - Sea/Estuary: Subclass 22.1 → 1km code 10 → Aggregate class Oceanic seas
    - Water (inland): Subclass 13.1 → 1km code 2 → Aggregate class Standing open water
    - Littoral and supra-littoral categories: mapped to Coastal aggregate class with specific 1km codes
    - Various grassland, woodland, arable, and urban categories mapped to their respective Aggregate classes and 1km codes

- 1km raster (created from 25m data):
  - Summary of 25m data within 1km grid
  - Great Britain: 700 columns × 1,300 rows
  - Northern Ireland: 500 columns × 500 rows
  - Pixel size: 1000 meters
  - Coordinate system and projection mirror the 25m datasets (GB: OSGB 1936 / British National Grid; NI: Ireland 1965 / Irish National Grid; both Transverse Mercator)
  - Lower left corner values start at 0 for both GB and NI

- Practical implications for data use:
  - The 25m raster provides detailed, high-resolution land-cover information by recording a single dominant class per 25m cell.
  - The 1km raster offers a coarser, storage-efficient representation by aggregating 25m results into 1km cells.
  - The 8-bit storage approach (code × 10) supports compact data handling in raster formats.
  - The dedicated mapping table (Table 3) enables translating between 25m Subclass codes, 1km codes, and Aggregate class designations for cross-resolution analyses.