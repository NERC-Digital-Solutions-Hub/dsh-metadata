# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Overview
- BAS collected a new high-resolution LiDAR dataset over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Products produced: Digital Terrain Model (DTM) representing bare-earth terrain and Digital Surface Model (DSM) representing surface features (buildings, vegetation).
- Data characteristics: two 2 cm height layers for terrain and surface height, 1 m grid cell resolution, average vertical accuracy of 25 cm.
- Coverage: area of 9,424 km² west of Exmouth (west of ~3°21′W).
- Access format: data provided as individual ESRI grid files corresponding to Ordnance Survey tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
- Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Data attributes: Elevation, described as Height; units are metres.

## Data specification and products
- Spatial resolution and layers: 1 m grid with 2 cm height layers for terrain and surface heights.
- Coverage extent: 9,424 km² in the west Cornwall and Devon region.
- Data attributes: Height (elevation) in metres; clear separation of bare-earth and surface features via DTM and DSM.

## Collection, processing, and quality control
- Field campaign: 26 LiDAR survey flights totaling 14,817 line km; designed for about 300 m swath overlap to meet accuracy/specifications.
- Platform and instrument: Optech ALTM 3100 EA scanner with integrated GPS/INS, mounted in a BAS Twin Otter aircraft (VP-FBL).
- Processing workflow: Environment Agency Geomatics used Terrascan software to derive DSM and DTM from calibrated LAS point cloud data.
- Calibration and supporting data: Raw range files, SBET post-processed files, SMRSMG accuracy files, calibration files, flight logs, and ground truth survey details; LAS data delivered as individual flight lines for quality checks.
- Quality control: DSM/DTM validated against existing LiDAR data and GPS ground truth; EA QC report documents accuracy and limitations.

## Data management and discoverability
- Data format and organization: Products are delivered as ESRI grid format tiles corresponding to OS tiles, facilitating discoverability and integration with existing GIS workflows.
- Access and references: Overview and project context available at http://www.tellusgb.ac.uk/.
- Supporting documentation: BASS survey report and EA QC report referenced for quality assessment and methodology.

## Implications for Data Leaders
- Demonstrates end-to-end data lifecycle management for high-resolution LiDAR data, including acquisition, calibration, processing, QA, and documentation.
- Highlights importance of cross-organisation collaboration (research, environments agencies) to deliver trustworthy data assets with clear metadata (coordinate system, resolution, units, coverage).
- Illustrates practical data product differentiation (DTM vs DSM) and the need for explicit data formats and tile-based organization to support discoverability and reuse.
- Provides a model for verifying data quality through ground truth comparisons and standardized QC reporting to support confidence in data-driven decision-making.