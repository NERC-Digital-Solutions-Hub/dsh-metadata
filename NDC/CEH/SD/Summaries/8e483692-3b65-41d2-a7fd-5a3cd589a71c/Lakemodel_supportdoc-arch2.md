# Digital elevation models and bathymetry data of Tsho Rolpa glacier lake, Nepal, 2019: supporting document

- Purpose and outputs
  - Provides high-resolution 3D representations of Tsho Rolpa glacier lake by combining UAV-derived DSM (surface) with bathymetry-based DTM (lakebed) to obtain lakebed and surface elevations.
  - DSM and DTM have a 10 cm spatial resolution; outputs enable analysis of lake topography and depth.

- Data and outputs
  - Two data folders:
    - Lake_DSM_processed_withGCP: 14 files (e.g., DSM_IDW_Lake_bed_mosaic, DSM_IDW_mosaic_fill_, TshoRolpa_lake_dam1_transparent_mosaic_group1); primarily TIFFs plus associated auxiliary files.
    - BathymetryData: 10 shapefiles (e.g., Bathmetry_16may.shp and related files) and a raw CSV Bathymetry_TSHO_ROLPA_16MAY.csv.
  - CSV header fields: PT_ID, East (UTM easting), North (UTM northing), Elev (elevation in metres), No_Sats (satellites), Date and Time.
  - UTM zone: 45N (Northern hemisphere).

- Collection methods
  - UAV imagery: 448 images captured from a fixed-wing UAV over ~7.064 km² surrounding the lake to produce topographic maps.
  - Georeferencing: 7 ground control points (GCPs) surveyed with GNSS rapid static mode to align outputs to WGS84/UTM 45N.
  - Bathymetry: boat-mounted ultrasonic altimetry (HydroLite-TM) to measure lake bed depth.

- Fieldwork and instrumentation
  - Fieldwork dates: May 7–21, 2019.
  - Equipment:
    - UAV: SenseFly eBee with Sony Cybershot DSC-WX220 camera.
    - Ground survey: Trimble dGPS for GCPs.
    - Bathymetry: HydroLite-TM single-frequency echo sounder with Trimble dGPS.
  - Software:
    - Flight planning/control: eMotion.
    - 3D reconstruction: Agisoft Photoscan (Structure-from-Motion).
    - Post-processing: ArcGIS.

- Processing and quality control
  - Data processing: SfM photogrammetry to generate DSMs; integration with bathymetric data to derive complete lake topography.
  - Accuracy metrics:
    - Relative 3D accuracy: ~0.005 m (after GNSS-based base corrections).
    - RMSE (X, Y, Z): 0.025 m, 0.082 m, 0.067 m, respectively.
  - Validation: seven GCPs used in self-calibrating bundle adjustment to enhance spatial accuracy.

- Data structure and access
  - Clear separation of outputs into DSM (surface) and Bathymetry (lakebed) datasets, with metadata and associated files to support GIS workflows.
  - All data references specify WGS84/UTM 45N coordinates and May 2019 observations, facilitating integration into time-series environmental monitoring efforts.