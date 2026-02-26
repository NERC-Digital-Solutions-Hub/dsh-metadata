# Daily and sub-daily hydrometeorological and soil data (2013-2019) [COSMOS-UK].

- Purpose and scope
  - Supporting documentation for COSMOS-UK, documenting daily and sub-daily hydrometeorological and soil moisture data from 51 COSMOS-UK sites, covering 2013–2019.
  - Created to enable environmental monitoring, analysis, and policy-relevant decision making; data curated for quality, openness, and traceability.

- Data coverage and structure
  - Total of 208 files comprising:
    - COSMOS-UK sites metadata
    - Sub-hourly hydrometeorological and soil data (per site)
    - Sub-hourly QC flags (per site)
    - Sub-hourly metadata (per site)
    - Hourly hydrometeorological and soil data (including volumetric water content, VWC)
    - Hourly metadata
    - Daily hydrometeorological and soil data (including VWC, potential evapotranspiration, SWE)
    - Daily metadata
  - Data periods: October 2013 to December 2019.
  - Key data components include VWC derived from cosmic-ray neutron sensor (CRNS) data, meteorological variables, soil sensors, and snow-related metrics.

- Data processing and methodology
  - Data collected on-site by various instruments, logged locally, telemetered hourly to a central system, then quality controlled.
  - Aggregation and timing:
    - Sub-hourly data (30-minute intervals) with timestamps at the end of each 30-minute period.
    - Hourly data derived from 30-minute records; daily data derived from hourly values.
  - Quality control (QC)
    - Two-stage QC: automated QC tests applied by processing scripts, plus daily visual inspection of plots.
    - QC flags: non-zero values indicate failures; flags are additive to yield a unique final value per data point.
    - QC flags stored in separate files with a _QCFLAG suffix; structure mirrors data files with _QCFLAG appended to column names.

- Derived variables and key methodologies
  - Sub-hourly data include primary meteorology (radiation, precipitation, temperature, humidity, pressure, wind) and soil variables (temperatures, volumetric water content at various depths, soil heat flux).
  - VWC derivation from CRNS:
    - Corrected neutron counts account for background cosmic rays, altitude, atmospheric pressure, and absolute humidity.
    - Three potential derivation methods; COSMOS-UK uses site-specific calibration with a reference soil water content.
    - Corrections for lattice water and soil organic carbon applied; 2018 introduces an additional correction for cosmic-ray flux fluctuations.
  - Daily VWC, PE (Penman-Monteith evapotranspiration), and SWE (snow water equivalent) derived from sub-hourly data:
    - Snow detection using daily albedo (10:00–14:00 GMT) to identify snow days; SWE estimated from counts relative to snow-free conditions.
    - PE calculated daily via Penman-Monteith using RN, G (soil heat flux), TA, RH, WS, PA.
  - Snow-related notes: snow can bias VWC on snowy days; SWE method described and referenced.

- Completeness and data quality
  - Completeness varies by site and variable; section 6 provides completeness percentages for met (precipitation, humidity, temperature, pressure, radiation, wind), soil (soil heat flux, soil temperature, TDT-based VWC), and VWC derived from CRNS.
  - Data quality controlled to remove data failing QC; QC flags document specific failures and their causes.

- Instrumentation and site variability
  - Instruments used (as summarized in Section 7):
    - Cosmic-Ray Neutron Sensors (CRNS) – Hydroinnova CRS-2000/B and CRS-1000/B
    - Rain gauges (OTT Pluvio)
    - Time-domain transmissometry soil moisture sensors (TDT) and associated temperature sensors
    - Soil heat flux plates (Hukseflux HFP01SC)
    - Soil temperature sensors (Hukseflux STP01)
    - Radiometers (Hukseflux NR01)
    - Automatic weather stations (Rotronic HC2A-S3)
    - Barometric pressure sensors (Vaisala PTB110)
    - Temperature and humidity sensors (Vaisala HUMICAP HMP155)
    - 3D and integrated 2D sonic anemometers
    - Snow depth sensors (Campbell SR50A)
    - Snow water equivalent sensors (Hydroinnova SnowFox)
    - Data logger (Campbell Scientific CR3000)
  - Not all instruments are deployed at every site; Section 7.2 provides site-by-site instrument presence/absence details (i.e., some sites lack certain sensors or have them installed differently).

- Data changes and version updates
  - Routine reprocessing when improvements are made; major changes include:
    - Jan 2021: update to D86_75m (depth of CRNS water content measurement)
    - Jan 2021: correction to effective CRNS depth calculation
    - Jul 2020: VWC calibration values updated; CRNS counts infilled from secondary tubes and NMDB data infilled; 30-minute precipitation calculation updated
    - Apr 2020: PE calculation updated (method revision; 30-minute values formed and then aggregated)
    - Dec 2019: SWE added; daily albedo added
  - Documentation notes all changes and their impact on time series consistency.

- Access, governance, and authorship
  - Data are described and archived in the NERC Environmental Information Data Centre (EIDC) and publicly accessible.
  - Document lists author contributions (Stanley as primary author; data managers; calibration/maintenance teams; site selection/negotiation; project management; metadata and data presentation).
  - Metadata and QC processes are designed to support data governance, traceability, and reproducibility for monitoring and policy-relevant analyses.

- Practical considerations for users (policy and monitoring perspective)
  - Data are designed to support environmental health monitoring and decision-making with a transparent QC framework and extensive metadata.
  - Public sharing of underlying data is supported, though some data handling considerations (e.g., decommissioned sites, snow biases) require careful interpretation.
  - For policy and management use, the dataset provides a rich, standardized, traceable record of hydrometeorological and soil moisture dynamics across multiple UK sites, with documented instrumentation, data processing, and revision history.