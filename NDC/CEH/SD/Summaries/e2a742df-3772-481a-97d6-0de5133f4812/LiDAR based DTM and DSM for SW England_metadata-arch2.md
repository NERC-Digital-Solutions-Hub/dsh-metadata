# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- High-resolution LiDAR dataset over Cornwall and Devon acquired in July–August 2013 for the Tellus South West project.
- Aims to provide standardized, QA’d environmental data products (DTM and DSM) for monitoring environmental health and policy performance over time.

## Dataset Characteristics
- Data quality: high resolution (~1 point per meter) with vertical accuracy around 25 cm.
- Data layers: Digital Terrain Model (DTM) representing bare earth; Digital Surface Model (DSM) including features on the bare earth (e.g., buildings, vegetation); both provided as height layers.
- Resolution and extent: 1 m grid cells over 9424 km² (west of Exmouth, approximately west of 3°21' W).
- Output attributes: Elevation (height in metres).

## Spatial Reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700).

## Data Products and Formats
- Data produced as 2 cm height layers for terrain and surface, delivered 1 m gridded.
- Available as individual ESRI grid tiles corresponding to OS reference tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).

## Data Collection and Experimental Design
- Coverage: 9424 km² area with LiDAR data collected over Cornwall and Devon.
- Flights: 26 survey flights, totaling 14,817 line km of LiDAR data.
- Overlap: designed to achieve ~300 m overlap between data swaths.
- Data density: approximately 1 point per m² (with stated ~1 point/meter in the summary).

## Collection Methods and Instrumentation
- Instrument: Optech ALTM 3100 EA scanning laser with integrated Applanix GPS/INS.
- Platform: BAS Twin Otter aircraft (VP-FBL) with calibration and flight navigation data.
- Data acquisition supported by contracted processing.

## Calibration, Processing, and Analytical Methods
- Processing: Environment Agency Geomatics used Terrascan software to convert calibrated point clouds into DSM and DTM layers.
- Calibration inputs: Raw range files, SBET post-processed files, SMRSMG accuracy files, calibration files, flight logs, and ground truth details.
- Output: Calibrated LAS point cloud data delivered as individual flight lines.
- Purpose: Ensure high-quality terrain and surface height models suitable for standardized environmental analyses.

## Quality Control
- Validation: DSM and DTM compared against existing LiDAR data and GPS ground truth.
- QA documentation: EA QC report assessing accuracy and limitations of the products.

## Data Access and Utilisation
- Data is provided as ESRI grid tiles and is designed to be stored, managed, and uploaded to appropriate data portals.
- Enables integration with other environmental datasets to enhance value beyond single-use applications.

## References / Supporting Documentation
- BASS survey report
- EA QC report

## Relevance for Environmental Monitoring Analysts
- Provides standardized, high-accuracy terrain and surface models for broad regional monitoring.
- Supports QA-driven data products with documented processing chains and ground-truth validation.
- Facilitates data integration and re-use by delivering widely compatible formats and clear metadata.