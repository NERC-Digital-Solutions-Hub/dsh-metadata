# COSMOS-UK: Daily and sub-daily hydrometeorological and soil data (2013-2018) [COSMOSUK]

- The dataset provides daily and sub-daily hydrometeorological and soil moisture time series from 50 COSMOS-UK sites spanning 2013–2018, assembled to support environmental monitoring and policy evaluation.
- Supporting documentation and metadata accompany the data, with data and methods regularly updated (versioning and reprocessing when improvements are made).

## Data structure and content

- Comprises 201 files in total, organized into:
  - COSMOS-UK_SiteMetadata_2013-2018.csv (site metadata)
  - Sub-hourly hydro-soil data by site (COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018.csv)
  - Sub-hourly QC flags per site (COSMOS-UK_<SITE_ID>_HydroSoil_SH_2013-2018_QC_Flags.csv)
  - Hourly hydro-soil data with volumetric water content (COSMOS-UK_<SITE_ID>_HydroSoil_Hourly_2013-2018.csv)
  - Daily hydro-soil data with VWC, potential evapotranspiration (PE), and snow water equivalent (SWE) (COSMOS-UK_<SITE_ID>_HydroSoil_Daily_2013-2018.csv)
- Temporal resolution:
  - Sub-hourly data at 30-minute intervals
  - Hourly data (VWC-derived)
  - Daily data (including daily averages for some variables)
- Spatial coverage:
  - 50 COSMOS-UK sites with geographic coordinates, soil properties, and land cover information.

## Variables and data types

- Sub-hourly variables (per Table 3.1 onward): radiation (incoming/outgoing longwave and shortwave), net radiation (RN), precipitation (PRECIP), atmospheric pressure (PA), air temperature (TA), relative humidity (RH), wind speed/direction (WS, WD, UX, UY, UZ), absolute humidity (Q), snow depth (SNOWD_DISTANCE_COR), wind components, soil heat flux (G1, G2), soil temperature (TDT sensors), volumetric water content (VWC) at various depths (TDT1_TSOIL, TDT1_VWC, etc.).
- Hourly data: corrected cosmic-ray neutron counts (CTS_MOD_CORR) and COSMOS_VWC (soil moisture), plus depth-specific metrics (D86_75m).
- Daily data: COSMOS_VWC (daily average), D86_75m, PE (potential evapotranspiration), SWE (snow water equivalent, mid-day value), SNOW flag (snow day), ALBEDO (derived from SWIN/SWOUT).
- Derived metrics and data products:
  - VWC derived from corrected neutron counts using one of several calibration approaches (COSMOS-UK uses site-specific N0 with field calibration).
  - SWE estimated from snow-free reference counts and snow depth indicator.
  - PE calculated via Penman-Monteith (using RN, G, TA, RH, WS, PA).

## Methodology and data processing

- Data collection and on-site logging:
  - Instruments feed data to data loggers on site; some measurements are instantaneous, others are aggregated over 30 minutes.
  - Data are telemetered hourly to a central CEH Wallingford system.
- Quality control (QC):
  - Two-stage QC workflow:
    1) Automated QC tests applied by a processing script; failing data are flagged and removed.
    2) Daily visual inspection using plots across 1- and 10-day windows.
  - QC flags:
    - Each automated test has a unique flag value; if data fail multiple tests, flag values are added to produce a unique final value.
    - QC flags are stored in site-specific QC_flag CSVs mirroring the data structure, with column names suffixed by _QCFLAG.
  - Description of tests and flag values (e.g., Zero data, Too few samples, Low power, Sensor fault, Diagnostic, Out of range, Secondary variable, Spike, Error codes) with associated bitwise values (1, 4, 8, 16, 32, 64, 128, 512, 1024).
- Data provenance and governance:
  - Data are processed, quality-assured, and then presented via reports, charts, and dashboards; underlying data are shared where appropriate.
  - A comprehensive metadata framework accompanies the data to support traceability and reuse.

## Derived variables and data products

- Sub-hourly to hourly VWC:
  - VWC derived from CRNS neutron counts, corrected for background cosmic ray intensity (via reference site NMDB data) and local atmospheric conditions (PA, Q).
  - Correction and calibration steps described, including site-specific N0 calibration coefficients and adjustments for structural water and soil organic carbon.
- Daily products:
  - COSMOS_VWC (daily), D86_75m (depth-adjusted), PE (Penman-Monteith), SWE, SNOW, and ALBEDO (derived from SWIN/SWOUT).
- Snow detection and SWE estimation:
  - Snow days identified using albedo thresholds (10:00–14:00 GMT mean albedo > 50% marks snow onset; < 35% marks end).
  - SWE estimated by comparing snow-free counts to observed counts (Method 1 in Wallbank et al., 2020).

## Metadata and provenance

- Site metadata includes:
  - SITE_NAME, SITE_ID, start/end dates, coordinates (E/N, lat/long in OSGB36 and WGS84), soil type, bulk density, soil organic carbon, and land cover.
- Instrumentation inventory:
  - Detailed descriptions of instruments used (CRNS, rain gauge, TDT soil moisture sensors, soil heat flux plates, soil temperature sensors, radiometer, automatic weather station, barometric pressure sensor, temperature/humidity sensors, wind sensors, snow depth and SWE sensors, data loggers).
  - Not all instruments are present at every site; Section 7.2 lists site-specific instrumentation.
- Versioning and updates:
  - Data reprocessing occurs when improvements are identified; updates have included VWC calibration, infilling of missing data from secondary tubes, NMDB corrections, precipitation updates, and refinements to PE and SWE calculations.

## Completeness and data quality

- Completeness assessments are provided per site for combined meteorological (Met) and soil data, and for the derived VWC from the CRNS.
- Completeness tables address data coverage across the study period (October 2013–December 2018) and highlight gaps due to instrument availability, maintenance, or QC removals.

## Instrumentation and site details

- COSMOS-UK uses a suite of instruments with documented specifications and operational ranges.
- Instrumentation has evolved over time; Section 7.2 details site-by-site variations in instrument installation.

## Data governance, access, and reuse

- Data are organized and documented for reuse by researchers and policymakers, with data and QC metadata hosted at an environmental information data centre.
- The documentation emphasizes openness, reproducibility, and the ability to trace data through QC flags to specific tests.

## Changes to data and version history

- July 2020 updates:
  - VWC calibration values updated; CRNS counts infilled from secondary tubes; NMDB data infilled; 30-minute precipitation updated; PE recalculated with revised method.
- December 2019 updates:
  - SWE added; snow days derived from albedo; mid-day SWE estimation introduced.
- Other ongoing improvements:
  - Daily albedo addition; ongoing reprocessing as data volumes grow and calibration methods improve.

## Author contributions

- Stanely (lead author) and a team of data managers, calibration specialists, site engineers, field staff, metadata coordinators, and project managers contributed to data curation, instrument maintenance, site selection, and data presentation.

## Implications for monitoring-framework authors

- Establish clear data structure from the outset (sub-hourly, hourly, and daily data with corresponding QC flags and metadata).
- Implement robust, two-stage QC with traceable flagging to ensure data integrity and facilitate auditing.
- Maintain comprehensive metadata (site characteristics, coordinates, soil properties) to support interpretation and reuse.
- Document data processing pipelines, including calibration, corrections (e.g., CRNS corrections), and method choices for derived variables (e.g., VWC, SWE, PE).
- Provide transparent data lineage and versioning; reprocess entire time series when improvements are made.
- Address data accessibility barriers by sharing underlying data and QC information; manage metadata gaps proactively.
- Capture instrumentation changes and site-specific deployments to aid comparability over time.
- Bundle derived products (e.g., SWE, albedo, PE) with clear methodology to support monitoring frameworks relying on standardized indicators.
- Include explicit limitations (e.g., snow cover affecting VWC estimates) and mitigation approaches (e.g., snow-detection thresholds, corrections).
- Ensure data governance processes align with openness, reproducibility, and long-term stewardship.