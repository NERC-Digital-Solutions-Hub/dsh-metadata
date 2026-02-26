# Co-aligned Hyperspectral and LiDAR UAV data collected in drought stressed European beech forest, Rhon Biosphere Reserve, Germany, 2020

## Overview
- A co-aligned dataset of hyperspectral and LiDAR UAV imagery collected in September 2020 across four sites within core protected areas of the UNESCO Rhön Biosphere Reserve, Germany.
- Targets European beech (Fagus sylvatica); headwall Hyperspec Nano sensor used for all imagery.

## Methods (Data collection)
- Sites: 1a, 1b, 1c (Sept 9, 2020) and Site 2 (Sept 10, 2020).
- Acquisition times and sky conditions recorded; sensor/UAV configuration detailed per site:
  - Site 1a: 17:35–18:12, cloudy; height 90 m; velocity 6.52 m/s; GSD 3.9 cm/px; overlap 40% (L), 1% (F); camera angle -90°.
  - Site 1b: 10:15–11:05, clear; height 90 m; velocity 7.83 m/s; GSD 3.9 cm/px; overlaps same as above; angle -90°.
  - Site 1c: 12:46–13:30, clear, strong winds; height 80 m; velocity 8.7 m/s; GSD 3.5 cm/px; overlaps same; angle -90°.
  - Site 2: 11:05–12:35, changeable sky; height 90 m; velocity 6.2 m/s; GSD 3.9 cm/px; overlaps same; angle -90°.
- Sensor and platform: headwall Hyperspec Nano hyperspectral sensor; LiDAR integrated in the Headwall system (Velodyne puck).
- Processing background: hyperspectral lines orthorectified using PPK GPS/IMU data and LiDAR-derived DEM at 10 cm; lines converted to surface reflectance via empirical line method.
- Noted issues: data gaps in dark canopy areas due to low signal; occasional cloud-induced darkening in a small number of lines; irradiance not monitored during flight.

## Data structure, nature and units
- Total files: 685, organized by site folders (1a, 1b, 1c, 2) with subfolders for hyperspectral flight lines.
- Data processing and format:
  - Hyperspectral lines orthorectified with PPK GPS/IMU and 10 cm LiDAR DEM.
  - Surface reflectance values (0–1) stored as 32-bit floating point; 273 spectral bands spanning 399–1001 nm.
  - Data in EPSG:4326 (WGS 84) geographic coordinates.
  - Some data gaps in dark canopy regions; occasional cloud-darkened lines.
- Root site folder contents:
  - 10 cm DEMs for each site (from maximum LiDAR returns).
  - Cleaned LiDAR LAS files (random points above canopy removed).
  - Velodyne LiDAR sensor data integration details.
  - A Site-specific *_VRT virtual raster file combining flight lines into a full-area mosaic per site.
- File naming and access:
  - Hyperspectral files: raw_[number]_rd_rf_or and raw_[number]_rd_rf_or.hdr (numbers 0–140,000; not all numbers used).
  - ENVI header files (.hdr) readable in ENVI or via R package hsdar (read_header).
  - LiDAR data: 20200909_site1a_lidar_cleaned.las, 20200909_lidar_cleaned_site1b1.las, etc.
  - DEM files: Site1a_lidar_dem.tif, Site1b_east_dem.tif, Site2.1_dem.tif, etc.
  - VRTs: Site1a_VRT.vrt, Site1b_VRT.vrt, Site1c_VRT.vrt, Site_2_VRT.vrt.
- Quality control:
  - QA conducted by NERC FSF prior to creation of mosaicked images, following pre-processing steps described in Section 2.

## Data quality and limitations
- Documented data gaps in dark canopy areas where the signal was poor.
- Some lines exhibit cloud-related darkening due to lack of irradiance monitoring during flight.
- Overall data are suitable for multisensor analyses (hyperspectral plus LiDAR) but users should account for canopy-related gaps and occasional atmospheric/lighting artifacts.

## Metadata, standards and interoperability
- Metadata implicit in file naming, flight parameters, processing steps, and sensor details (sensor type, flight height, speed, overlap, camera angle).
- Coordinate system and units clearly defined (EPSG:4326; 0–1 reflectance scale; 273 bands; 399–1001 nm range).
- ENVI-compatible headers and hsdar-supported access facilitate interoperability with common hyperspectral analysis workflows.

## Governance, access and stewardship implications
- Dataset is substantial in size and complexity (685 hyperspectral files plus LiDAR and DEMs); plan needed for storage, transfer, and cataloging.
- Provenance is well-documented: target species, study area, sensor, flight configuration, processing steps (orthorectification, empirical line reflectance), and QA status.
- For long-term stewardship: consider adding persistent identifiers, licensing details, and a machine-readable metadata schema (e.g., ISO 19115 or equivalent) to support discovery, reuse, and proper attribution.
- Ensure clear update/versioning policy if reprocessing or re-releasing mosaics occurs, and maintain traceability to acquisition dates and processing parameters.

## Practical takeaways for data stewards
- Maintain and publish comprehensive metadata including acquisition dates, times, sky conditions, wind (where available), sensor configuration, flight heights, GSD, overlap, and camera angle.
- Preserve and document the processing workflow (orthorectification method, DEM source and resolution, reflectance transformation method) and data quality notes (gaps, cloud effects).
- Ensure all related files (DEM, LAS, hyperspectral bands, ENVI headers, VRTs) are linked and discoverable together to support end-to-end reuse.
- Plan for data transfer and access strategies given the dataset size, and provide guidance for users on software compatibility (e.g., ENVI, R with hsdar).