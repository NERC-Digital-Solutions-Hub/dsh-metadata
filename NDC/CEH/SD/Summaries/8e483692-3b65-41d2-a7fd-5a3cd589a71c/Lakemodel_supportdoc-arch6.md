# Digital elevation models and bathymetry data of Tsho Rolpa glacier lake, Nepal, 2019: supporting document

## Overview of the data
- 3D DEMs (DSM for surface and DTM for lake bed) generated from UAV imagery with 10 cm spatial resolution.
- Bathymetry data integrated so both lakebed and surface elevations are represented.
- UAV survey covers Tsho Rolpa lake and surrounding area (~7.064 km2) using 448 images.
- Georeferencing to a common frame (WGS84/UTM Zone 45N) achieved with seven ground control points (GCPs) surveyed via GNSS rapid static method.
- Boat-mounted ultrasonic bathymetry data collected to measure lake bed topography, enabling depth and volume calculations.

## Collection methods
- Fixed-wing UAV (SenseFly eBee) used with a Sony Cybershot DSC-WX220 camera to capture high-resolution images (4896 x 3672 px).
- Georeferencing ensured via seven GNSS-based GCPs with eight-minute observations per point.
- Bathymetry obtained using a boat-mounted ultrasonic altimeter (HydroLite-TM) linked to a GNSS receiver.
- Study area and flight planning supported by software including eMotion (flight control), Agrisoft Photoscan (SfM for DSM), and ArcGIS for post-processing.

## Fieldwork and instrumentation
- Fieldwork conducted May 7–21, 2019.
- Instruments: eBee SenseFly UAV, Sony DSC-WX220 camera; Trimble dGPS for ground control and topography; HydroLite-TM sonar for bathymetry.
- Software: eMotion for flight planning and control; Agisoft Photoscan for SfM processing; ArcGIS for data handling and analysis.
- Camera specifications and sensor details documented for reproducibility.

## Quality control
- 3D relative accuracy of 0.005 m achieved after post-processing with GNSS base observations near the outlet channel.
- RMSEs: X = 0.025 m, Y = 0.082 m, Z = 0.067 m calculated from SfM bundle adjustment incorporating all seven GCPs.

## Details of data structure
- Dataset organized into two folders: Lake_DSM_processed_withGCP and BathymetryData.
- Lake_DSM_processed_withGCP contains 14 main files (e.g., DSM_IDW_Lake_bed_mosaic, DSM_IDW_mosaic_fill_, TshoRolpa_lake_dam1_transparent_mosaic_group1); primary formats are TIFF (.tif) with supporting auxiliary files.
- BathymetryData folder contains 10 shapefiles (e.g., Bathmetry_16may.shp and linked files) and raw data Bathymetry_TSHO_ROLPA_16MAY.csv.
- CSV support data: PT_ID, East (UTM easting), North (UTM northing), Elev (elevation in metres), No_Sats (satellites), Date and Time.
- Coordinate reference: Universal Transverse Mercator, Zone 45N, Northern Hemisphere.