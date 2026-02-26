# Digital elevation models and bathymetry data of Tsho Rolpa glacier lake, Nepal, 2019: supporting document

- Overview of the data
  - 3D digital elevation models (DEMs) of Tsho Rolpa glacier lake generated from UAV imagery with a spatial resolution of 10 cm.
  - Combined with bathymetry data to obtain both the lakebed elevation (DTM) and the lake surface elevation (DSM).
  - Visual description: lake with bathymetric observations overlaid on UAV-derived DSM and orthomosaic.

- Collection methods
  - 448 images captured from a fixed-wing UAV (SenseFly eBee) covering the lake and surrounding area (~7.064 km²).
  - Ground control: seven GNSS ground control points (GCPs) surveyed in GNSS rapid static mode (eight-minute observations per point) to georeference outputs to WGS84/UTM Zone 45N.
  - Bathymetry: boat-mounted ultrasonic altimetry data collected to measure lake bed topography for depth and volume calculations.
  - Fieldwork dates: May 7–21, 2019.

- Field equipment and software
  - UAV: eBee SenseFly with a Sony Cybershot DSC-WX220 camera (4896 × 3672 px; 4.57 mm focal length; 1/2.3" Exmor RTM CMOS sensor).
  - Topography and positioning: Trimble dGPS; GNSS base station near the outlet channel for differential corrections.
  - Bathymetry: HydroLite-TM single-frequency echo sounder integrated with Trimble dGPS.
  - Software: eMotion for flight planning/control; Agisoft Photoscan (SfM) for reconstructing DSM; ArcGIS for post-processing.

- Quality control
  - Achieved an average 3D relative accuracy of 0.005 m after post-processing with GNSS observations from a base station.
  - RMSEs from SfM: X = 0.025 m, Y = 0.082 m, Z = 0.067 m.
  - Seven GCPs used in a self-calibrating bundle adjustment to improve spatial accuracy.

- Data structure and contents
  - Dataset consists of two folders: Lake_DSM_processed_withGCP and BathymetryData.
  - Lake_DSM_processed_withGCP: 14 files (mainly DSM-related) with names such as DSM_IDW_Lake_bed_mosaic, DSM_IDW_mosaic_fill, and TshoRolpa_lake_dam1_transparent_mosaic_group1; file formats include .tif and associated metadata files.
  - BathymetryData: 10 shapefiles (e.g., Bathmetry_16may.shp) plus associated files; raw data in Bathymetry_TSHO_ROLPA_16MAY.csv.
  - CSV fields: PT_ID (point id), East (UTM easting), North (UTM northing), Elev (elevation in metres), No_Sats (number of satellites), Date and Time.
  - Coordinate reference: UTM Zone 45N, Northern Hemisphere.

- Notes on coordinate system and scope
  - UTM (Universal Transverse Mercator) zone 45N; WGS84 reference frame.
  - The study covers the lake and surrounding immediate area, enabling lakebed (bathymetric) and surface (DSM) integration for depth and volume analysis.

- Potential applications
  - Deriving lake depth and volume by integrating DSM with bathymetric measurements.
  - Monitoring changes in lakebed/topography over time for glacial lake stability assessments.
  - Providing georeferenced, high-resolution surface and bathymetric datasets for hydrological and geomorphological analyses.