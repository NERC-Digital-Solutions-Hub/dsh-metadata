# 25m raster

- The 25m raster dataset was created by converting land parcels from the vector dataset into a 25m grid, with each cell recording the dominant land cover as an LCM2000 Subclass.
- Separate datasets exist for Great Britain and Northern Ireland.

## 25m raster details ( GB and NI )

- Grid resolution and size:
  - Great Britain: 24,400 columns × 48,400 rows
  - Northern Ireland: 7,600 columns × 7,200 rows
- Lower left corner coordinates:
  - Great Britain: easting 50,000 m, northing 10,000 m
  - Northern Ireland: easting 180,000 m, northing 280,000 m
- Pixel size: 25 m (both GB and NI)
- Coordinate system and projection:
  - Great Britain: British National Grid (OSGB 1936), Transverse Mercator
  - Northern Ireland: Irish National Grid, Transverse Mercator
- Spheroid and datum:
  - Great Britain: Airy; OSGB 1936
  - Northern Ireland: Airy Modified 1849; Ireland 1965
- Pixel centre adjustment: To obtain the pixel centre, add 12.5 m to lower-left corner coordinates.

## 1km raster details ( GB and NI )

- The 1km raster was created by summarising the 25m raster within a 1km grid.
- Grid size:
  - Great Britain: 700 columns × 1,300 rows
  - Northern Ireland: 500 columns × 500 rows
- Lower left corner coordinates:
  - Great Britain: easting 0 m, northing 0 m
  - Northern Ireland: easting 0 m, northing 0 m
- Pixel size: 1,000 m (1 km) for both GB and NI
- Coordinate system and projection:
  - Great Britain: British National Grid, Transverse Mercator
  - Northern Ireland: Irish National Grid, Transverse Mercator
- Spheroid and datum:
  - Great Britain: Airy; OSGB 1936
  - Northern Ireland: Airy Modified 1849; Ireland 1965
- Pixel centre adjustment: To obtain the pixel centre, add 500 m to lower-left corner coordinates.

## Subclass to Aggregate class mapping (Table 3)

- The 25m raster uses LCM2000 Subclass codes; for storage efficiency these codes (normally floating point with one decimal) are converted to unsigned 8-bit values by multiplying by 10 (e.g., Water (inland) with code 22.1 becomes 221).
- A crosswalk (Table 3) provides the correspondence between:
  - LCM2000 Subclass codes (25m)
  - LCM2000 Subclass codes (1km)
  - LCM2000 Aggregate class codes (1km)
  - LCM2000 Aggregate class names
- Examples from the mapping:
  - Sea / Estuary
    - 25m Subclass code: 221
    - 1km code: 1
    - Aggregate class: Oceanic seas; 1km code 10
  - Water (inland)
    - 25m Subclass code: 131
    - 1km code: 2
    - Aggregate class: Standing open water; 1km code 8
  - Littoral rock
    - 25m Subclass code: 201
    - 1km code: 3
    - Aggregate class: Coastal; 1km code 9
  - Saltmarsh
    - 25m Subclass code: 212
    - 1km code: 5
    - Aggregate class: Coastal; 1km code 9
  - Supra-littoral rock
    - 25m Subclass code: 181
    - 1km code: 6
    - Aggregate class: Coastal; 1km code 9
  - Supra-littoral sediment
    - 25m Subclass code: 191
    - 1km code: 7
    - Aggregate class: Coastal; 1km code 9
  - Bog (deep peat)
    - 25m Subclass code: 121
    - 1km code: 8
    - Aggregate class: Mountain, heath, bog; 1km code 6
  - Dense dwarf shrub heath
    - 25m Subclass code: 101
    - 1km code: 9
    - Aggregate class: Mountain, heath, bog; 1km code 6
- The full crosswalk provides mappings for all LCM2000 Subclasses and their corresponding 1km and Aggregate class codes.

## Encoding and data management

- Subclass codes (LCM2000) are stored as unsigned 8-bit integers by multiplying by 10 (to remove the decimal place).
- Outputs are designed to support categorising land cover against standards and to be presented in clear formats like reports, maps, and charts.
- Datasets are stored and made available through appropriate data portals, ensuring accessibility of the underlying data used to create the final outputs.

## Relevance for environmental monitoring

- Provides standardized, multi-scale land cover information (25m and 1km) for Great Britain and Northern Ireland.
- Enables consistent assessment of environmental health and policy performance over time by using a common coding scheme and crosswalk between grid scales.
- Supports integration with other data sources by providing documented metadata, coordinate systems, and data encodings.

## Challenges and opportunities

- Challenge: Increase the value of datasets by combining them with other relevant data sources rather than using them in isolation.
- Challenge: Facilitate access to the underlying data used to generate the final outputs for broader scrutiny and reuse.