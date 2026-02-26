# Digital elevation models and bathymetry data of Tsho Rolpa glacier lake, Nepal, 2019: supporting document

- Overview of the data
  - 3D DEMs (DTM and DSM) generated from UAV imagery at 10 cm resolution; integrated with bathymetry to obtain lakebed and surface elevations.
  - Visualization notes: lake with bathymetric observations overlaid on UAV-derived DSM and orthomosaic.

- Collection methods
  - 448 images captured with a fixed-wing UAV over Tsho Rolpa lake and surrounding area (~7.064 km²).
  - Georeferencing to WGS84/UTM Zone 45N using 7 ground control points (GCPs) surveyed with GNSS rapid static method (8 minutes per point).
  - Boat-mounted ultrasonic bathymetry data collected to measure lake bed depth.

- Fieldwork and instrumentation
  - Fieldwork: May 7–21, 2019.
  - UAV: SenseFly eBee with Sony Cybershot DSC-WX220 camera (4896 × 3672 px, 6.17 × 4.63 mm chip).
  - Ground control: Trimble dGPS; bathymetry: HydroLite-TM echo sounder with Trimble dGPS.
  - Software: eMotion for flight planning/control; Agisoft Photoscan for Structure-from-Motion (SfM) processing; ArcGIS for post-processing.

- Quality control
  - 3D relative accuracy ~0.005 m achieved post-processing with GNSS base station corrections.
  - RMSEs: X = 0.025 m, Y = 0.082 m, Z = 0.067 m (SfM-based outputs).
  - Seven GCPs used in self-calibrating bundle adjustment within Photoscan.

- Details of data structure
  - Two folders: Lake_DSM_processed_withGCP and BathymetryData.
  - Lake_DSM_processed_withGCP: 14 TIFF-based files (e.g., DSM_IDW_Lake_bed_mosaic, DSM_IDW_mosaic_fill_, TshoRolpa_lake_dam1_transparent_mosaic_group1) with associated ancillary files.
  - BathymetryData: 10 shapefiles (e.g., Bathmetry_16may.shp) and a raw data CSV (Bathymetry_TSHO_ROLPA_16MAY.csv) with fields: PT_ID, East, North, Elev, No_Sats, Date, Time.
  - Coordinate reference: UTM Zone 45N, northern hemisphere.

- Relevance for monitoring frameworks
  - Provides high-resolution, georeferenced surface and bed elevations suitable for lake volume, bathymetric change, and topographic monitoring.
  - Clear end-to-end workflow from data collection to SfM processing and quality metrics, enabling reproducibility and cross-study comparisons.
  - Metadata elements included (sensor details, flight/process steps, coordinate system) to support transparency and data governance.

- Data governance considerations
  - Data formats (TIFF rasters, shapefiles, CSV) support interoperability and integration into monitoring dashboards and analyses.
  - Documentation of georeferencing (GCPs, GNSS methods) and processing (SfM, IDW interpolation) facilitates auditability.
  - While open-access status isn’t stated, the detailed structure and metadata enhance potential for sharing within monitoring frameworks and collaborative projects.