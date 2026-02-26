# 25m raster

- What it is: A raster dataset created by converting land parcels within a vector dataset into a 25-meter grid, where each cell records the dominant land cover as an LCM2000 Subclass. Covers Great Britain and Northern Ireland, with metadata provided in Tables 1–3.

- Spatial and basic metadata (25m raster):
  - Great Britain: 24,400 columns × 48,400 rows.
  - Northern Ireland: 7,600 columns × 7,200 rows.
  - Lower left easting/northing: GB 50,000 m; NI 180,000 m.
  - Pixel size: 25 m for both GB and NI.
  - Coordinate system and projection: GB uses British National Grid with Transverse Mercator; NI uses Irish National Grid with Transverse Mercator.
  - Spheroid and datum: GB uses Airy; NI uses Airy Modified 1849; GB datum OSGB 1936; NI Ireland 1965.
  - Pixel centre reference: add 12.5 m to easting/northing to obtain pixel centre coordinates.

- 1km raster (summary of the 25m data):
  - Created by summarising the 25m raster within a 1km grid.
  - Great Britain: 700 columns × 1,300 rows.
  - Northern Ireland: 500 columns × 500 rows.
  - Pixel size: 1,000 m.
  - Coordinate system, projection, and datums match the 25m data (GB: OSGB 1936; NI: Ireland 1965; Transverse Mercator; Airy / Airy Modified 1849).
  - Pixel centre reference: add 500 m to lower-left coordinates to obtain pixel centre.

- Data encoding and storage efficiency:
  - The 25m Subclass codes are typically floating point with one decimal place but are stored as unsigned 8-bit bytes by multiplying by 10 (0–255). Example: Water (inland) Subclass 22.1 becomes 221.

- Two summarisation schemes for 25m data:
  - LCM2000 Subclass: fine-grained classification, stored as scaled 8-bit codes.
  - LCM2000 Aggregate class: coarser groupings, used for broader analyses and compatible with the 1km grid.

- Crosswalk between 25m Subclasses and 1km Aggregates (Table 3 concept):
  - Each 25m Subclass has a corresponding 1km code and an Aggregate class with its own 1km code.
  - Example crosswalk: Sea/Estuary Subclass 25m code 221 maps to 1km code 1 and Aggregate class Oceanic seas with 1km code 10.
  - This crosswalk supports translating detailed 25m classifications to 1km resolution for analyses at different scales.

- Land cover categories represented (high-level):
  - Sea/Estuary, Water (inland), Littoral and Supra-littoral rocks and sediments, Saltmarsh, bog, various grasslands (improved, neutral, arable-associated), woodlands (broad-leaved/mixed and coniferous), arable crops (cereals, horticulture, non-rotational), urban/suburban developed, inland bare ground, and montane habitats.
  - Each category is defined both in Subclass terms (finer detail) and Aggregate terms (broader groupings) with corresponding 1km codes for compatibility.

- Implications for analysts:
  - Enables correlations and predictions across scales by providing a consistent 25m base and a summarised 1km layer.
  - Facilitates data integration with other datasets via the explicit crosswalk between Subclass and Aggregate classifications.
  - Requires attention to coordinate system differences between Great Britain and Northern Ireland when combining datasets.