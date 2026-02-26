# Digital elevation models and bathymetry data of Tsho Rolpa glacier lake, Nepal, 2019: supporting document

- Overview
  - 3D DEMs (DSM for surface) and DTM (lakebed) derived from UAV imagery with 10 cm resolution.
  - Bathymetry data integrated to obtain lakebed and lake surface elevations; combined dataset covers the lake and nearby surroundings (~7.064 km²).

- Collection methods
  - 448 images captured from a fixed-wing UAV to generate topographic maps of Tsho Rolpa lake and surrounding area.
  - Georeferencing to a common frame (WGS84/UTM Zone 45N) using seven ground control points (GCPs) surveyed with GNSS rapid static method.
  - Boat-mounted ultrasonic sonar used to measure lake bed elevations for depth and volume estimation.

- Fieldwork and instrumentation
  - Field dates: May 7–21, 2019.
  - UAV: SenseFly eBee with Sony Cybershot DSC-WX220 camera (4896 × 3672 px, 7.76 mm sensor, 4.572 mm focal length).
  - Ground control: Trimble dGPS for GCPs.
  - Bathymetry: HydroLite-TM single-frequency echo sounder with Trimble dGPS.
  - Software: eMotion (flight planning/control), Agisoft Photoscan (SfM for DSM), ArcGIS (post-processing).

- Quality control and accuracy
  - 3D relative accuracy after GNSS-based processing: ~0.005 m.
  - RMSE (X, Y, Z) from SfM processing: 0.025 m (X), 0.082 m (Y), 0.067 m (Z).
  - Self-calibrating bundle adjustment incorporating seven GCPs to constrain the model.

- Data structure and contents
  - Two folders:
    - Lake_DSM_processed_withGCP: contains 14 main TIFF files (e.g., DSM_IDW_Lake_bed_mosaic, DSM_IDW_mosaic_fill_, TshoRolpa_lake_dam1_transparent_mosaic_group1) and associated auxiliary files.
    - BathymetryData: contains 10 shapefiles and associated files, plus raw Bathymetry_TSHO_ROLPA_16MAY.csv.
  - Bathymetry CSV format: PT_ID, East (UTM), North (UTM), Elev (m), No_Sats, Date and Time.
  - Coordinate reference: UTM Zone 45N, WGS84-based system for georeferencing and interoperability.