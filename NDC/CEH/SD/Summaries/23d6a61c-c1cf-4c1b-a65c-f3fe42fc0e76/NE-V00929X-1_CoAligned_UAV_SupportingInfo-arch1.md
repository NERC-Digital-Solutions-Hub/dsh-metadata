# Co-aligned Hyperspectral and LiDAR UAV data collected in drought stressed European beech forest, Rhon Biosphere Reserve, Germany, 2020

## Overview
- Co-aligned hyperspectral and LiDAR UAV data from four sites within core protected areas of the UNESCO Rhön Biosphere Reserve, dominated by European beech (Fagus sylvatica).
- Collected in September 2020 using the headwall Hyperspec Nano sensor; data include hyperspectral imagery and LiDAR-derived products.
- Dataset comprises 685 files, including hyperspectral flight lines, LiDAR point clouds (cleaned), DEMs, and a combined hyperspectral mosaic (VRT).
- Hyperspectral data: 273 spectral bands, 399–1001 nm, 32-bit floating point, 5 cm pixel size, surface reflectance (empirical line method), 0–1 reflectance scale.
- LiDAR data: Velodyne puck, DEMs at ~10 cm resolution, and cleaned LAS files.
- Data are orthorectified with PPK GPS/IMU data; coordinates are in EPSG: 4326 (WGS84).

## Acquisition details by site
- Site 1a (09 Sept 2020, 17:35–18:12): cloudy with intensity changes; height 90 m; velocity 6.52 m/s; GSD 3.9 cm; front overlap 40%, side overlap 1%; camera angle -90°.
- Site 1b (09 Sept 2020, 10:15–11:05): clear sky; height 90 m; velocity 7.83 m/s; GSD 3.9 cm; overlap 40%/1%; camera angle -90°.
- Site 1c (09 Sept 2020, 12:46–13:30): clear sky, strong winds; height 80 m (GSD 3.5 cm); velocity 8.7 m/s; overlap 40%/1%; camera angle -90°.
- Site 2 (10 Sept 2020, 11:05–12:35): changeable sky (clouds/sun); height 90 m; velocity 6.2 m/s; GSD 3.9 cm; overlap 40%/1%; camera angle -90°.
- Note: wind information available for some flights; irradiation not monitored in-flight for some lines; some lines exhibit cloud darkening.

## Data structure, content, and units
- 685 files organized by Site folders (1a, 1b, 1c, 2) with subfolders for hyperspectral flight lines.
- Hyperspectral data lines:
  - Orthorectified using PPK GPS/IMU with LiDAR-derived 10 cm DEM.
  - Surface reflectance, converted with empirical line method.
  - Data gaps in dark canopy areas due to weak signal.
  - Cloud darkening present in a small number of lines due to lack of irradiance monitoring.
  - 32-bit floating point, 0–1 scale, 273 bands, 399–1001 nm, ~5 cm pixel size.
  - Coordinates in EPSG:4326 (WGS84).
- Root folders include:
  - 10 cm DEMs per site (from maximum LiDAR return).
  - Cleaned LAS LiDAR files.
  - LiDAR sensor: Velodyne puck.
  - *_VRT virtual raster files compiling flight lines into full-site mosaics.
- Hyperspectral data file naming:
  - raw_[number]_rd_rf_or or raw_[number]_rd_rf_or.hdr
  - [number] ranges 0–140,000; not all numbers are used.
- ENVI header files accessible via ENVI or R package hsdar (read_header).
- LiDAR and DEM file naming examples:
  - 20200909_site1a_lidar_cleaned.las, Site1a_lidar_dem.tif, Site1a_VRT.vrt, etc.
- Quality control: QA performed by NERC FSF prior to mosaicked image creation; preprocessing steps detailed in Section 2.

## Processing, QA, and metadata
- Data orthorectified with PPK GPS/IMU data using LiDAR DEM at 10 cm resolution.
- Hyperspectral data converted to surface reflectance via empirical line method.
- QA checks conducted by NERC FSF before mosaic generation.
- Pre-processing details referenced to Section 2 (not reiterated here).

## Access and usage notes
- Data are provided with suitable metadata and ENVI headers; use ENVI or R (hsdar) to read headers and spectral data.
- VRT files allow full-site mosaics for integrated analysis.
- 0–1 reflectance scale and 32-bit precision support quantitative analyses and modeling.
- Spatial alignment with LiDAR-derived DEM enables integration of spectral and structural metrics.

## Limitations and considerations for analysts
- Data gaps in dark canopy areas due to weak signal.
- Cloud darkening observed in some lines; irradiation not monitored during flight for all lines, affecting radiometric consistency.
- Some flight lines lack wind information; conditions varied across sites.
- Not all potential flight-number entries (0–140,000) are populated; data selection may be required.
- Comparisons across sites should account for variable sky conditions, wind, and atmospheric effects.

## Potential analyses and applications
- Integrate hyperspectral reflectance with LiDAR-derived canopy structure (e.g., height, density) to assess drought stress signatures in beech forests.
- Develop predictive models relating spectral indices and structural metrics to drought indicators or stress levels.
- Conduct fine-scale mapping of drought stress patterns across the Rhön Beech forest using the high-resolution dataset.
- Use the VRT mosaics to perform landscape-scale analyses and cross-site comparisons with consistent geospatial framing.