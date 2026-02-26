# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- High-resolution LiDAR dataset over Cornwall and Devon collected in July–August 2013 for the Tellus South West project.
- Produces Digital Terrain Model (DTM, bare earth) and Digital Surface Model (DSM, surface features) at 1 m grid resolution with approximately 25 cm vertical accuracy.
- Data cover: 9,424 km² west of Exmouth; provided as ESRI grid tiles representing OS grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).

## Data contents and attributes
- Layers: DTM (bare-earth terrain) and DSM (bare-earth plus features like buildings/vegetation).
- Primary attribute: Elevation; Description = Height; Units = metres.
- The dataset comprises 2 cm height layers representing terrain and surface height, with 1 m grid cells and ~25 cm height accuracy.

## Data collection and processing
- Survey design: 26 LiDAR flights, totaling 14,817 line km over 9,424 km² with ~300 m swath overlap; targeted to meet 25 cm vertical accuracy and 1 point/m² density.
- Instrumentation: Optech ALTM 3100 EA scanning laser; integrated GPS/INS; mounted in BAS Twin Otter aircraft.
- Processing pipeline: Environment Agency Geomatics used Terrascan to convert calibrated LAS point clouds into DSM and DTM layers.
- Calibration and supporting data: Raw range files, SBET post-processed data, SMRSMG accuracy files, calibration files, flight logs, and any ground truth survey details; calibrated LAS delivered as individual flight lines.

## Quality assurance and provenance
- Quality control: DSM and DTM validated against existing LIDAR and GPS ground-truth data; detailed accuracy and limitations summarized in the EA QC report.
- Provenance: Data collected by BAS for the Tellus SW project; conversion and QA performed by the Environment Agency.

## Access, metadata, and limitations
- Access format: Data available as individual ESRI grid tiles; coverage area and projection specified above.
- Metadata scope: Includes coordinate system, data attributes, calibration details, flight logs, and ground truth information.
- Limitations and considerations: Accuracy and limitations documented in the EA QC report; some data transformation may be required for use in different GIS environments.