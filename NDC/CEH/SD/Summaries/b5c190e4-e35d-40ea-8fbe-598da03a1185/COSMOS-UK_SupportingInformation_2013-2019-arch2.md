# Supporting documentation for COSMOS-UK. Stanley et al. (2021). Daily and sub-daily hydrometeorological and soil data (2013-2019) [COSMOSUK]. NERC Environmental Information Data Centre.

## Introduction
- Contains daily and sub-daily time series of hydrometeorological and soil moisture data from 51 COSMOS-UK sites (2013–2019).
- Comprises 208 files, including site metadata, sub-hourly data and QC flags, hourly data, and daily data for hydrosoil variables.
- Data portal: COSMOS-UK website; documentation is based on the COSMOS-UK User Guide.

## Dataset Structure and Content
- Data files (examples):
  - COSMOS-UK_SiteMetadata_2013-2019.csv
  - Sub-hourly hydrosoil data and QC flags (per site)
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019.csv and corresponding metadata
  - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2019.csv and metadata
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2019.csv and metadata
- Variables and outputs:
  - Sub-hourly (30-minute) and hourly hydrometeorological data (radiation, precipitation, air temperature, humidity, pressure, wind, etc.)
  - Soil data: soil temperature at multiple depths and soil volumetric water content (VWC)
  - Daily data: VWC, potential evapotranspiration (PE), snow water equivalent (SWE), snow day indicator, albedo
- Data handling:
  - Missing values are coded as -9999.
  - Timestamps: sub-hourly data end of the 30-minute period; daily data timestamps refer to the start of the day (00:00) and cover the preceding 24 hours.
- Data quality:
  - Two-stage QC: automated QC tests plus daily visual inspection.
  - QC flags stored in separate COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019_QC_Flags.csv (column names end with _QCFLAG).
  - Data failing QC are removed; flags preserve traceability to the specific tests failed.

## Sub-hourly, Hourly, and Daily Data
- Sub-hourly data (SH):
  - Resolution: 30 minutes; includes standard meteorological variables and soil measurements.
  - Some sensors have site-specific exceptions (e.g., snow depth, wind components, TDT sensor counts at certain depths).
- Hourly data:
  - VWC derived from CRNS data and on-site corrections; 30-minute counts aggregated to hourly totals.
  - VWC is derived using site-specific calibration (N0 method) with corrections for atmospheric pressure, humidity, and cosmic-ray intensity.
  - D86_75m and related soil temperature/moisture variables provided for multiple depths.
- Daily data:
  - VWC, PE (Penman-Monteith), SWE derived from CRNS data and albedo-based snow detection.
  - SWE estimation uses daily count differences relative to snow-free conditions; midday SWE value computed from counts over the day.
  - Snow days flagged using albedo thresholds (average 10:00–14:00 GMT); PE calculated from sub-hourly data with positive contributions only.
  - 30-minute data aggregated to daily values where applicable; D86 depths summarized as daily means.

## Methodology
- On-site instrumentation records data to loggers; data telemetered hourly to UKCEH Wallingford.
- Processing and QC:
  - Automatic QC tests applied to relevant variables; each test has a unique flag value; combinations add up to a final flag for traceability.
  - Daily visual inspection complements automated QC.
- VWC derivation:
  - CRNS neutron counts corrected for background cosmic rays (via Jungfraujoch reference), altitude, atmospheric pressure, and absolute humidity.
  - Methods to derive VWC from corrected counts include site-specific N0 calibration (primary method used here), universal calibration (hmf), and neutron transport modelling; COSMOS-UK uses site-specific N0 with corrections for lattice water and soil organic carbon.
  - 2018 adjustment: added correction factor Fi to account for fluctuations in incoming cosmic rays (geomagnetic effects and reference-counter differences).
- Snow and energy balance:
  - SWE calculation method described (Wallbank et al., 2020); snow days identified via albedo thresholds.
  - PE computed from net radiation, soil heat flux, air temperature, humidity, wind, and pressure (FAO 56/Penman-Monteith).

## Completeness
- Completeness assessed and reported per site for combined data groups (Met, Soil) and for derived VWC data.
- Met: precipitation, humidity, air temperature, atmospheric pressure, radiation, wind, etc.
- Soil: soil heat flux, soil temperature, and VWC from TDT sensors.
- VWC completeness reflects CRNS-derived data completeness.

## Instrumentation
- Cosmic-Ray Neutron Sensor (CRNS):
  - Models: Hydroinnova CRS-2000/B and CRS-1000/B; footprint tens of meters, effective soil moisture depth ~15–40 cm.
- Rain gauge:
  - Model: OTT Pluvio (with corrections for installation context).
- Soil moisture and related sensors:
  - TDT soil moisture sensors with multiple depths; soil temperature sensors (TDTs and STP variants).
- Energy and radiation sensors:
  - Radiometer (NR01) for solar and longwave components; integrated 4-component measurements.
- Atmospheric and meteorological sensors:
  - Automatic weather station (Rotronic HC2A-S3), barometric pressure sensor, Vaisala HUMICAP humidity/temperature probe, 3D and integrated 2D sonic anemometers.
- Snow sensors:
  - Snow depth (SR50A) and SnowFox SWE sensor for snowpack measurements.
- Data logging and communications:
  - Micrologger (CR3000) for measurement and control, with field engineering support for maintenance.

## Changes to Data
- Data processing and calibration updates implemented to improve consistency and accuracy:
  - Jan 2021: D86_75m and CRNS effective depth correction updated.
  - Jul 2020: VWC calibration values updated; CRNS data infilling from secondary tubes; NMDB data infilling; 30-minute precipitation computation updated.
  - Apr 2020: PE methodology updated (switch to 30-minute values aggregated to hourly/daily).
  - Dec 2019: SWE added; daily albedo added; snow-day methodology introduced.
- Reprocessing of full time series whenever major improvements are made.

## Author Contributions
- S. Stanley: primary author and data contact.
- Data managers: H. M. Cooper, M. Fry, O. Hitt, O. Swain.
- Instrument calibration and maintenance, site engineering, project management, metadata, and data presentation contributions listed.

## References and Related Documentation
- Foundational methodological references for calibration, VWC derivation, snow estimation, and CRNS processing (e.g., Baatz et al., Bogena et al., Desilets et al., Franz et al., Zreda et al., Evans et al., Wallbank et al.).
- COSMOS-UK data processing and validation framework described in Stanley et al. 2021; COSMOS-UK User Guide available via COSMOS-UK website.