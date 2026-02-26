# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- British Antarctic Survey acquired a high-resolution LiDAR dataset over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Conversion to digital terrain model (DTM) and digital surface model (DSM) was performed by the Environment Agency (contract).
- Dataset includes 2 cm height layering for terrain and surface, at 1 m grid resolution, with an average height accuracy of 25 cm.
- Coverage: 9,424 km² west of Exmouth (approximately 3°21'W), encompassing land west of Exmouth.
- Data are provided as individual files representing Ordnance Survey tiles in ESRI grid format (e.g., SX37ne, SX37nw, SX37se, SX37sw).

## Data products and formats
- DTM: topographic model of bare earth.
- DSM: height of features on the bare earth (buildings, vegetation) included.
- Data attributes: Elevation, measured in metres.
- Files: ESRI grid format by OS tiles; also available as calibrated LAS point cloud data delivered as individual flight lines.

## Spatial reference and coverage
- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700).
- Spatial extent: 9,424 km² over Cornwall and Devon region west of Exmouth.

## Experimental design and collection methods
- 26 LiDAR survey flights collected 14,817 line kilometers of data.
- Designed to achieve ~300 m overlap between swaths and meet 25 cm vertical accuracy with 1 point per m² data density.
- Equipment: Optech ALTM 3100 EA scanning laser, integrated Applanix GPS/INS; mounted in a BAS Twin Otter aircraft (VP-FBL).

## Data processing and quality control
- Processing: Terrascan software used by Environment Agency Geomatics to derive DSM and DTM from calibrated point cloud.
- Calibration inputs: Raw range files, post-processed SBET, SMRSMG accuracy files, calibration files, flight logs, and any ground truth data.
- Quality control: DSM/DTM validated against existing LiDAR datasets and GPS ground truth data; Quality Control (QC) reports produced by EA.

## Access, provenance, and supporting documentation
- Data provenance: BAS acquisition; EA processing and QC; associated documentation includes BASS survey report and EA QC report.
- Supporting project reference: Tellus South West (web presence: tellusgb.ac.uk).