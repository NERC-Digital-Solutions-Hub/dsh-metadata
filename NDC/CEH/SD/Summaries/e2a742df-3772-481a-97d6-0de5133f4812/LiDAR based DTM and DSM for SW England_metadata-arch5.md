# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Summary for Data Stewards

- Purpose and scope
  - High-resolution LiDAR dataset over Cornwall and Devon collected for the Tellus South West project in July–August 2013.
  - Provides Digital Terrain Model (DTM, bare earth) and Digital Surface Model (DSM, includes features such as buildings and vegetation) at 1 m grid resolution with high vertical accuracy.

- Data content and structure
  - Area covered: 9,424 km², west of Exmouth (approximately west of 3°21′W).
  - Layers: two height layers representing terrain and surface heights.
  - Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
  - File formats: data available as individual ESRI grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
  - Attributes: Elevation (height) with units in metres.

- Collection details
  - Sensor and platform: Optech ALTM 3100 EA LiDAR system with integrated Applanix GPS/INS, mounted in a BAS Twin Otter aircraft.
  - Coverage and density: 26 survey flights totaling 14,817 line km, designed for ~300 m swath overlap to achieve ~1 point/m² data density.
  - Temporal window: July–August 2013.
  - Data provenance: raw range files, SBET position data, SMRSMG accuracy files, calibration files, flight logs, and any ground-truth surveys.

- Processing and production
  - Processing workflow: Terrascan used to convert calibrated point clouds into DSM and DTM layers.
  - Deliverables: calibrated LAS point clouds delivered as individual flight lines.
  - Quality control: DSM and DTM validated against existing LiDAR and GPS ground-truth data; EA QC report documents accuracy and limitations.

- Quality and accuracy
  - Reported vertical accuracy: approximately 25 cm.
  - Data density target: ~1 point per m².
  - QA artifacts: EA QC report; BASS survey report referenced for supporting validation.

- Access, metadata and documentation
  - Primary data access through the Tellus SW project resources (web: http://www.tellusgb.ac.uk/).
  - Supporting documentation: BASS survey report and EA QC report.
  - Data governance considerations for stewards:
    - Maintain provenance by tracking raw inputs (range files, SBET, calibration data) and processing steps (Terrascan settings).
    - Document spatial extents, tile naming, and coordinate systems to ensure interoperability with other systems.
    - Ensure metadata captures coverage, resolution, accuracy, collection dates, instrument details, processing software, and QA outcomes.
    - Monitor and communicate any data updates or corrections and maintain versioning across tiles.

- Relationships and constraints
  - Data is organized as discrete OS grid tiles; integration across tiles may require consistent mosaicking practices.
  - Coverage focuses on western Cornwall and Devon; ensure users understand the geographic extent and boundaries.
  - No embargo or access restrictions are stated; stewardship should confirm any usage or licensing requirements in accompanying metadata.