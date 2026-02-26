# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

- Overview
  - British Antarctic Survey (BAS) collected a new high-resolution LiDAR dataset over Cornwall and Devon during July–August 2013 for the Tellus South West project.
  - Data aim: high-accuracy digital terrain model (DTM) and digital surface model (DSM) with ~1 point per m2 density and ~25 cm vertical accuracy.
  - DTM represents bare earth; DSM includes heights of features on the bare earth (e.g., buildings, vegetation).
  - Spatial scope: 9424 km2 area west of Exmouth (west of ~3°E21′W). Coordinate system: OSGB 1936/British National Grid (EPSG:27700).

- Data products and attributes
  - Two height layers at 1 m resolution: terrain (DTM) and surface (DSM) height.
  - Elevation attribute: Height (units: metres).
  - Data accessible as individual files corresponding to OS tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).

- Experimental design and coverage
  - 26 LiDAR survey flights yielding 14817 line km of data across 9424 km2.
  - Designed to achieve ~300 m swath overlap and meet target specifications: 25 cm vertical accuracy; 1 point per m2 data density.

- Collection methods
  - Instrument: Optech ALTM 3100 EA scanning laser with integrated Applanix GPS/INS.
  - Platform: BAS Twin Otter aircraft (VP-FBL).

- Calibration, processing, and data lineage
  - Calibration inputs: raw range files; post-processed SBET files; SMRSMG accuracy files; calibration files; flight logs; ground truth survey details.
  - Output: calibrated LAS point cloud delivered as individual flight lines.
  - Processing: Environment Agency Geomatics used Terrascan software to derive DSM and DTM from the calibrated point cloud.

- Quality control and validation
  - DSM and DTM validated against existing LIDAR datasets and GPS ground truth data.
  - QA/QA summary provided in EA QC report detailing accuracy and limitations.

- Access, metadata, and references
  - Data and project information available via Tellus South West resources.
  - Supporting documents: BASS survey report; EA QC report.