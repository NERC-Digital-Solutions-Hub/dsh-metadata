# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- BAS acquired a high-resolution LiDAR dataset over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Data converted to digital terrain model (DTM) and digital surface model (DSM) by the Environment Agency under contract.
- Dataset covers 9,424 km² west of Exmouth (roughly west of 3°21'W); coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Two height layers (terrain and surface) at ~1 m grid resolution; vertical accuracy ~25 cm.
- Output available as individual ESRI grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).

## Data structure and attributes
- DTM: bare-earth terrain model; DSM: height of surface features (buildings, vegetation) on the bare earth.
- Elevation attribute with units in metres.
- Spatial tiles provided as ESRI grid format to cover the study area.

## Spatial extent
- Area: 9,424 km², west of Exmouth (approx. 3°21'W).
- Coverage organized into OS tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).

## Experimental design and sampling
- 26 LiDAR survey flights collected 14,817 line kilometres of data.
- Designed for ~300 m swath overlap between data swaths.
- Data density ~1 point per m² with the stated vertical accuracy targeting 25 cm.

## Collection methods and instrumentation
- System: Optech ALTM 3100 EA scanning laser.
- Positioning: integrated Applanix GPS/INS.
- Platform: BAS Twin Otter aircraft (VP-FBL) with instrument mounted in the camera bay.
- Output: calibrated LAS point cloud, delivered as individual flight lines.

## Calibration, processing, and quality control
- Calibration inputs: raw range files; post-processed SBET files; SMRSMG accuracy files; calibration files; flight logs; ground truth data.
- Processing: Environment Agency Geomatics used Terrascan to produce DSM and DTM from the calibrated point cloud.
- Quality control: DSM and DTM validated against existing LiDAR and GPS ground truth data; QA documented in EA QC report.

## Outputs and documentation
- Products: DSM and DTM layers suitable for environmental monitoring and spatial analysis.
- Supporting documentation: BASS survey report; EA QC report.
- Access and storage: data delivered as ESRI grid tiles; intended for storage and upload to appropriate project portals; QA and calibration metadata accompany outputs.

## Relevance for environmental monitoring and policy performance
- Provides a high-resolution, standardized, and QA-documented LiDAR dataset suitable for longitudinal environmental health assessments and mapping.
- Facilitates data integration with other datasets and reuse by other stakeholders due to standardized formats and documented processing.
- Addresses common monitoring challenges by enabling data value enhancement through reuse and broader data accessibility.