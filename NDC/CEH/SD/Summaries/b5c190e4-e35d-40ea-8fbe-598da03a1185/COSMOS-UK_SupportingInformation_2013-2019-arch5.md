# COSMOS-UK Daily and sub-daily hydrometeorological and soil data (2013-2019) [COSMOSUK]. NERC Environmental Information Data Centre

- A comprehensive COSMOS-UK dataset (2013–2019) comprising sub-hourly (30-minute), hourly, and daily hydrometeorological and soil moisture data from 51 sites, plus site metadata.
- Total of 208 files including site metadata, sub-hourly/hourly/daily data, and corresponding QC metadata.
- Primary purpose: enable robust data governance, discovery, sharing, and reuse by researchers and practitioners.

## Data structure and contents

- Sub-hourly data and QC
  - Data: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019.csv
  - QC flags: COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2019_QC_Flags.csv
  - Metadata: COSMOS-UK_HydroSoil_SH_2013-2019_Metadata.csv
- Hourly data
  - Data: COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2019.csv
  - Metadata: COSMOS-UK_HydroSoil_Hourly_2013-2019_Metadata.csv
- Daily data
  - Data: COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2019.csv
  - Metadata: COSMOS-UK_HydroSoil_Daily_2013-2019_Metadata.csv
- Site metadata
  - COSMOS-UK_SiteMetadata_2013-2019.csv
- Overall: 51 sites with 30-minute, hourly, and daily products; data cover October 2013–December 2019 (end dates vary for decommissioned sites).

## Data collection, processing and quality control

- Instrumentation (not all instruments present at every site; main types include):
  - Cosmic-Ray Neutron Sensor (CRNS) for soil moisture (VWC) and related depths
  - Rain gauge (OTT Pluvio)
  - Time-domain transmissometry (TDT) soil moisture sensors at multiple depths
  - Soil heat flux plates
  - Soil temperature sensors (multiple depths)
  - Radiometer and net radiation components
  - Automatic weather station (temperature, humidity, etc.)
  - Barometric pressure sensor
  - Wind (3D sonic and integrated 2D sonic anemometers)
  - Snow depth and Snow Water Equivalent (SWE) sensors
  - Micrologger for data logging
- Data capture and aggregation
  - Measurements captured as instantaneous or 30-minute averages; 30-minute periods end timestamps mark the end of the interval.
  - Data telemetered hourly to a central system; subjected to two QC stages:
    - Automatic QC via processing script (flags assigned per variable; flags accumulate if multiple tests fail)
    - Daily visual inspection of plots
  - Missing values coded as -9999.
- Derived products and methods
  - Volumetric Water Content (VWC) derived from corrected CRNS counts using site-specific N0 calibration and corrections for lattice water and soil organic carbon.
  - Snow days and Snow Water Equivalent (SWE) estimated from albedo thresholds and CRNS counts (method described in Wallbank et al., 2020).
  - Daily Potential Evapotranspiration (PE) calculated with Penman-Monteith using sub-hourly inputs (RN, G, TA, RH, WS, PA); negative values ignored for daily totals.
  - 2018 update adds an additional correction factor Fi to CRNS counts to account for geomagnetic fluctuations and reference-counter differences.
- Data quality and flags
  - QC flags are stored in separate files with suffixes “_QCFLAG” appended to column names.
  - Flag values correspond to specific failure tests (e.g., missing data, zero values, too few samples, low power, sensor faults, out-of-range, spikes, etc.).
  - The QC system enables traceability of failures to exact tests via unique flag compositions.

## Metadata, provenance and standards

- Metadata files accompany each data product, detailing variable names, units, aggregation, and notes on each variable (e.g., measurement depths, sensors, and processing steps).
- Site metadata include coordinates (OSGB36 and WGS84 references), soil properties (bulk density, soil organic carbon, lattice water), land cover, soil type, and related notes.
- Data provenance is anchored in the COSMOS-UK project (Stanley et al. 2021) with methodologies described in Evans et al. 2016 and related literature; full documentation and user guide are available via the COSMOS-UK site.
- Data provider and maintainer roles are defined; data are stored and disseminated through the NERC Environmental Information Data Centre.

## Completeness and limitations

- Completeness varies by site and variable group (Met: precip, humidity, temperature, pressure, radiation, wind; Soil: soil heat flux, soil temperature, TDT-based VWC).
- Volumetric water content (VWC) data are derived from CRNS and (for daily) CRNS-based methods, with known snow-pack sensitivity on VWC estimates during snow days.
- Some sensors are not installed at all sites; snow depth measurements are limited to specific sites.
- Daily timestamps reflect the start of the day (00:00) and summarize the preceding 24-hour period; sub-daily datasets timestamp end or beginning as described per dataset.

## Instrumentation overview and site coverage

- Detailed inventories provided; not all instruments present at every site (e.g., certain wind components, snow sensors, or automatic weather station configurations may be absent at some sites).
- Instrument types include:
  - CRNS (Hydroinnova CRS-2000/B and CRS-1000/B)
  - OTT Pluvio rain gauge
  - Acclima TDT soil sensors
  - Hukseflux HFP01SC, STP01 for soil heat flux and temperature
  - Hukseflux NR01 radiometer
  - Rotronic HC2A-S3 weather station components
  - Vaisala PTB110 barometric sensor
  - Vaisala HUMICAP HMP155 for temp/humidity
  - Gill WindMaster 3D, WindSonic for wind measurements
  - Campbell SR50A snow depth sensor
  - Hydroinnova SnowFox SWE sensor
  - Campbell CR3000 data logger
- Full instrumentation details, including site-by-site variations, are documented in the 7.2 instrument table.

## Data updates, versioning and changes

- Data processing evolves over time; major changes have included:
  - Jan 2021: D86_75m updated for CRNS effective depth calculation.
  - Jul 2020: VWC calibration values updated; CRNS counts infilled from secondary tubes; NMDB data infilled; 30-minute precipitation calculation updated; PE method revised (and aggregation changes to hourly/daily).
  - Dec 2019: SWE added; daily albedo added.
- When updates occur, the full time series is reprocessed to maintain consistency and integrity.

## Access, governance and reuse considerations

- Data are hosted in the NERC Environmental Information Data Centre under the COSMOS-UK project framework.
- Supporting documentation and user guides are publicly available; the data are intended to be discoverable and reusable by researchers, with clear metadata, provenance, and QC information.
- Users should reference Stanley et al. (2021) and related methodological papers for processing steps and calibration details; acknowledge data stewardship and publication citations as appropriate.
- -9999 designates missing data; QC flags provide traceability to data points removed due to quality checks.

## Known issues and caveats

- Snow cover can bias VWC estimates; SWE estimation relies on albedo thresholds and CRNS-derived counts.
- Site-specific calibration (N0) and corrections introduce uncertainties in VWC estimates; not all sites may have identical sensor configurations across the entire period.
- Some sites have incomplete sensor sets or decommissioned data (e.g., Wytham Woods, Redmere end dates); completeness varies by site.
- Data are provided with comprehensive QC, but researchers should review QC flags relevant to their analyses and consider reprocessing if integrating with other data sources.

## References and additional information

- Stanly et al. 2021; Evans et al. 2016; Wallbank et al. 2020; Baatz et al. 2014; Franz et al. 2012/2013; Köhli et al. 2015; Desilets et al. 2010; Zreda et al. 2012; FAO 1998.