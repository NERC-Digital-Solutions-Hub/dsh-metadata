Co-aligned Hyperspectral and LiDAR UAV data collected in drought stressed European beech forest, Rhon Biosphere Reserve, Germany, 2020

## Overview
- Dataset combining hyperspectral and LiDAR UAV data from four beech-dominated sites (1a, 1b, 1c, 2) within the UNESCO Rhön Biosphere Reserve, Germany.
- Collected in September 2020 to study drought-stressed European beech forests.
- Sensors: headwall Hyperspec Nano for hyperspectral data; Velodyne LiDAR integrated in the Headwall system.
- Data organized to support cross-site comparison and integrated analyses of canopy structure and hyperspectral reflectance.

## Data Collection Methods
- Sites: Four sites (1a, 1b, 1c, 2) within core protected areas, European beech forest.
- Dates: 9–10 September 2020; times and sky conditions recorded per site.
- Flight details per site: velocity (6.2–8.7 m/s), height above ground (80–90 m), ground sampling distance (GSD) 3.5–3.9 cm/px, 40% line overlap, 1% frame overlap, camera angle -90°.
- Conditions: cloud cover variable (clear to cloudy), wind data mostly provided except for some sites.
- Data processing intro: hyperspectral lines orthorectified using PPK GPS/IMU data; LiDAR DEM used at 10 cm resolution; lines converted to surface reflectance via empirical line method.
- Known data limitations: gaps in dark canopy areas due to weak signal; occasional cloud darkening in a small subset of lines; irradiance not monitored during flight.

## Data Structure, Content, and Units
- Total dataset: 685 files, organized into per-site folders (Site1a, Site1b, Site1c, Site2).
- Hyperspectral data:
  - 273 spectral bands, 399–1001 nm range, ~5 cm pixel size.
  - Data stored as 32-bit floating point, scaled 0–1.
  - Orthorectified lines with PPK GPS/IMU data and LiDAR-derived DEM at 10 cm resolution.
  - Surface reflectance, converted using empirical line method.
  - Notes on data quality: dark canopy data gaps; some lines affected by cloud darkening.
  - File naming: raw_[number]_rd_rf_or and raw_[number]_rd_rf_or.hdr (numbers range 0–140,000, not all used).
  - ENVI headers accessible via ENVI or R (hsdar package).
- LiDAR data:
  - Cleaned LAS files (noise/above-canopy points removed).
  - Examples: 20200909_site1a_lidar_cleaned.las, 20200910_site2_lidar_clean.las.
- DEMs:
  - 10 cm DEMs derived from maximum LiDAR returns (e.g., Site1a_lidar_dem.tif).
  - Additional site-specific DEMs listed (e.g., Site1b_east_dem.tif, Site1c.1_lidar_dem.tif).
- Virtual raster mosaics:
  - Site-specific VRT files (e.g., Site1a_VRT.vrt, Site_2_VRT.vrt) to cover full flight areas.
- Metadata and accessibility:
  - Data are provided with accompanying ENVI headers; guidance available via hsdar for handling hyperspectral data in R.
  - QA performed by NERC FSF before mosaic creation, with preprocessing steps described in section 2.

## Processing, Quality Assurance, and Access
- Preprocessing and processing steps include orthorectification, radiometric correction to surface reflectance (empirical line method), and generation of mosaicked imagery via VRTs.
- QA validation carried out by NERC Field Spectrometry Facility (FSF) prior to mosaic creation.
- Data accessibility:
  - Comprehensive file naming conventions and structured folders for site-specific data, enabling straightforward discovery and integration.
  - Compatibility with common tools (ENVI, R with hsdar) for analysis and metadata extraction.

## Data Governance, Standards, and Usability Considerations for Data Leaders
- Data lineage and provenance:
  - Clear linkage between hyperspectral lines, LiDAR data, DEMs, and resulting VRT mosaics.
  - Use of PPK GPS/IMU for precise orthorectification and alignment with LiDAR-derived DEM.
- Data quality and coverage:
  - Acknowledged data gaps in dense canopy zones; transparent documentation of data limitations and conditions during collection.
- Standardization and metadata:
  - Consistent naming conventions for hyperspectral files and LiDAR/DEM assets.
  - Surface reflectance data with explicit spectral range, scale, and band count; 32-bit floating point precision documented.
  - Spatial reference system explicitly specified (EPSG: 4326, WGS 84); ready for cross-project interoperability.
- Reproducibility and reuse:
  - Processing workflow described (orthorectification, empirical line correction, QA), with access to preprocessed mosaics via VRTs.
  - ENVI headers and hsdar compatibility facilitate replication in common analysis environments.
- Collaboration and community alignment:
  - Data packaged with comprehensive site-level context (dates, conditions, sensor setup) supporting cross-site analyses and potential sharing with research networks studying drought effects on forests.
- Practical considerations for future data strategy:
  - Maintain and extend metadata to cover wind data gaps and irradiance monitoring absence.
  - Consider additional standardization for atmospheric corrections and cloud-affected line handling.
  - Ensure continued QA documentation and versioning for future mosaic campaigns.

## Key Takeaways for Data Leaders
- This dataset exemplifies coordinated multi-sensor remote sensing (hyperspectral + LiDAR) across multiple sites with rigorous data management, provenance, and QA.
- The combination of 10 cm LiDAR-derived DEMs with high-resolution hyperspectral reflectance enables detailed canopy analysis under drought stress, while the structured data organization supports scalable reuse and cross-site comparisons.
- Provenance, metadata richness, and clear processing steps are central to ensuring data usability, discoverability, and alignment with broader data strategy goals.