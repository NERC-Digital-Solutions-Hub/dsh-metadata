# DATA STRUCTURE

- File and format: MANURE-GIS_ManureVolumes_EnW.shp (shapefile) containing Manure volumes by livestock type and land use for England and Wales.

- Scope: Dataset of manure volumes categorized by livestock sector, manure type/housing, and destination land use type, with corresponding units.

- Attribute schema (selected patterns):
  - Column codes combine: Livestock Sector (e.g., Beef, Broilers, Dairy, Layers, Pigs, Sheep), Manure/Housing (Farmyard manure, Slurry, Direct excreta), and Destination Land Use Type (Grass, Arable Winter/Spring, Arable Spring, Arable Winter, or “-” for unspecified).
  - Units specify measurement: kilograms (kg) for Farmyard manure and Direct excreta; litres for Slurry.
  - Examples:
    - B_FYM_Gras: Beef, Farmyard manure, Grass, kilograms.
    - B_Slu_Gras: Beef, Slurry, Grass, litres.
    - P_OutGrazi: Pig Outdoor, Direct excreta, unspecified land use, kilograms.

- Special note:
  - S_Grazing field indicates only the proportion of sheep excreta deposited at grazing on managed grassland is included (excludes rough grazing).

- Geographic scope: England and Wales.

- Data governance implications for Data Stewards:
  - Metadata and data dictionary needed: map each coded column to a human-readable description, including units and scope.
  - Ensure consistency of units across fields; document any exceptions or conversion needs.
  - Maintain provenance and update cadence to reflect new volumes or revised estimates.
  - Provide clear documentation of the meaning of "-" land-use type entries and notes like the (*) caveat for grazing.
  - Ensure interoperability by supplying GIS-ready data alongside metadata; consider coordinating with user needs for downstream analyses.

- Quality and usability considerations:
  - The large number of coded columns may require a comprehensive codebook for end-users.
  - Validate completeness and accuracy of mappings between livestock, manure type, land use, and units.
  - Consider versioning and change logs when datasets are updated.