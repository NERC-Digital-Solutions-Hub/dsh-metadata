# Digital elevation models and bathymetry data of Tsho Rolpa glacier lake, Nepal, 2019: supporting document

## Overview
- 3D DEMs of Tsho Rolpa glacier lake generated from UAV imagery at 10 cm spatial resolution.
- Data combined with bathymetry to obtain both lakebed elevation (DTM) and lake surface elevation (DSM).
- Lake extent ~7.064 km²; bathymetric observations overlayed on UAV-derived DSM (Figure 1).
- Outputs provided as DSMs and bathymetric data to support depth and volume analysis.

## Collection methods
- 448 images captured from a fixed-wing UAV (SenseFly eBee) to cover the lake and surrounding area.
- Imaging details: Sony Cybershot DSC-WX220 camera, 4896 × 3672 px resolution, nominal focal length 4.572 mm.
- Georeferencing tied to WGS84/UTM Zone 45N using seven Ground Control Points (GCPs) surveyed with GNSS rapid static mode (8 minutes per point).

## Fieldwork and instrumentation
- Fieldwork dates: May 7–21, 2019.
- Equipment:
  - UAV: eBee SenseFly; flight planning with eMotion.
  - SfM processing: Agisoft Photoscan (Structure-from-Motion) to reconstruct DSM; ArcGIS for post-processing.
  - Bathymetry: boat-mounted HydroLite-TM single-frequency echo sounder with Trimble dGPS.
- Bathymetric data integrated to derive lake depth/volume.

## Quality control
- Relative 3D accuracy after GNSS-based adjustment: 0.005 m.
- RMSE from SfM: X = 0.025 m, Y = 0.082 m, Z = 0.067 m.
- Seven GCPs used in self-calibrating bundle adjustment to constrain the model.

## Details of data structure
- Two folders and file sets:
  - Lake_DSM_processed_withGCP: 14 files (DSM_IDW_Lake_bed_mosaic, DSM_IDW_mosaic_fill_, TshoRolpa_lake_dam1_transparent_mosaic_group1; mostly .tif and associated files).
  - BathymetryData: 10 shapefiles (e.g., Bathmetry_16may.shp and associated files) plus raw data Bathymetry_TSHO_ROLPA_16MAY.csv.
- CSV content in Bathymetry_TSHO_ROLPA_16MAY.csv includes: PT_ID, East (UTM easting), North (UTM northing), Elev (elevation in metres), No_Sats, Date and Time.
- Coordinate reference: UTM Zone 45N, Northern Hemisphere.