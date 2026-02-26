# Daily and sub-daily hydrometeorological and soil data (2013-2019) [COSMOSUK]

## Overview
- Supporting documentation for the COSMOS-UK dataset (Stanley et al., 2021).
- Contains daily and sub-daily time series of hydrometeorological and soil moisture data from 51 COSMOS-UK sites, 2013–2019.
- Dataset comprises 208 files, including site metadata, sub-hourly data and QC, hourly data, and daily data (plus corresponding metadata).

## Data products and structure
- Sub-hourly data (30-minute resolution) for each site, with a separate sub-hourly QC flag file.
- Hourly data, including volumetric water content (VWC) derived from cosmic-ray neutron sensing.
- Daily data (VWC, potential evapotranspiration, snow water equivalent).
- Metadata files accompanying each data type (site metadata, data variable descriptions).
- All values missing are coded as -9999 in data files.
- QC workflow:
  - Automatic QC tests with per-variable flags; failures result in data removal and a combined QC flag value saved in a separate QC file (structure mirrors data files with _QCFLAG appended to column names).
  - Daily visual QC review complements automatic QC.

## Data resolution and variables
- Sub-hourly (30-minute) data includes: incoming/outgoing longwave and shortwave radiation, net radiation, precipitation, atmospheric pressure, air temperature, wind speed/direction, absolute humidity, relative humidity, snow depth, wind components, soil temperature and volumetric water content (TDT sensors) at various depths, soil heat flux, and multiple soil temperature/moisture channels.
- Hourly data includes: VWC (from CRNS and other sensors) and related meteorological variables.
- Daily data includes: COSMOS_VWC, D86_75m (CRNS effective depth), potential evapotranspiration (PE), snow water equivalent (SWE), daily albedo.
- Special notes:
  - VWC derived from CRNS counts with corrections for atmospheric pressure, humidity, and cosmic-ray intensity; methods include site-specific N0, universal calibration (hmf), and neutron transport modeling, with COSMOS-UK using site-specific N0 calibration.
  - 2018 update adds an extra correction factor Fi to counts to address spurious trends in CRNS data.
  - SWE is estimated from daily neutron counts; albedo thresholding (10:00–14:00 GMT) used to identify snow days, with SWE derived from snow-free counts.

## Data quality and completeness
- Quality controlled via two-stage QC: automated QC tests and daily visual checks.
- QC flags indicate missing data, zero values where not possible, insufficient samples, low power, sensor faults, diagnostic flags, out-of-range values, secondary variable issues, spikes, and other error codes.
- Completeness (per site) is reported for combined Met/Soil variables and for the derived VWC data from CRNS.
- Snow days and SWE estimation can be affected by snow cover, with adjustments described in the methodology.

## Instrumentation and measurement approaches
- Instruments (COSMOS-UK standard, with site variations):
  - Cosmic-Ray Neutron Sensor (CRNS) – Hydroinnova CRS-2000/B and CRS-1000/B for VWC (30-minute counts, then hourly and daily data).
  - Rain gauge – OTT Pluvio.
  - Point soil moisture sensors – Acclima Digital TDT at multiple depths.
  - Soil heat flux plates – Hukseflux HFP01SC (0.03 m depth).
  - Soil temperature sensors – Hukseflux STP01 at multiple depths.
  - Radiometer – Hukseflux NR01 (shortwave and longwave components).
  - Automatic weather station – Rotronic HC2A-S3 within Gill MetPak Pro Base Station.
  - Barometric pressure sensor – Vaisala PTB110.
  - Temperature and humidity sensors – Vaisala HUMICAP HMP155.
  - Wind sensors – 3D sonic anemometer and integrated 2D sonic anemometer (Gill WindMaster/Integrated WindSonic).
  - Snow depth sensor – Campbell SR50A.
  - Snow water equivalent (SWE) – Hydroinnova SnowFox.
  - Data logger – Campbell Scientific CR3000.
- Instrumentation availability varies by site (detailed site-by-site table in Section 7.2).

## Data processing and methodology
- Data are measured on site, logged locally, telemetered hourly to a central system, and subjected to QC.
- Timestamps refer to the end of the 30-minute period for sub-hourly data; daily time stamps refer to the start of the day (00:00) for the preceding 24-hour period (except noted differences for some datasets).
- VWC derivation and depth-specific calculations follow established COSMOS-UK methodologies (Evans et al. 2016; Köhli et al. 2015; Desilets et al. 2010).
- SWE estimation relies on daily counts and snow-albedo thresholds, with further details in Wallbank et al. (2020).
- PE (daily) estimated using Penman-Monteith ( FAO 56, 1998) with inputs from QC-controlled sub-hourly data.

## Data availability and handling missing data
- Missing values are denoted as -9999 in all data files.
- QC flags provide traceability for data removed due to quality issues and allow reconstruction of the failure causes.
- Several data corrections and calibrations updated over time (e.g., VWC calibrations, CRNS count corrections, NMDB data infilling, precipitation calculation changes).

## Changes to data and versions
- Notable data updates and corrections:
  - Jan 2021: D86_75m corrected (CRNS effective depth).
  - Jul 2020: VWC calibration updates; CRNS counts infilled from secondary tubes; NMDB data infilled; 30-minute precipitation calculation updated.
  - Apr 2020: PE updated (method revision; 30-minute values aggregated to hourly and daily).
  - Dec 2019: SWE added; daily albedo added.
- Data reprocessing occurs when improvements are made to ensure consistency across the full time series.

## Author contributions and references
- Primary authorship and data coordination led by S. Stanley; data managers include H. M. Cooper, M. Fry, O. Hitt, O. Swain; instrumentation and field engineering contributors listed; project management and metadata responsibilities distributed among a wide team.
- References cover calibration methods, VWC derivation, and COSMOS-UK methodological background (e.g., Baatz et al. 2014; Zreda et al. 2012; Evans et al. 2016; Wallbank et al. 2020).