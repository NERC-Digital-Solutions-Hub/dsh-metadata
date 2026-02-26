# Daily and sub-daily hydrometeorological and soil data (2013-2022) [COSMOSUK]

- Overview
  - COSMOS-UK network comprises 51 sites with time series from 2013 to 2022.
  - Dataset includes 258 files: site metadata, sub-hourly data and flags/metadata, daily data with derived variables (VWC, PE, SWE), and corresponding QC/flags.
  - Data cover hydrometeorology and soil moisture (and derived soil properties) at multiple resolutions and depths.
  - Data are hosted via COSMOS-UK/NERC Environmental Information Data Centre; more details are on the COSMOS-UK website.

- Data coverage and structure
  - Sub-hourly (30-minute resolution) data files per site (COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022.csv) with 30-minute end-of-interval timestamps.
  - Daily data files per site (COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022.csv) with daily totals or means for derived variables.
  - Metadata files accompany both sub-hourly and daily data, plus separate QC Flags files and general site metadata.
  - Missing values are coded as -9999 in data files.
  - Telemetry: data are aggregated on the logger (mean or sum over 30-minute periods) and transmitted hourly to a central system.

- Key data components and variables
  - Sub-hourly data variables (examples): incoming/outgoing longwave and shortwave radiation (LWIN, LWOUT, SWIN, SWOUT), net radiation (RN), precipitation types (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), atmospheric pressure (PA), air temperature (TA), wind speed/direction (WS, WD), humidity (Q, RH), snow depth (SNOW_DEPTH), heat fluxes (G1, G2), soil temperature and moisture at multiple depths (TDT*, VWC, STP_TSOIL*), albedo-related variables (ALBEDO), and derived metrics (PE, GCC, SWE, COSMOS_VWC, CTS_MOD_CORR, D86_75m).
  - Daily data variables (examples): LWIN, LWOUT, SWIN, SWOUT (in MJ m-2 day-1 or equivalent), RN (daily total), PRECIP/precipitation components (mm day-1), PA, TA, WS, WD, Q, RH, soil variables (TDT*, VWC), G1, G2, SWE, PE, GCC, COSMOS_VWC, CTS_MOD_CORR, D86_75m, SNOW, SNOW_DEPTH, ALBEDO.
  - Derived daily products include volumetric water content (VWC) from CRNS, snow water equivalent (SWE) and albedo estimates, potential evapotranspiration (PE) via Penman-Monteith, and PhenoCam-derived green colour content (GCC).
  - For QC, two flag systems exist: QC flags (why data were removed) and data flags (whether data are infilled/estimated).

- Quality control and flags
  - Two-stage QC:
    - Automatic QC tests run on applicable variables; failing data are flagged and removed.
    - Daily visual inspection of data via automated plots.
  - QC flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv (structure mirrors data file; appended with _QCFLAG).
  - Data flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Flags.csv (values M, U, I, E describing missing, unchecked, infilled, estimated).
  - Important distinction:
    - QC flags explain why data were removed and do not reflect data content; non-zero QC flag values imply infilled/estimated data in the corresponding data value.
    - Data flags indicate data status (e.g., infilled or estimated) for the value itself.

- Sub-hourly data details
  - Variables are described in the sub-hourly metadata (COSMOS-UK_HydroSoil_SH_2013-2022_Metadata.csv).
  - Infilled values are explicitly indicated (e.g., PA, TA, G1, G2) with notes on infill status per variable.
  - Net radiation (RN) and absolute humidity (Q) are not run through QC tests because they are derived from QC’d inputs.

- Daily data details
  - Derived variables (VWC, SWE, PE) are generated from sub-hourly data and ancillary sensors (e.g., CRNS for VWC, albedo/PhenoCam for GCC, and SNOW thresholds for Snow Day/SWE estimation).
  - SWE estimates use snow-day classification based on albedo (10:00–14:00 GMT) and a snow-free reference count rate to derive snow depth at midday.
  - PE is computed using Penman-Monteith method with RN, G (mean of G1 and G2), TA, RH, WS, and PA.
  - GCC is derived from PhenoCam images; daily GCC is the maximum value observed in a day, with masks applied to focus on surrounding field areas. Note: daily GCC data are not quality-controlled.
  - Daily data products are derived from sub-hourly inputs; QC applies to sub-hourly data, and daily values inherit QC status from underlying data.

- Infilling
  - Infilling fills gaps in time series with interpolation (linear or second-order polynomial).
  - Gap and method selection criteria:
    - Gap size: up to 10 values for linear; larger gaps may use polynomial with more surrounding values (up to 4 on each side).
    - RMSE-based selection: 5000 artificial gaps are used to evaluate interpolation methods for each variable; the best method is chosen per gap.
  - Infilling is applied to selected sub-hourly and daily variables; some datasets (e.g., GCC) may not undergo QC-based infilling.

- Completeness
  - A site-by-site completeness assessment is provided, combining Met (met variables: precipitation, humidity, air temperature, pressure, radiation, wind) and Soil (soil heat flux, soil temperature, TDT moisture sensors) groups; VWC completeness is reported for CRNS-derived data.
  - The document provides a completeness table per site, reflecting overall data availability across the included variable groups.

- Instrumentation and site variability
  - Instruments used include:
    - Cosmic-Ray Neutron Sensor (CRNS) for VWC; counts corrected for pressure, humidity, and cosmic ray intensity; footprint tens of meters, effective depth ~15–40 cm; data corrected via CTS_MOD_CORR.
    - Rain gauges (OTT Pluvio 1), tipping-bucket gauges (RainE), and SnowFox snow-related sensors.
    - Time-domain transmissometry soil moisture sensors (TDT) and soil temperature sensors (STP) at multiple depths.
    - Heat flux plates (0.03 m depth) and radiometer (NR01) for net radiation and radiation components.
    - Automatic weather station components (air temperature, humidity, barometer).
    - PhenoCam (GCC) for greenness proxy; field masks applied to isolate site surroundings.
    - Snow depth sensors (SR50A) and snow-related data products.
  - Site variations: instrumentation configurations differ by site and over time; Tables 8–9 in the document summarize installation types and site-specific setups.

- Data changes and versioning
  - The data undergo periodic reprocessing to incorporate improvements.
  - Examples of major changes:
    - Reprocessing VWC at Hollin Hill (Feb 2023) due to pressure sensor calibration error.
    - Removal of certain heat flux values (G1, G2) from 00:30 and 01:00 data (Feb 2023) due to midnight calibration artifacts.
    - Infilling updates and methodological revisions (e.g., 2022 infilling improvements for multiple variables).
    - Sensor recalibrations and updates to calibration/processing parameters (e.g., VWC calibration values, D86_75m depth corrections).
  - A detailed chronology lists changes from 2019–2023.

- Authorship and references
  - Primary data author: S. Stanley; project/data management and site coordination by a team including H.M. Cooper, M. Fry, R. Smith, O. Swain, H.C. Ward, and others.
  - References include foundational papers on CRNS calibration, soil moisture methods, and radiometric/meteorological instrumentation and methods used in COSMOS-UK.

- Practical implications for data use
  - Rich, multi-sensor dataset suitable for investigating soil moisture dynamics, energy balance components, precipitation partitioning, and vegetation/phenology signals at landscape scales.
  - Users should account for site- and time-dependent instrument configurations, QC and data-flag meanings, and the distinction between QC-derived removals and infilled/data-flagged values.
  - Derived daily products (VWC, SWE, PE, GCC) come with their underlying data provenance and QC/flag considerations.

- Access and citation
  - Data are hosted under COSMOS-UK and the NERC Environmental Information Data Centre; refer to the Stanley et al. (2023) documentation for detailed data descriptions, processing steps, and methodological references.