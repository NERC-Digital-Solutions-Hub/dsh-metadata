# Silene uniflora populations GPS extents dataset

- Temporal scope: Observations collected during field work between February 2018 and September 2021.
- Data provenance: Sites identified from Botanical Society of the British Isles records, existing literature, and communication with county recorders; visits conducted to record population extents.
- Spatial reference: GPS-based extents recorded as latitude and longitude in decimal degrees, datum WGS84.
- Habitat information: Broad habitat/substrate types recorded per population (e.g., montane, coastal, mine, serpentine).
- Position accuracy and validation: GPS positions checked against satellite imagery to ensure correct location; quality control applied to verify spatial placement.
- Data structure and format:
  - 56 rows in the dataset, each representing a single population.
  - Columns:
    - Column 1: Population name (based on local area names/landmarks).
    - Column 2: Population code (used for a connected dataset).
    - Column 3: Habitat type.
    - Remaining columns: Pairs of latitude/longitude positions that define the bounding extents of the population site.
- Related datasets: The population data are linked to a connected dataset titled “Heavy metal tolerance records for Silene uniflora.”
- GIS implications:
  - The data provide polygonal extents (via bounding coordinate pairs) suitable for map-based visualization and spatial analysis in GIS.
  - Useful for cross-referencing with other geospatial layers and for assessing spatial patterns in habitat and potential metal tolerance contexts.