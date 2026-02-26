# Daily and sub-daily hydrometeorological and soil data (2013-2018) [COSMOS-UK]

- The COSMOS-UK dataset provides 50-site coverage of hydrometeorological and soil moisture time series from 2013 to 2018, in multiple resolutions (sub-hourly, hourly, daily) across a total of 201 CSV files plus site metadata.
- Intended for GIS-informed data products: enables map-based visualization and exploration of regional hydrology and soil moisture dynamics.

## Data files and structure

- 201 files total, organized by site and data type:
  - COSMOS-UK_SiteMetadata_2013-2018.csv
    - Site-level details: site name/ID, start/end dates, coordinates (EASTING, NORTHING in OSGB36; LATITUDE, LONGITUDE in WGS84), soil type, bulk density, soil organic carbon, land cover.
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018.csv
    - Sub-hourly (30-minute) hydrometeorological and soil data per site (−9999 for missing); includes radiation components, net radiation, precipitation, atmospheric pressure, air temperature, relative humidity, wind (speed and direction), soil temperature and VWC sensors, snow depth, and multiple VWC measurements.
    - Notable site-specific sensor availability (e.g., snow depth measured only at some sites; some wind components missing at certain sites; Wytham data ends 2016).
  - COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018_QC_Flags.csv
    - QC flags for sub-hourly data; mirrors SH file structure with _QCFLAG suffix; flags encode automatic QC test outcomes and can be combined to identify data failures.
  - COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2018.csv
    - Hourly VWC data derived from CRNS-corrected counts; includes COSMOS_VWC and CTS_MOD_CORR plus depth-related VWC (D86_75m).
  - COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2018.csv
    - Daily aggregates: COSMOS_VWC (daily average), D86_75m, PE (potential evapotranspiration), SWE, SNOW (snow day indicator), ALBEDO.
- VWC derivation and related data are described in detail in Section 4 and Section 5, including correction steps and methods for converting corrected neutron counts to soil moisture.

## Sub-hourly data (30-minute resolution)

- Variables (per site) include:
  - Radiation (incoming/outgoing longwave and shortwave), net radiation
  - Precipitation, atmospheric pressure, air temperature, relative humidity
  - Wind speed and direction; X/Y/Z wind components
  - Humidity-related variables, soil temperature and VWC from multiple TDT sensors at various depths
  - Snow depth (where measured), heat flux (G1, G2)
- Data handling:
  - Missing values denoted by -9999
  - Data are telemetered hourly to a central CEH system and pass two QC stages
  - Some variables are not recorded at all sites; section notes specific sensor gaps
- Time stamps reflect the end of the 30-minute period (e.g., 12:30 data cover 12:00–12:30)

## Hourly volumetric water content (VWC)

- Data derived from CRNS counts corrected for:
  - Background cosmic ray intensity (via a Jungfraujoch reference site)
  - Site altitude, atmospheric pressure, and absolute humidity
- Methods to derive VWC include site-specific N0 calibration, universal hydrogen mole fraction method, and neutron transport modelling; COSMOS-UK uses site-specific N0 calibration with corrections for lattice/bound water and soil organic carbon
- 30-minute counts are aggregated to hourly totals, then converted to VWC; D86 depth values are computed from hourly VWC data
- VWC data are complemented by derived distance-weighted measurements (D86 at specified distances)

## Daily data (VWC, PE, SWE)

- Daily VWC derived from daily average corrected counts
- SWE estimated from daily count-derived snow-free VWC during snow days
- PE computed using Penman–Monteith using sub-hourly inputs (RN, G1/G2, TA, RH, WS, PA)
- Snow days detected via albedo thresholds (10:00–14:00 GMT) and used to flag days with detectable snow
- DATE_TIME in daily data marks 00:00 of the day and represents the preceding 24-hour period

## Completeness and data quality

- Completeness is summarized per site for Met (meteorological), Soil (soil temp, soil heat flux, TDT VWC), and VWC (CRNS-derived) data; exact percentages are provided in Table 6.1
- Data quality control (QC):
  - Two-stage QC: automated tests (e.g., zero data, too few samples, low power, sensor fault, diagnostic, out of range, secondary variable, spike, error codes) and daily visual inspection
  - QC flags recorded in dedicated QC flag files; flags are additive and traceable to specific tests
  - If data fail tests, they are removed from the data file but the QC flag records the reasons
- Wytham data ends on 01/10/2016; other sites have varying sensor availability throughout the period

## Instrumentation

- Major instrument categories (with notes on site variations):
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (Hydroinnova CRS-2000/CRS-1000/B)
  - Rain gauge: OTT Pluvio 1
  - Point soil moisture sensors using time-domain transmissometry (TDT) with multiple depths
  - Soil heat flux plates (Hukseflux HFP01SC)
  - Soil temperature sensors (Hukseflux STP01) at multiple depths
  - Radiometer suite (four-component radiometer; HR-based net radiation)
  - Automatic weather station and barometric/temperature/humidity sensors (Rotronic HC2A-S3; Vaisala PTB110; HMP155)
  - 3D and 2D sonic anemometers for wind
  - Snow depth sensors (Campbell SR50A) and SnowFox-based SWE
  - Campbell Scientific CR3000 data loggers
- Section 7.2 lists site-by-site instrumentation variations (not all sites have every instrument)

## Changes to data (since previous release)

- Jul 2020: VWC calibration values updated; CRNS counts infilled from secondary tube; NMDB data infilled; 30-minute precipitation updated (non-real-time version)
- Apr 2020: PE calculation methodology revised; switch to 30-minute values and subsequent aggregation
- Dec 2019: SWE added; daily albedo added (based on SWIN/SWOUT)
- Other ongoing data processing improvements and updates described in the changes note

## Author contributions and references

- Documentation and data management led by S. Stanley and colleagues; data managers and calibration/maintenance teams detailed
- Key references cover calibration and methods for cosmic-ray soil moisture, VWC derivation, and related hydrology research (e.g., Baatz et al., Evans et al., Zreda et al., Franz et al.)

## Practical GIS usage notes

- Use COSMOS-UK_SiteMetadata_2013-2018.csv to plot site locations (OSGB36 coordinates for map placement; convert to desired CRS if needed)
- Join sub-hourly, hourly, and daily data to the site metadata via SITE_ID for spatially explicit analysis
- Use QC flags to filter unreliable data before visualization or spatial aggregation
- For VWC mapping, combine hourly/daily COSMOS_VWC with depth-specific VWC (TDT-based sensors) and CRNS-derived measurements
- Be aware of sensor coverage gaps by site and time (e.g., snow depth availability, decommissioned sites, and site-specific sensor configurations) when designing maps and time-series visualizations