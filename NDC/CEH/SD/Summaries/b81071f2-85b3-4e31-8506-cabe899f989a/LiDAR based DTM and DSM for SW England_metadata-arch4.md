# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- BAS acquired a high-resolution LiDAR dataset over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Raw LiDAR data were converted into Digital Terrain Model (DTM) and Digital Surface Model (DSM) by the Environment Agency (contract).

## Data Characteristics
- Resolution and accuracy: 2 cm height layers for terrain and surface at 1 m grid cell resolution; average vertical accuracy of 25 cm.
- Coverage: 9424 km², west of Exmouth (approximately west of 3°21′W).
- Data attributes: Elevation (Height) in metres.

## Data Structure and Format
- Provided as individual files representing Ordnance Survey tiles in ESRI grid format (e.g., SX37ne, SX37nw, SX37se, SX37sw).
- Coordinate system: OSGB 1936/British National Grid (EPSG:27700).
- DSM vs DTM: DTM = bare-earth terrain; DSM = features above bare earth (buildings, vegetation).

## Acquisition, Collection, and Processing
- Survey scope: 26 flights, 14,817 line km of new LiDAR data, covering 9,424 km² with ~300 m overlap between data swaths.
- Equipment: Optech ALTM 3100 EA scanning laser; integrated Applanix GPS/INS; mounted on BAS Twin Otter (VP-FBL).
- Processing: Environment Agency Geomatics used Terrascan to generate DSM and DTM from calibrated LAS point clouds.
- Calibration and quality assurance: Includes raw range files, SBET, SMRSMG accuracy files, calibration files, flight logs, and ground-truth details; calibrated LAS delivered per flight line.
- Quality control: DSM and DTM validated against existing LiDAR and GPS ground-truth data; EA QC report documents accuracy and limitations.

## Access, Output, and Documentation
- Output organization: data delivered as individual flight lines; project overview available at tellusgb.ac.uk.
- Supporting documents: BASS survey report; EA QC report.

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle management: data collection, processing, metadata, quality control, and documentation.
- Highlights data discoverability and provenance through tile-based organization and explicit metadata (resolution, accuracy, date, coverage).
- Shows cross-organization collaboration (BAS and Environment Agency) within a regional data program.

## Limitations and Considerations
- Spatial scope limited to Cornwall and Devon; excludes areas east of Exmouth.
- Vertical accuracy ~25 cm; DSM/DTM differences may occur in areas with dense vegetation.
- Large data volume considerations for storage, versioning, and ongoing updates.