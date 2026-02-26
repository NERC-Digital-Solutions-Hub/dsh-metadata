# COSMOS-UK Daily and sub-daily hydrometeorological and soil data (2013-2019) [COSMOSUK]

- Overview
  - A comprehensive dataset from 51 COSMOS-UK sites covering 2013–2019.
  - Contains 208 files split into site metadata, sub-hourly, hourly, and daily data plus corresponding QC and metadata files.
  - Data are telemetered to UKCEH and undergo multi-stage quality control.

- Data resolution, period, and scope
  - Sub-hourly data at 30-minute resolution from Oct 2013 to Dec 2019.
  - Hourly volumetric water content (VWC) derived from cosmic-ray neutron sensors; hourly hydro-soil data (sub-hourly data processed to hourly).
  - Daily data (2013–2019) include VWC, potential evapotranspiration (PE), and snow water equivalent (SWE).
  - Complete metadata describing sites, instrumentation, and data processing.

- File structure and contents
  - COSMOS-UK_SiteMetadata_2013-2019.csv: site locations, coordinates, soil and land-cover info, and site characteristics.
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019.csv and COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019_Metadata.csv: sub-hourly meteorological and soil variables; missing values marked as -9999.
  - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2019.csv and Metadata: hourly VWC data and related variables.
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2019.csv and Metadata: daily VWC, PE, SWE; includes albedo-derived snow indicators and snow-day flag.
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019_QC_Flags.csv and corresponding QC flag files: quality control flags for each data point.

- Variables and data sources
  - Meteorological and radiometric: incoming/outgoing longwave (LWIN/LWOUT), incoming/outgoing shortwave (SWIN/SWOUT), net radiation (RN), precipitation, atmospheric pressure, air temperature, relative humidity, wind speed/direction, absolute humidity, and albedo.
  - Snow and soil: snow depth, SWE, soil temperature at multiple depths, soil moisture (VWC) from TDT sensors, soil heat flux (G1/G2), and TDT moisture/ocean sensors.
  - Volumetric water content (VWC) also derived hourly from CRNS (cosmic-ray neutron sensor) data; daily VWC calculated as daily mean of hourly corrected counts.

- Data processing and quality control
  - Automatic QC tests applied to relevant variables; data failing tests are flagged and removed; unique QC flags allow traceability of failures.
  - QC flags are stored in separate files with suffixes _QCFLAG and mirror the structure of the data files.
  - Two-stage QC: automated processing script tests plus daily visual inspection of plots.
  - Missing data are coded as -9999; complex QC codes include missing data, zero values where not plausible, too few samples, low power, sensor faults, out-of-range values, spikes, and other diagnostic flags.
  - All time stamps are end-of-interval for sub-hourly data; daily timestamps reflect the start of the 24-hour period (00:00) for the preceding day, except for daily albedo and SWE calculations.

- Derivation of key variables
  - VWC from CRNS:
    - Corrected neutron counts account for background cosmic ray intensity (NMDB reference), altitude, atmospheric pressure, and humidity.
    - Site-specific N0 calibration derived from field calibration; accounts for lattice/bound water and soil organic carbon.
    - 2018 correction factor Fi applied to counts to adjust for fluctuations in incoming cosmic rays.
  - SWE and albedo:
    - Snow days identified using daily albedo thresholds (10:00–14:00 GMT): snow day if albedo > 50%; end when albedo < 35%.
    - SWE estimated from differences between measured counts and snow-free reference counts (Wallbank et al. 2020 method).
  - Potential evapotranspiration (PE):
    - Calculated with Penman-Monteith method using RN, soil heat flux, TA, RH, WS, and PA; daily PE is the sum of positive sub-hourly values (negative sub-hourly PE ignored).
  - Time stamps:
    - Sub-hourly data end at the timestamp (e.g., 12:30 represents data from 12:00–12:30).
    - Daily data timestamped at 00:00 for the preceding 24 hours.

- Completeness and caveats
  - Completeness by site summarized in Table 6.1; overall data coverage varies across meters and soil/meteorological variables.
  - VWC data completeness is tied to CRNS data quality and snow cover effects (snow can bias VWC estimates; SWE derived to mitigate some impacts).
  - Spatial footprint and depth of CRNS influence the effective sampling depth (roughly 15–40 cm; footprint extends tens of meters).

- Instrumentation and site coverage
  - Primary instruments include:
    - Cosmic-Ray Neutron Sensor (CRNS) – Hydroinnova CRS-2000/B and CRS-1000/B.
    - Rain gauge – OTT Pluvio.
    - Point soil moisture sensors (TDT) at multiple depths.
    - Soil heat flux plates – Hukseflux HFP01SC.
    - Soil temperature sensors – Hukseflux STP01.
    - Radiometer – Hukseflux NR01 (net radiation via up/down components).
    - Automatic weather station – Rotronic HC2A-S3 with supporting sensors.
    - Barometric pressure – Vaisala PTB110.
    - Temperature/humidity – Vaisala HUMICAP HMP155A.
    - Wind measurement – 3D Sonic Anemometer and 2D integrated WindSonic.
    - Snow depth – Campbell SR50A.
    - SWE – Hydroinnova SnowFox.
    - Data logger – Campbell Scientific CR3000.
  - Not all instruments are installed at every site; site-by-site instrumentation details are provided (Table 7.1).

- Changes to data and updates
  - Major revisions include:
    - Jan 2021: D86_75m correction for CRNS effective depth.
    - Jul 2020: VWC calibration updates; CRNS counts infilled from secondary tubes; NMDB data infilled; 30-minute precipitation calculation updated.
    - Apr 2020: PE methodology revised and 30-minute values aggregated to hourly and daily.
    - Dec 2019: SWE added; daily albedo included.
  - Data reprocessing occurs when improvements are implemented.

- Access, provenance, and references
  - Data hosted at NERC Environmental Information Data Centre (COSMOS-UK repository).
  - Documentation and user guides are linked from the COSMOS-UK website (cosmos.ceh.ac.uk).
  - Key methodological references include Evans et al. 2016; Zreda et al. 2012; Franz et al. 2012/2013; Köhli et al. 2015; Wallbank et al. 2020; and FAO 1998.

- Author contributions and contact
  - Primary author: S. Stanley; data managers and calibration/maintenance teams documented; project management and site metadata contributors listed.