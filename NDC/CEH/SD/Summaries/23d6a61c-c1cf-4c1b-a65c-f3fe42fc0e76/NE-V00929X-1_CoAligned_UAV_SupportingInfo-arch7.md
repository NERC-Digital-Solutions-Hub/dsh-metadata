# Co-aligned Hyperspectral and LiDAR UAV data collected in drought stressed European beech forest, Rhon Biosphere Reserve, Germany, 2020

## Methods
- Data collected from four sites within core protected areas of the UNESCO Rhön Biosphere Reserve, dominated by European beech (Fagus sylvatica), in September 2020 using the Headwall Hyperspec Nano sensor for hyperspectral data and a Velodyne LiDAR puck for LiDAR data.
- Flight and sensor details:
  - Site 1a: 09 Sep 2020, 17:35–18:12, cloudy with varying intensity; height above ground level ~90 m; velocity 6.52 m/s; GSD 3.9 cm/px; lateral overlap 40%; flight overlap 1%; camera angle -90°.
  - Site 1b: 09 Sep 2020, 10:15–11:05, clear sky, light wind; height ~90 m; velocity 7.83 m/s; GSD 3.9 cm/px; overlaps as above.
  - Site 1c: 09 Sep 2020, 12:46–13:30, clear sky, strong winds; height ~80 m; velocity 8.7 m/s; GSD 3.5 cm/px; overlaps as above.
  - Site 2: 10 Sep 2020, 11:05–12:35, changeable sky; height ~90 m; velocity 6.2 m/s; GSD 3.9 cm/px; overlaps as above.
- Data processing:
  - Hyperspectral lines orthorectified using PPK GPS/IMU data and LiDAR-derived DEM at 10 cm resolution.
  - Lines converted to surface reflectance via empirical line method.
  - Noted data gaps in dark canopy regions and occasional cloud darkening due to irradiance monitoring not active during flight.
- Data characteristics:
  - Hyperspectral data: 32-bit floating point, 0–1 scale, 273 spectral bands, 399–1001 nm, ~5 cm pixel size, EPSG:4326 (WGS 84).
  - Data organized for each site with dedicated flight line subfolders.
  - All data align with a common coordinate system and are suitable for GIS-based analysis and mapping.

## Data Structure, Nature and Units of recorded values
- Dataset contains 685 files, organized by site (1a, 1b, 1c, 2) into site-specific folders with subfolders for hyperspectral flight lines.
- Processing outputs:
  - Hyperspectral lines orthorectified and delivered as surface reflectance data; 32-bit floating point; 273 bands; 399–1001 nm; ~5 cm pixels.
  - DEMs: 10 cm resolution LiDAR-derived DEMs for each site.
  - LiDAR point clouds: cleaned LAS files (random above-canopy points removed).
  - LiDAR sensor: Velodyne puck integrated into Headwall system; LAS files named to reflect date/site.
  - Virtual rasters: *_VRT files (Site1a_VRT.vrt, Site1b_VRT.vrt, Site1c_VRT.vrt, Site_2_VRT.vrt) combining flight lines into a full-site mosaic.
- File naming conventions:
  - Hyperspectral: raw_[number]_rd_rf_or and raw_[number]_rd_rf_or.hdr (numbers range 0–140,000 with gaps); ENVI headers readable via ENVI or R (hsdar package).
  - LiDAR: 20200909_site1a_lidar_cleaned.las, 20200909_lidar_cleaned_site1b1.las, etc.
  - DEMs: Site1a_lidar_dem.tif, Site1b_east_dem.tif, Site1b_west_dem.tif, Site1c.1_lidar_dem.tif, Site1c.2_lidar_dem.tif, Site2.1_dem.tif, Site2.2_dem.tif.
- Quality Control:
  - QA performed by NERC FSF prior to mosaic creation; preprocessing steps documented in Section 2.

## Notes for GIS-focused use
- The integration of hyperspectral (273 bands, 399–1001 nm) and LiDAR data enables spatially explicit analysis of canopy structure and spectral properties in drought-stressed beech forest.
- All data are georeferenced to WGS84 (EPSG:4326) for compatibility with common GIS workflows.
- Produced products (orthorectified hyperspectral lines, high-resolution DEMs, cleaned LAS, and VRT mosaics) are designed to support map-based visualization, feature extraction, and cross-dataset analyses.