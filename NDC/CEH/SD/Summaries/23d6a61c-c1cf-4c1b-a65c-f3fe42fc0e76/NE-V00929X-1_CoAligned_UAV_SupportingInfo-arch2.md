# Co-aligned Hyperspectral and LiDAR UAV data collected in drought stressed European beech forest, Rhon Biosphere Reserve, Germany, 2020

## Overview
- Co-aligned UAV hyperspectral and LiDAR datasets collected in September 2020.
- Four sites within core protected areas of the Rhön Biosphere Reserve, Germany, dominated by European beech (Fagus sylvatica).
- Objective aligned with environmental monitoring: provide standardized data to assess forest condition under drought stress.

## Data collection (Methods)
- Sensors and platform:
  - Hyperspectral sensor: headwall Hyperspec Nano.
  - LiDAR: Velodyne puck integrated with the Headwall system.
- Sites and timing:
  - Site 1a, 1b, 1c (Sept 9, 2020) and Site 2 (Sept 10, 2020).
  - Times varied across sites with notes on sky conditions and wind; camera angle fixed at -90°.
- Flight and capture details:
  - Heights above ground level: ~80–90 m.
  - Ground sampling distance (GSD): ~3.5–3.9 cm per pixel.
  - Line overlap: 40%; Flight overlap: 1%.
  - Variability in cloud cover and wind across flights; cloud darkening observed in a small subset of lines due to irradiance monitoring gaps.
- Data processing inputs:
  - Orthorectification via PPK GPS/IMU using LiDAR-derived 10 cm DEM.
  - Hyperspectral data converted to surface reflectance using the empirical line method.
  - Data recorded as 32-bit floating point, 0–1 reflectance, 273 spectral bands (399–1001 nm).

## Data structure, nature and units
- Total files: 685, organized by site folders (1a, 1b, 1c, 2).
- Within each site:
  - Subfolders contain hyperspectral flight lines (orthorectified to 10 cm DEMs).
  - Data are provided as surface reflectance imagery.
- Data gaps:
  - Dark canopy areas with poor signal.
- Coordinate system:
  - All data in EPSG: 4326 (WGS 84).
- Root site folders contents:
  - 10 cm DEMs per site (from maximum LiDAR return).
  - Cleaned LiDAR LAS files (random points above canopy removed).
  - LiDAR sensor data integrated as part of the Headwall system.
  - A _VRT virtual raster mosaic per site covering the full flight area.
- Hyperspectral data naming and formats:
  - Files named raw_[number]_rd_rf_or or raw_[number]_rd_rf_or.hdr.
  - [number] ranges from 0–140,000 (not all numbers used).
  - ENVI headers readable directly (ENVI or via R package hsdat/read_header).
- LiDAR and DEM file naming:
  - Example LiDAR: 20200909_site1a_lidar_cleaned.las, 20200909_lidar_cleaned_site1b1.las, etc.
  - DEMs: Site1a_lidar_dem.tif, Site1b_east_dem.tif, Site1b_west_dem.tif, Site1c.1_lidar_dem.tif, Site1c.2_lidar_dem.tif, Site2.1_dem.tif, Site2.2_dem.tif.
- Virtual raster:
  - Site1a_VRT.vrt, Site1b_VRT.vrt, Site1c_VRT.vrt, Site_2_VRT.vrt.

## Data processing and quality control
- Processing steps:
  - Hyperspectral lines orthorectified using PPK GPS/IMU with LiDAR-derived DEM at 10 cm resolution.
  - Surface reflectance produced via empirical line method.
- Quality assurance:
  - QA conducted by NERC FSF prior to creation of mosaiced images; pre-processing steps documented in section 2.
- Notes on data quality:
  - Some lines exhibit cloud-related darkening; irradiance monitoring during flight was not performed for all lines.