# Co-aligned Hyperspectral and LiDAR UAV data collected in drought stressed European beech forest, Rhon Biosphere Reserve, Germany, 2020

## Overview
- Dataset from four beech-dominated sites (1a, 1b, 1c, 2) in the UNESCO Rhön Biosphere Reserve, collected September 2020.
- Focus on co-aligned hyperspectral and LiDAR data using Headwall Hyperspec Nano sensor.

## Methods (Data Collection)
- Data type: Co-aligned hyperspectral and LiDAR imagery.
- Flight details:
  - Site 1a: 09 Sep 2020, 17:35–18:12, cloudy; velocity 6.52 m/s; height 90 m; GSD 3.9 cm/px; L overlap 40%; F overlap 1%; camera angle -90°.
  - Site 1b: 09 Sep 2020, 10:15–11:05, clear; velocity 7.83 m/s; height 90 m; GSD 3.9 cm/px; L 40%; F 1%; angle -90°.
  - Site 1c: 09 Sep 2020, 12:46–13:30, clear, strong winds; velocity 8.7 m/s; height 80 m; GSD 3.5 cm/px; L 40%; F 1%; angle -90°.
  - Site 2: 10 Sep 2020, 11:05–12:35, mixed sky; velocity 6.2 m/s; height 90 m; GSD 3.9 cm/px; L 40%; F 1%; angle -90°.
- Sensor configuration: Headwall Hyperspec Nano; LiDAR via Velodyne puck integrated into Headwall.
- Data products include orthorectified hyperspectral lines (PPK GPS/IMU corrected) with LiDAR-derived DEMs.

## Data Structure, Nature and Units
- Total: 685 files organized by site (1a, 1b, 1c, 2) into site-specific folders and subfolders for hyperspectral flight lines.
- Processing and formats:
  - Hyperspectral lines orthorectified using PPK GPS/IMU with 10 cm LiDAR DEM.
  - Data are surface reflectance (empirical line method) with some data gaps in dark canopy regions.
  - Occasional cloud darkening in a small number of lines; irradiance not monitored during flight.
  - Hyperspectral data: 32-bit floating point, 273 bands, 399–1001 nm, ~5 cm pixel size.
  - Coordinate system: EPSG:4326 (WGS 84).
- Root folders include:
  - 10 cm DEMs per site from maximum LiDAR return.
  - Cleaned LAS files (noise above canopy removed).
  - LiDAR sensor data (Velodyne puck) integrated with Headwall.
  - Site-specific VRT virtual rasters combining flight lines into full-area mosaics.
- Hyperspectral file naming: raw_[number]_rd_rf_or and raw_[number]_rd_rf_or.hdr (numbers 0–140,000; not all used).
- ENVI headers readable in ENVI or via R (hsdar package).

## Data Quality and QA
- Quality Assurance performed by NERC FSF prior to mosaic creation; preprocessing steps referenced in section 2.

## Cautions and Considerations
- Data gaps exist in dark canopy portions.
- Cloud darkening present in a few lines.
- Irradiance not monitored during flights, which may affect radiometric considerations in some lines.

## Potential Uses (Data Support Context)
- Combine hyperspectral and LiDAR to analyze drought responses in European beech forests.
- Support data-driven insights for forest health, canopy structure, and spectral-structural relationships.
- Enable end users to explore self-serve analyses through the provided hyperspectral lines, LiDAR data, DEMs, and VRT mosaics.