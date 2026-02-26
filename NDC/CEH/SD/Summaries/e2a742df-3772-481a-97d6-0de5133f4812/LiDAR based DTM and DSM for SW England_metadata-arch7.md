# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- High-resolution LiDAR-derived Digital Terrain Model (DTM) and Digital Surface Model (DSM) for Cornwall and Devon, part of the Tellus South West project.
- Area: 9,424 km2, all land west of Exmouth (west of ~3°21'W).
- Outputs: DSM (features on the bare earth, e.g., buildings, vegetation) and DTM (bare-earth topography).
- Purpose for GIS: enables map-based visualisations and spatial analyses of terrain and surface features for policy, planning, and public-facing applications.

## Data Details
- Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Resolution and accuracy: 1 m grid cells; average vertical accuracy ~25 cm.
- Data attributes: Elevation (Height) in metres.
- Format and structure: ESRI grid format; data delivered as individual flight-line files (e.g., OS grid tiles such as SX37ne, SX37nw, SX37se, SX37sw).

## Acquisition & Processing
- Collection period: July–August 2013.
- Platform and sensors: BAS Twin Otter aircraft carrying an Optech ALTM 3100 EA LiDAR system with integrated Applanix GPS/INS.
- Coverage and sampling: 26 survey flights, ~14,817 line km of LiDAR data over 9,424 km2, with ~300 m overlap between data swaths.
- Processing workflow: Environment Agency Geomatics used Terrascan to convert calibrated LAS point clouds into DSM and DTM layers.
- Calibration and QA inputs: Raw range files, post-processed SBET, SMRSMG accuracy files, calibration files, flight logs, ground truth data, and the calibrated LAS point cloud (per flight line).

## Quality Assurance
- Validation: DSM and DTM compared against existing LiDAR data and GPS ground-truth data.
- Documentation: EA QC report detailing accuracy and limitations of the products.

## Usage and References
- Project overview: Tellus SW (web: http://www.tellusgb.ac.uk/).
- Supporting documents: BASS survey report; EA QC report.