# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- High-resolution LiDAR dataset over Cornwall and Devon collected in July–August 2013 for the Tellus South West project.
- Digital Terrain Model (DTM) and Digital Surface Model (DSM) created from the raw point cloud, with matching high accuracy and detailed vertical representation.

## Dataset Details
- Data characteristics: two 2 cm height layers (terrain and surface) at 1 m grid cell resolution; average height accuracy ~25 cm.
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Attributes: Elevation with units in metres.

## Coverage and Formats
- Area: 9,424 km² west of Exmouth (roughly west of 3°21′W).
- Data outputs: DSM (surface features such as buildings/vegetation) and DTM (bare-earth terrain).
- File formats: individual files representing Ordnance Survey tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw) in ESRI grid format.

## Acquisition and Processing
- Survey design: 26 flight lines, totaling 14,817 line km of LiDAR data; intended ~300 m swath overlap; target 25 cm vertical accuracy and 1 point per m² data density.
- Collection method: Optech ALTM 3100 EA scanner with integrated Applanix GPS/INS, mounted on BAS Twin Otter aircraft.
- Processing: Environment Agency used Terrascan to transform calibrated point clouds into DSM and DTM layers.
- Calibration inputs: Raw range files, SBET, SMRSMG accuracy files, calibration files, flight logs, and ground truth details; delivered as calibrated LAS point clouds by flight line.

## Quality Assurance
- DSM/DTM validated against existing LiDAR and GPS ground-truth data; QA and limitations summarized in the EA QC report.

## Access and References
- Availability: Data provided as ESRI grid tiles; details and overview at http://www.tellusgb.ac.uk/.
- Supporting documents: BASS survey report; EA QC report.