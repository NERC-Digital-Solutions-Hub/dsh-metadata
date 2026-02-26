# Daily and sub-daily hydrometeorological and soil data (2013-2018) [COSMOSUK]

- A comprehensive COSMOS-UK data package providing daily and sub-daily hydrometeorological and soil moisture data from 50 sites over 2013–2018.
- Core contents span 201 files including site metadata, sub-hourly data, QC flags, hourly volumetric water content (VWC), and daily derived data.

## Data scope and structure

- Time period and scope
  - 2013–2018 across 50 COSMOS-UK network sites.
- File types (201 files)
  - COSMOS-UK_SiteMetadata_2013-2018.csv: site details and coordinates.
  - Sub-hourly hydro-soil data per site: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018.csv.
  - Sub-hourly QC flags per site: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018_QC_Flags.csv.
  - Hourly hydro-soil data with VWC: COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2018.csv.
  - Daily data set: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2018.csv.
- Missing data
  - Missing values are indicated by -9999.

## Data contents and variables

- Sub-hourly data (30-minute resolution)
  - Variables include radiation components (LWIN, LWOUT, SWIN, SWOUT, RN), precipitation (PRECIP), atmospheric pressure (PA), air temperature (TA), wind (WS, WD), humidity (Q, RH), snow depth (SNOWD_DISTANCE_COR), wind components (UX, UY, UZ), soil heat flux (G1, G2), soil temperature and VWC across multiple TDT sensors (TDT1_TSOIL, TDT1_VWC, etc.), and VWC from TDT sensors at various depths.
  - Snow depth and wind components have site-specific availability; Wytham Woods ends data in 2016.
- Hourly VWC data
  - Derived VWC (COSMOS_VWC) and corrected neutron counts (CTS_MOD_CORR) plus height-distance variables (D86_75m).
- Daily data
  - Derived VWC (COSMOS_VWC), D86_75m, potential evapotranspiration (PE), snow water equivalent (SWE), daily snow day flag (SNOW), and albedo (ALBEDO).
- Derived data notes
  - VWC derived from cosmic-ray neutron sensor (CRNS) counts with corrections for atmospheric pressure, humidity, and cosmic ray intensity ( NMDB reference).
  - Three potential derivation methods; COSMOS-UK uses site-specific N0 calibration with a reference soil moisture value.
  - 2018 reprocessing added an extra correction for fluctuations in incoming cosmic rays, with a site-specific gamma factor (ɣ).

## Data processing and quality control

- Data flow
  - Data are measured on-site, telemetered hourly to CEH Wallingford, and subjected to two QC stages.
- Automatic QC
  - Tests run automatically per variable; data failing tests are flagged and removed.
  - Each test has a unique QC flag; multiple failures sum their flag values for traceability.
- QC flags
  - QC flags are stored in separate files mirroring the data structure, with column names suffixed by _QCFLAG.
- Visual QC
  - Daily review via automatically generated plots for 1- and 10-day time frames.
- Data handling
  - QC’d data are removed; QC flag records capture the reasons for removal.

## Data completeness and coverage

- Completeness metrics
  - Site-level completeness reported for Met (meteorological) and Soil groups, plus derived VWC data completeness.
- VWC completeness
  - Completeness indicators also apply to VWC data derived from the CRNS.

## Instrumentation and site deployment

- Core instruments (COSMOS-UK)
  - Cosmic-Ray Neutron Sensor (CRNS): soil moisture via neutron counts; site-specific calibrations and corrections.
  - Rain gauge: OTT Pluvio 1.
  - Point soil moisture sensors (TDT) with multiple depths for VWC and soil temperature.
  - Soil heat flux plates (Hukseflux HFP01SC).
  - Soil temperature sensors (Hukseflux STP01) at multiple depths.
  - Radiometer system (four-component) for shortwave and longwave components.
  - Automatic weather station (air temp, humidity, and barometric pressure).
  - Wind sensors (3D sonic and integrated 2D sonic equipment).
  - Snow depth sensors (SR50A) and SnowFox-based SWE estimation.
  - Data loggers (Campbell Scientific CR3000).
- Site variability
  - Not all instruments are present at every site; a detailed table lists site-specific instrument installations.

## Methodology highlights

- Sub-hourly data
  - 30-minute measurements, with some variables aggregated as means or sums over the preceding period; timestamps reflect the end of the 30-minute window.
- VWC derivation
  - Corrected neutron counts account for background cosmic rays, altitude, atmospheric pressure, and absolute humidity.
  - Correction approaches include site-specific N0 calibration; main methods include site-specific, universal (hmf), and neutron transport modelling. COSMOS-UK adopts site-specific N0 calibration with adjustments for structural water and soil organic carbon.
  - 2018 reprocessing introduces a site-specific ɣ factor to stabilize trends in VWC.
- Daily data derivation
  - Daily VWC created by averaging hourly corrected counts and applying the VWC equation.
  - SWE estimation uses snow albedo-based snow-day logic and the difference between snow-free counts and observed counts; SWE and D86 are derived from daily values.
  - PE (potential evapotranspiration) computed via Penman-Monteith using RN, G (mean of G1 and G2), TA, RH, WS, and PA; negative sub-daily PE values are discarded.
  - Daily timestamps refer to the start of the day (00:00 GMT) and cover the preceding 24 hours, differing from sub-daily data timestamps.

## Changes to data (releases and updates)

- Jul 2020: VWC calibration values updated; CRNS counts infilled from secondary tube; NMDB data infilled; 30-minute precipitation updated (non-real-time version used).
- Apr 2020: PE methodology revised; shift to 30-minute values aggregated to hourly/daily.
- Dec 2019: SWE added; daily albedo added (based on SWIN/SWOUT for mid-day hours).

## Access and references

- Data hosted and documented via the COSMOS-UK portal and the NERC Environmental Information Data Centre (EIDC).
- Supports the COSMOS-UK User Guide for additional methodological details and updates.
- Key references for methods include Baatz et al. (2014), Franz et al. (2012, 2013), Zreda et al. (2012), Evans et al. (2016), Köhli et al. (2015), and Wallbank et al. (2020, in prep).