# Supporting documentation for COSMOS-UK. Stanley et al. (2023). Daily and sub-daily hydrometeorological and soil data (2013-2022) [COSMOSUK]. NERC Environmental Information Data Centre.

- Overview
  - 51 COSMOS-UK sites with data from 2013 to end-2022.
  - Time resolution includes sub-hourly (30-minute) and daily data.
  - Dataset comprises 258 files: site metadata, sub-hourly data and flags, daily data and flags, and associated metadata.
  - Data are recorded on site, telemetered hourly to a central system, and processed with quality control and infilling where appropriate.
  - Decommissioned sites noted (e.g., Wytham Woods, Redmere, Cochno, Harwood Forest).

- Data structure and files
  - COSMOS-UK_SiteMetadata_2013-2022.csv: site locations, coordinates, soil type, land cover, soil properties; includes start/end dates per site.
  - Sub-hourly data and metadata: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022.csv and COSMOS-UK_HydroSoil_SH_2013-2022_Metadata.csv.
  - Sub-hourly QC: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv; Sub-hourly data flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Flags.csv.
  - Daily data and metadata: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022.csv and COSMOS-UK_HydroSoil_Daily_2013-2022_Metadata.csv.
  - Daily data flags: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022_Flags.csv.
  - Data processing and methods are documented across these sections and related support materials.

- Sub-hourly hydrometeorological and soil data (30-minute resolution)
  - Variables include: LWIN, LWOUT, SWIN, SWOUT, RN (net radiation), PRECIP, PRECIP_TIPPING, PRECIP_RAINE, PA (pressure), TA (temperature), WS (wind speed), WD (wind direction), Q (absolute humidity), RH (relative humidity), SNOW_DEPTH, wind components (UX, UY, UZ), heat fluxes (G1, G2), soil temperatures and volumetric water content (TDT and STP sensors at multiple depths).
  - Timestamps are end-of-interval (e.g., 12:30 for data from 12:00–12:30).
  - QC and data flags separate from the primary data files.

- Daily hydrometeorological and soil data (derived metrics)
  - Derived/derived-from-data variables at daily resolution include: volumetric water content (VWC) from CRNS (COSMOS_VWC), snow water equivalent (SWE), snow days, atmospheric pressure, wind metrics, albedo, potential evapotranspiration (PE) via Penman-Monteith, and green colour content (GCC) derived from PhenoCam imagery.
  - SWE and VWC are derived with methods that account for snow presence and CRNS corrections; daily VWC uses corrected neutron counts and calibration steps.
  - GCC is derived from PhenoCam imagery with site-specific masks; note that GCC has not undergone QC.

- Quality control and data flags
  - Two-stage QC for sub-hourly data:
    - Automatic QC scripting with tests per variable; flagged and removed where failing tests.
    - Daily visual inspection of automatically generated plots.
  - QC flags file explains why data were removed (non-zero QC flags); some variables (RN and Q) are not QC’d because they are derived from QC’d inputs.
  - Data flags file describes data quality status (M = Missing, U = Unchecked, I = Infilled, E = Estimated).
  - QC and data flags are provided per site and mirror the structure of the main data files with appropriate suffixes.

- Completeness
  - Site-level completeness assessed across Met (meteorological) and Soil groups; VWC completeness reported for CRNS-derived data.
  - Completeness varies by site and variable; overall data coverage documented for October 2013–December 2022.

- Infilling
  - Infilling fills gaps in selected variables using interpolation (linear or order-2 polynomial).
  - Gap acceptance: up to 10 consecutive values; interpolation method chosen based on surrounding data and RMSE testing.
  - RMSE-based method selection is used to determine the best infilling approach for each variable and gap scenario.
  - Infilling is recorded in data, with corresponding infill indicated in the data flags (I).

- Instrumentation
  - COSMOS-UK uses a range of instruments (e.g., Cosmic-Ray Neutron Sensor for VWC, OTT Pluvio rain gauge, tipping bucket RainE, Time Domain Transmissometry soil moisture sensors, Hukseflux soil heat flux plates, STP soil temperature sensors, radiometer, automatic weather station, barometric and humidity sensors, 3D sonic anemometers, PhenoCam, SnowFox, CRNS count correction, etc.).
  - Instrumentation has evolved over time; Section 7 details instrument types and site-specific configurations, including capacity for multiple sensors and site-specific setups.

- Data changes and reprocessing
  - Data processing is continually reviewed; major changes trigger reprocessing of the full time series.
  - Notable updates include VWC recalibration, changes to heat flux handling, interpolation adjustments for small gaps, and updated calibration constants (e.g., Gamma values, N0_MOD, N_MIN, N_MAX).
  - History of changes includes significant updates in 2019–2023 (e.g., SWE addition, daily albedo, infilling enhancements, VWC recalibrations).

- Access, authorship, and references
  - Authored and managed by S. Stanley and the COSMOS-UK team; data management and site operations coordinated across multiple contributors.
  - Data and methodologies referenced to peer-reviewed sources on cosmic-ray soil moisture, calibration methods, and derivation approaches (e.g., Baatz et al., Franz et al., Zreda et al., Evans et al., Wallbank et al.).

- Relevance for environmental monitoring analysts
  - Provides a standardized, quality-controlled, long-term dataset of sub-hourly and daily hydrometeorological and soil moisture variables across a broad UK network.
  - Enables assessment of environmental health, soil moisture dynamics, evapotranspiration, and energy balance components over time.
  - Rich derived data (VWC via CRNS, SWE, PE, GCC) support complex analyses and cross-dataset integrations, with clear QC and data-flag transparency to inform uncertainty and data suitability for policy monitoring and scientific applications.