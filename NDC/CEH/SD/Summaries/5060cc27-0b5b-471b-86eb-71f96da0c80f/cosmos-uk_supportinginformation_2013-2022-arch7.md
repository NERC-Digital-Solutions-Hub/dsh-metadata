# COSMOS-UK Daily and sub-daily hydrometeorological and soil data (2013-2022) [COSMOSUK]. NERC Environmental Information Data Centre.

- A comprehensive COSMOS-UK data collection documenting daily and sub-daily hydrometeorological and soil moisture measurements from 51 sites over 2013–2022.
- Structure includes 258 files: site metadata, sub-hourly data and flags, daily data and flags, and corresponding metadata.
- Data are housed on the COSMOS-UK network with coordinates, soil types, land cover, and decommissioning notes for some sites.

## Spatial and Temporal Coverage
- 51 COSMOS-UK sites with geographic coordinates (OSGB36 and WGS84 references).
- Time period: October 2013 to December 2022 (end of 2022).
- Data include both sub-hourly (30-minute resolution) and daily time series, with hourly telemetries to central system.

## Data Structure and Files
- Sub-hourly data: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022.csv
- Sub-hourly metadata: COSMOS-UK_HydroSoil_SH_2013-2022_Metadata.csv
- Sub-hourly QC flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_QC_Flags.csv
- Sub-hourly data flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2022_Flags.csv
- Daily data: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022.csv
- Daily metadata: COSMOS-UK_HydroSoil_Daily_2013-2022_Metadata.csv
- Daily flags: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2022_Flags.csv
- Full data and QA structures use -9999 for missing values, with QC and data flags to indicate data provenance.

## Variables and Derived Data
- Sub-hourly (30-minute resolution, Oct 2013–Dec 2022): radiation (LWIN/LWOUT/SWIN/SWOUT), net radiation (RN), precipitation (PRECIP, PRECIP_TIPPING, PRECIP_RAINE), atmospheric pressure (PA), air temperature (TA), wind (WS, WD, UX/UY/UZ), humidity (Q, RH), snow depth (SNOW_DEPTH), soil moisture and temperature at multiple TDT sensors (TDT1–TDT10_VWC/TSOIL, STP_TSOILx), heat fluxes (G1/G2), and additional derived variables (COSMOS_VWC, SWE, PE, GCC, ALBEDO, GCC from PhenoCam).
- Daily (aggregated 30-min data to daily): LWIN/LWOUT/SWIN/SWOUT, RN, PRECIP/RN etc., plus derived daily metrics such as PE (Penman-Monteith), SWE, ALBEDO, and GCC (from PhenoCam).
- Derived data: 
  - Volumetric Water Content (VWC) from Cosmic-Ray Neutron Sensor (CRNS) using CTS_MOD_CORR with corrections for altitude, pressure, and humidity; site-specific N0 calibration; corrections for lattice water and soil organic carbon.
  - Snow Water Equivalent (SWE) estimated from CRNS counts on snow days detected via albedo thresholds.
  - Potential Evapotranspiration (PE) via FAO Penman-Monteith using RN, G1/G2, TA, RH, WS, PA.
  - Green Colour Content (GCC) from PhenoCam imagery; daily maximum GCC with site masks; note: GCC data not quality controlled in this dataset.
- Flags:
  - QC flags (per variable) explain data removals due to QC tests; separate QC flag files mirror data structure with _QCFLAG.
  - Data flags indicate infilling or estimation (M = missing, U = unchecked, I = infilled, E = estimated).

## Quality Control and Infilling
- Two-stage QC:
  - Automated QC tests with variable-specific checks; failing data removed; flags stored in QC files.
  - Daily visual inspection via plots.
- QC flags provide traceability of why data were removed or infilled.
- Data flags indicate data provenance (M, U, I, E) and mirror data structure.
- Infilling:
  - Simple interpolation (linear or second-order polynomial) for gaps deemed reasonable.
  - Gap acceptance: up to 10 values; uses up to 4 surrounding values for polynomial interpolation.
  - RMSE-based method selection to identify best interpolation approach for each variable and gap scenario.
  - Infilling applied only to selected sub-hourly and daily variables; infilled values flagged accordingly.

## Completeness
- Site-wide completeness summarized for Met (meteorological) and Soil groups (including VWC for CRNS-derived data) over 2013–2022.
- VWC completeness described separately due to CRNS-derived methodology and snow-day handling.

## Instrumentation and Site Variability
- Network instruments include:
  - Cosmic-Ray Neutron Sensor (CRNS) for VWC; corrections for pressure, humidity, and cosmic-ray flux; multiple methods for converting counts to VWC.
  - Rain gauges (OTT Pluvio) and tipping-bucket rain gauges (RainE) for precipitation measurements.
  - Time-domain reflectometry soil moisture sensors (TDT) at multiple depths for VWC and temperature.
  - Soil heat flux plates at 0.03 m depth.
  - Radiometer (four-component) for net radiation.
  - Automatic weather station (temperature, humidity, pressure).
  - PhenoCam for GCC (vegetation greenness) with site masks; images up to 5 per day.
- Site variability: instrument configurations differ by site and time; decommissioned sites noted (e.g., Wytham Woods, Redmere, Cochno, Harwood Forest).
- Comprehensive instrumentation details provided in Section 7, with site-specific setup tables (8–9).

## Data Access and Use
- Data are hosted and described by NERC Environmental Information Data Centre; COSMOS-UK website provides project context and user guides.
- Documentation emphasizes that derived daily data (e.g., GCC) have not undergone separate QC, but all sub-hourly values feeding them are QC-checked.

## Data Quality, Reprocessing and Changes
- Data are subject to ongoing review; major data changes trigger full reprocessing of the time series.
- Notable changes include recalibration for VWC (CRNS) at Hollin Hill, removal of certain heat-flux values, refined infilling, and updates to calibration constants and processing methods over time.
- Change history entries detail months and specifics (e.g., Feb 2023 reprocessing, 2022–2021 calibration updates, Snow/EW derivations).

## Author Contributions and References
- S. Stanley as primary contact; multiple collaborators contributed to data management, site metadata, system design, instrumentation, and processing algorithms.
- References include methodological papers on CRNS calibration, VWC derivation, SWE estimation, and standard hydrology/meteorology sources (e.g., Zreda et al., Desilets et al., Franz et al., FAO 56).