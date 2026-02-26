# 25m raster

- What it is: A 25m resolution raster created by converting land parcels from the vector dataset into a 25m grid, recording the dominant land cover using LCM2000 Subclasses.

- Spatial extent and resolution:
  - Great Britain: 24,400 columns × 48,400 rows; 25m pixel size
  - Northern Ireland: 7,600 columns × 7,200 rows; 25m pixel size
  - Pixel-centre offset note: add 12.5m to each lower-left corner value

- Spatial reference and projection:
  - Great Britain: British National Grid, Transverse Mercator, spheroid Airy, datum OSGB 1936
  - Northern Ireland: Irish National Grid, Transverse Mercator, spheroid Airy Modified 1849, datum Ireland 1965

- Lower-left corner coordinates:
  - GB: easting 50,000 m; northing 10,000 m (lower-left of lower-left pixel)
  - NI: easting 180,000 m; northing 280,000 m (lower-left of lower-left pixel)

- 1km raster (derived from 25m data):
  - GB: 700 columns × 1,300 rows; 1,000 m pixel size
  - NI: 500 columns × 500 rows; 1,000 m pixel size
  - Lower-left corner coordinates: same reference frameworks as 25m, with 500 m offset to pixel-centre

- Encoding and data types:
  - 25m Subclass codes (normally floating point with one decimal) are multiplied by 10 to store as unsigned 8-bit bytes (0–255)
  - Example: Water (inland) Subclass 22.1 becomes 221 in the raster

- Subclass to Aggregate class mapping (Table 3):
  - The 25m and 1km rasters include a correspondence between LCM2000 Subclasses and LCM2000 Aggregate classes, with corresponding codes
  - Examples of categories included: Sea/Estuary, Water (inland), Littoral rock/sediment, Bog, Dense/Open dwarf shrub heath, Montane habitats, Various woodland types, Grasslands (improved, neutral, set-aside, Bracken, Calcareous, Acid), Arable and horticulture, Suburban/rural developed, Continuous urban, Inland bare ground
  - This mapping links specific 25m codes to broader Aggregate class codes for 1km summarisations

- Data relations and purpose:
  - 1km raster summarises 25m data by aggregating to 1km grid
  - Used to store and analyse land-cover information efficiently at two resolutions
  - Enables GIS workflows that require consistent, standardized encodings and seamless spatial analysis across Great Britain and Northern Ireland

- Notes and practical considerations for GIS work:
  - Pixel values encode land-cover classes using a scaled Subclass-to-Aggregate framework
  - When converting between 25m and 1km, the relationship is defined by Table 3 mappings
  - Be aware of differing coordinate systems and datums between GB (OSGB 1936) and NI (Ireland 1965) when integrating with other datasets