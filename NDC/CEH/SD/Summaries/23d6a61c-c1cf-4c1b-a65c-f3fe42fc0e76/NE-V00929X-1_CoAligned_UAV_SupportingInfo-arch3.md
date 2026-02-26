Co-aligned Hyperspectral and LiDAR UAV data collected in drought stressed European beech forest, Rhon Biosphere Reserve, Germany, 2020

## Overview
- Co-aligned hyperspectral (273 bands, 399–1001 nm) and LiDAR data from four sites in the UNESCO Rhön Biosphere Reserve.
- Focused on drought-stressed European beech forest (Fagus sylvatica) and collected September 2020 with the Headwall Hyperspec Nano sensor.
- Data designed to support environmental health monitoring and forest health assessments at high spatial and spectral resolution.

## Methods
- Study sites: four sites (1a, 1b, 1c, 2) within core protected areas; images captured in Sep 2020.
- Acquisition details per site: times, sky conditions, sensor configuration, UAV flight parameters.
  - Typical altitude ~80–90 m; ground sampling distance (GSD) ~3.5–3.9 cm; velocity ~6–8.7 m/s; camera angle −90°.
  - Overlaps: line overlap 40%, flight overlap 1% (nominally listed as 1%, likely a placeholder; main overlap is 40%).
- Data processing: orthorectified lines using PPK GPS/IMU and LiDAR-derived 10 cm DEM; reflectance corrected with empirical line method.
- Observations: some data gaps in dark canopy areas; occasional cloud darkening due to irradiance monitoring gaps during flight.

## Data Structure, Nature and Units
- Total: 685 files, organized by site (1a, 1b, 1c, 2) into subfolders of flight lines.
- Hyperspectral data
  - 32-bit floating point, 0–1 reflectance scale, 273 spectral bands, 399–1001 nm.
  - ~5 cm pixel size; EPSG: 4326 (WGS 84) geographic coordinates.
  - Two-part file naming: raw_[number]_rd_rf_or and raw_[number]_rd_rf_or.hdr.
  - ENVI header files readable in ENVI or via R (hsdar package).
- LiDAR and ancillary data
  - Cleaned LAS files (removal of random above-canopy points).
  - Velodyne LiDAR sensor integrated in Headwall system.
  - 10 cm DEMs produced from maximum LiDAR returns (per site).
  - DEM files named per site (e.g., Site1a_lidar_dem.tif).
  - Virtual raster mosaics (VRT) for each site (e.g., Site1a_VRT.vrt).
- Quality assurance
  - QA performed by NERC FSF prior to creation of mosaicked images; pre-processing steps referenced in section 2.

## Data Processing and Quality
- Orthorectification relies on PPK GPS/IMU data and LiDAR-derived 10 cm DEMs.
- Data are surface reflectance, processed via empirical line correction.
- Metadata and data provenance are emphasized; some gaps in metadata noted (e.g., limited wind data in some lines; irradiance monitoring gaps causing cloud-darkening artifacts).

## Metadata, Access & Standards
- Spatial reference: EPSG:4326; geographic coordinates.
- Hyperspectral files include ENVI headers for compatibility with standard analysis tools.
- Documentation highlights how to read headers (e.g., via ENVI or R hsdar).

## Implications for Monitoring Frameworks
- Strengths for environmental health monitoring
  - Combines high-resolution structural (LiDAR) and spectral (hyperspectral) information to assess forest health, canopy structure, and stress indicators.
  - Fine spatial scale (≈5 cm pixels) enables detailed assessment within protected forest areas.
  - DEMs and LiDAR-derived products support biomass and canopy modeling.
- Data quality and governance considerations
  - Data gaps in dark canopy areas and cloud/darkening artifacts can affect comparability across lines; requires careful masking and quality control in analyses.
  - Requires careful metadata management and possible coordination with originators to fill gaps (wind data, irradiance details, etc.).
  - Standardized formats and headers support interoperability, but ongoing governance is needed to maintain accessibility and reproducibility.

## Key Considerations for Authors of Monitoring Frameworks
- When integrating such datasets, plan for:
  - Handling data gaps and atmospheric/illumination effects in hyperspectral data.
  - Ensuring consistent reflectance corrections and documentation of processing steps.
  - Establishing metadata requirements and data provenance to facilitate data sharing and reuse.
  - Leveraging the complementary LiDAR and hyperspectral information to derive robust environmental health indicators (e.g., drought stress, canopy structure, foliar properties).

## Potential Applications for Policy and Decision-Making
- Development of forest health indicators for drought response and resilience strategies.
- Improved monitoring of protected forest ecosystems through integrated structural and spectral metrics.
- Support for reporting under environmental health and biodiversity policies by providing high-resolution, multi-sensor datasets and derived metrics.