# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- High-resolution LiDAR data collection over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Produces two core map-based elevation products: Digital Terrain Model (DTM) and Digital Surface Model (DSM) at 1 m grid resolution, with ~25 cm vertical accuracy.
- Coverage: 9,424 km², west of Exmouth (approximately 3°21' W).
- Delivered as ESRI grid tiles for GIS use (e.g., SX37ne, SX37nw, SX37se, SX37sw).

## Data characteristics
- Layers: DTM (bare earth) and DSM (bare earth plus features like buildings/vegetation).
- Resolution: 1 m grid cells.
- Elevation attributes: Height in metres.
- Data reference system: OSGB 1936 / British National Grid (EPSG: 27700).

## Coverage and data formats
- Area coverage: 9,424 km² across Cornwall and Devon, west of Exmouth.
- Tile formats: ESRI grid tiles corresponding to OSGB grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).

## Acquisition and data collection
- Flights: 26 survey flights.
- Distance: 14,817 line kilometres of new LiDAR data.
- Swath overlap: ~300 m between data swaths.
- Data density: ~1 point per m².
- Vertical accuracy: ~25 cm.

## Methods and processing
- Sensor and platform: Optech ALTM 3100 EA scanning LiDAR with integrated GPS/INS, mounted on BAS Twin Otter aircraft.
- Calibration inputs: Raw range files, SBET files, SMRSMG accuracy files, calibration files, flight logs, ground truth details, and full LAS point cloud per flight line.
- Processing workflow: Environment Agency Geomatics used Terrascan to transform calibrated LAS into DSM and DTM layers.

## Quality assurance
- DSM and DTM validated against existing LiDAR and GPS ground-truth data.
- QA documentation provided in EA QC report.

## Outputs and usage
- Products: DTM (bare earth) and DSM (surface features) at 1 m resolution.
- Data attributes: Height measurements in metres.
- Suitability for GIS work: Ready-to-map elevation layers for tasks such as terrain analysis, flood modelling, infrastructure planning, landscape assessment, and policy-focused mapping.

## Access and references
- Tellus South West project overview: http://www.tellusgb.ac.uk/
- Supporting references: BASS survey report; EA QC report.