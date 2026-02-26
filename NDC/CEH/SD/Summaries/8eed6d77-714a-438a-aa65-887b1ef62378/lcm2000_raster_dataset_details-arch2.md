# 25m raster

- The 25m raster dataset is created by converting land parcels from a vector dataset into a 25m grid. Each grid cell stores the dominant land cover using LCM2000 Subclasses.
- The dataset covers Great Britain and Northern Ireland with specific metadata for each region.

## 25m raster details (Great Britain and Northern Ireland)

- Great Britain: width 24,400 pixels, height 48,400 pixels; lower left easting 50,000 m; lower left northing 10,000 m; pixel size 25 m; coordinate system British National Grid; projection Transverse Mercator; Spheroid Airy; Datum OSGB 1936.
- Northern Ireland: width 7,600 pixels, height 7,200 pixels; lower left easting 180,000 m; lower left northing 280,000 m; pixel size 25 m; coordinate system Irish National Grid; projection Transverse Mercator; Spheroid Airy Modified 1849; Datum Ireland 1965.
- Note: The values refer to the lower left corner of the lower left pixel; to obtain the pixel centre, add 12.5 m to each coordinate.

## 1km raster

- The LCM2000 raster 1km data are produced by summarising the 25m raster within 1km grid cells.
- Great Britain: width 700 pixels, height 1,300 pixels; lower left easting/northing = 0 m; pixel size 1000 m; same coordinate system and projection as 25m.
- Northern Ireland: width 500 pixels, height 500 pixels; lower left easting/northing = 0 m; pixel size 1000 m; same coordinate system and projection as 25m.
- Note: To obtain the pixel centre for 1km rasters, add 500 m to each lower-left value.

## Classification and coding of the rasters

- The 25m data can be summarised in two ways: by LCM2000 Subclass and by LCM2000 Aggregate class.
- Table 3 provides the correspondence between Subclasses and Aggregate classes and their attribute codes.
- Coding approach: 25m Subclass codes are typically floating-point with one decimal place but are multiplied by 10 for storage as unsigned 8-bit bytes (0–255). Example: Water (inland) Subclass code 22.1 becomes 221 in the raster dataset.

## Key mappings (Table 3, summarized)

- Sea / Estuary
  - 25m Subclass code: 221
  - 1km Subclass code: 1
  - Aggregate class: Oceanic seas
  - 1km Aggregate code: 10
- Water (inland)
  - 25m Subclass: 131
  - 1km Subclass code: 2
  - Aggregate class: Standing open water
  - 1km Aggregate code: 8
- Littoral rock
  - 25m Subclass: 201
  - 1km Subclass code: 3
  - Aggregate class: Coastal
  - 1km Aggregate code: 9
- Saltmarsh
  - 25m Subclass: 212
  - 1km Subclass code: 5
  - Aggregate class: Coastal
  - 1km Aggregate code: 9
- Supra-littoral rock
  - 25m Subclass: 181
  - 1km Subclass code: 6
  - Aggregate class: Coastal
  - 1km Aggregate code: 9
- Supra-littoral sediment
  - 25m Subclass: 191
  - 1km Subclass code: 7
  - Aggregate class: Coastal
  - 1km Aggregate code: 9
- Bog (deep peat)
  - 25m Subclass: 121
  - 1km Subclass code: 8
  - Aggregate class: Mountain, heath, bog
  - 1km Aggregate code: 6
- Dense dwarf shrub heath
  - 25m Subclass: 101
  - 1km Subclass code: 9
  - Aggregate class: Mountain, heath, bog
  - 1km Aggregate code: 6
- Open dwarf shrub heath
  - 25m Subclass: 102
  - 1km Subclass code: 10
  - Aggregate class: Mountain, heath, bog
  - 1km Aggregate code: 6
- Montane habitats
  - 25m Subclass: 151
  - 1km Subclass code: 11
  - Aggregate class: Mountain, heath, bog
  - 1km Aggregate code: 6
- Broad-leaved / mixed woodland
  - 25m Subclass: 11
  - 1km Subclass code: 12
  - Aggregate class: Broad-leaved / mixed woodland
  - 1km Aggregate code: 1
- Coniferous woodland
  - 25m Subclass: 21
  - 1km Subclass code: 13
  - Aggregate class: Coniferous woodland
  - 1km Aggregate code: 2
- Improved grassland
  - 25m Subclass: 51
  - 1km Subclass code: 14
  - Aggregate class: Improved grassland
  - 1km Aggregate code: 4
- Neutral grassland
  - 25m Subclass: 61
  - 1km Subclass code: 15
  - Aggregate class: Semi-natural grassland
  - 1km Aggregate code: 5
- Setaside grassland
  - 25m Subclass: 52
  - 1km Subclass code: 16
  - Aggregate class: Semi-natural grassland
  - 1km Aggregate code: 5
- Bracken
  - 25m Subclass: 91
  - 1km Subclass code: 17
  - Aggregate class: Semi-natural grassland
  - 1km Aggregate code: 5
- Calcareous grassland
  - 25m Subclass: 71
  - 1km Subclass code: 18
  - Aggregate class: Semi-natural grassland
  - 1km Aggregate code: 5
- Acid grassland
  - 25m Subclass: 81
  - 1km Subclass code: 19
  - Aggregate class: Semi-natural grassland
  - 1km Aggregate code: 5
- Fen, marsh, swamp
  - 25m Subclass: 111
  - 1km Subclass code: 20
  - Aggregate class: Semi-natural grassland
  - 1km Aggregate code: 5
- Arable cereals
  - 25m Subclass: 41
  - 1km Subclass code: 21
  - Aggregate class: Arable and horticulture
  - 1km Aggregate code: 3
- Arable horticulture
  - 25m Subclass: 42
  - 1km Subclass code: 22
  - Aggregate class: Arable and horticulture
  - 1km Aggregate code: 3
- Arable non-rotational
  - 25m Subclass: 43
  - 1km Subclass code: 23
  - Aggregate class: Arable and horticulture
  - 1km Aggregate code: 3
- Suburban / rural developed
  - 25m Subclass: 171
  - 1km Subclass code: 24
  - Aggregate class: Built up areas and gardens
  - 1km Aggregate code: 7
- Continuous urban
  - 25m Subclass: 172
  - 1km Subclass code: 25
  - Aggregate class: Built up areas and gardens
  - 1km Aggregate code: 7
- Inland bare ground
  - 25m Subclass: 161
  - 1km Subclass code: 26
  - Aggregate class: Mountain, heath, bog
  - 1km Aggregate code: 6

## Notes and considerations for analysis

- The rasters provide a standardised representation of land cover across Great Britain and Northern Ireland, suitable for monitoring environmental condition and policy performance over time.
- Data quality checks, verification, cleaning, and transformation are applied before analysis.
- Outputs are presented in clear formats (e.g., maps, charts, reports) and datasets are stored/uploaded to appropriate portals to support access and reuse.
- Challenges highlighted for analysts:
  - Increasing the value of datasets by combining them with other relevant data (avoiding single-use applications).
  - Enabling others to access the underlying data used to create final outputs.