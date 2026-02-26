# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- British Antarctic Survey conducted a high-resolution LiDAR survey over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Production of digital terrain model (DTM) and digital surface model (DSM) layers at approximately 1 m grid resolution with vertical accuracy around 25 cm.
- Study area covers 9,424 km² west of Exmouth.

## Data Description
- Spatial extent: 9,424 km²; area west of Exmouth (roughly west of 3°21′W).
- Layers: DTM (bare-earth height) and DSM (bare-earth plus features like buildings/vegetation) represented as 2 cm height layers.
- Resolution and accuracy: 1 m grid cells; average vertical accuracy ~25 cm.
- Data attributes: Elevation, height measured in metres.
- Tile structure: Available as individual ESRI grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
- Coordinate reference system: OSGB 1936 / British National Grid (EPSG:27700).

## Data Collection and Processing
- Survey scope: 26 flights totaling 14,817 line km of new LiDAR data over 9,424 km².
- Data density: approximately 1 point per m².
- Overlap: about 300 m between data swaths to ensure complete coverage.
- Sensor and platform: Optech ALTM 3100 EA scanning LiDAR with integrated GPS/INS, mounted on BAS Twin Otter aircraft.
- Calibration and inputs: Raw range files, post-processed SBET, SMRSMG accuracy files, calibration files, flight logs, and any ground-truth survey details.
- Processing workflow: Terrascan software used by Environment Agency Geomatics to generate DSM and DTM from the calibrated point cloud.
  
## Quality Assurance and Validation
- Quality control: DSM and DTM validated against existing LiDAR datasets and GPS ground-truth data.
- Documentation: EA QC report summarising accuracy and limitations; supporting references include the BASS survey report and the EA QC report.

## Access, Documentation, and Governance
- Data access: Provided as individual ESRI grid tile files.
- Documentation and context: Overview of the Tellus project available at http://www.tellusgb.ac.uk/.
- Provenance and governance: Detailed calibration files, flight logs, and ground-truth data support data provenance and reproducibility of the products.