# Digital elevation models and bathymetry data of Tsho Rolpa glacier lake, Nepal, 2019: supporting document

## Overview
- 3D DEMs (DSM) and a bathymetry dataset are combined to produce lake surface elevations and lakebed elevations (DTM/DSM) with a 10 cm spatial resolution.
- Demonstrates integration of UAV-derived topography with bathymetric measurements to enable depth and volume calculations.

## Data collection and methods
- 448 UAV images captured from a fixed-wing SenseFly eBee over the lake and surrounding area (~7.064 km²).
- Georeferencing: 7 ground control points (GCPs) surveyed with GNSS rapid static mode; eight-minute observations per point; reference frame WGS84/UTM Zone 45N.
- Bathymetry: boat-mounted ultrasonic altimetry used to measure lake bed topography for depth/volume estimation.
- Sensor and camera: Sony Cybershot DSC-WX220 (4896 × 3672 px), mounted on eBee with 4.572 mm nominal focal length.
- Software and processing: eMotion for flight planning/control; Agisoft Photoscan (SfM) for DSM reconstruction; ArcGIS for post-processing.

## Fieldwork timeline
- May 7–21, 2019.

## Quality control and accuracy
- 3D relative accuracy after GNSS processing: 0.005 m.
- RMSE (X, Y, Z): 0.025 m, 0.082 m, 0.067 m respectively.
- Seven GCPs incorporated in self-calibrating bundle adjustment to constrain georeferencing.

## Data structure and formats
- Two folders:
  - Lake_DSM_processed_withGCP: 14 files (DSM_IDW_Lake_bed_mosaic, DSM_IDW_mosaic_fill_, TshoRolpa_lake_dam1_transparent_mosaic_group1); main files are TIFFs.
  - BathymetryData: 10 shapefiles (including Bathmetry_16may.shp and associated files) and raw data Bathymetry_TSHO_ROLPA_16MAY.csv.
- CSV format: PT_ID, East (UTM easting), North (UTM northing), Elev (elevation in metres), No_Sats (satellites), Date and Time.
- Projection: UTM Zone 45N (N hemisphere); WGS84.

## Visualization and context
- Figure 1 (referenced) shows bathymetric observations overlaid on the UAV-derived DSM.

## Potential uses and implications
- Enables integrated analyses of lake depth and volume for geomorphology, hydrology, and climate-related studies.
- Provides georeferenced, high-resolution topographic and bathymetric data suitable for collaboration and reuse across researchers and partners.