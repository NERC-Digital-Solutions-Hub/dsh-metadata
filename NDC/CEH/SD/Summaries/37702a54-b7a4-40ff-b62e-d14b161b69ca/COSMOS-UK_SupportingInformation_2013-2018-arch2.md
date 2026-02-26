# Daily and sub-daily hydrometeorological and soil data (2013-2018) [COSMOSUK]

- Scope and purpose
  - Narrates a long-term dataset of hydrometeorological and soil moisture measurements from 50 COSMOS-UK sites, covering 2013–2018.
  - Aims to provide standardized, quality-controlled time series to monitor environmental conditions and support evaluation of environmental health and policy performance over time.

- Data structure and contents
  - Total of 201 files, organized into:
    - COSMOS-UK SiteMetadata_2013-2018.csv (site locations, soil type, land cover, etc.)
    - Sub-hourly hydro-soil data (SH) per site
    - Sub-hourly QC flags per site
    - Hourly hydro-soil data (including volumetric water content, VWC)
    - Daily hydro-soil data (including VWC, potential evapotranspiration, SWE)
  - Key variables include: radiation (incoming/outgoing longwave and shortwave, net radiation), precipitation, atmospheric pressure, air temperature, relative humidity, wind, VWC at various depths, soil temperatures, soil heat flux, SNOW/ALBEDO, and SWE via CRNS-derived estimates.

- Data collection and processing
  - On-site instrumentation (see Instrumentation section) includes:
    - Cosmic-Ray Neutron Sensor (CRNS) for VWC
    - Rain gauge, soil moisture sensors (TDT), soil heat flux plates, multi-depth soil temperature sensors
    - Radiometer and automatic weather station (temperature, humidity, pressure)
    - 3D/2D sonic anemometers for wind
    - Snow depth sensors and SnowFox-based SWE estimation
    - Campbell CR3000 micrologger for data capture
  - Data handling
    - Data logged at 30-minute intervals (some instantaneous, some aggregated) and telemetered hourly to CEH Wallingford
    - Timestamps refer to end of the aggregation period (e.g., 12:30 represents data 12:00–12:30)
  - Quality control
    - Two-stage QC: automated QC tests and daily visual inspection
    - QC flags are stored in separate QC_FLAG datasets; data failing QC are flagged and removed
    - QC flags are additive to yield a unique final flag per data point; -9999 indicates missing values

- Quality control details
  - Automatic QC tests cover: zero data, too few samples, low power, sensor fault, diagnostic flags, out of range, secondary variable consistency, spikes, and error codes
  - Flag values are combined to produce a unique final QC flag (e.g., 72 could indicate multiple failing tests)
  - QC flag files mirror the data files but with _QCFLAG appended to column names

- Completeness and data quality
  - Completeness assessed per site across Met (meteorological) and Soil groups; VWC completeness is separately reported
  - Completeness varies by site and variable; a dedicated completeness section (Table 6.1) documents site-level data coverage

- Completeness and limitations of derived VWC
  - VWC is derived from CRNS, corrected for background cosmic ray intensity, altitude, atmospheric pressure, and absolute humidity
  - VWC uses one of three methods (site-specific N0, universal calibration, neutron transport modeling); COSMOS-UK adopts the site-specific N0 approach
  - 2018 update introduced a site-specific gamma correction to remove spurious trends in VWC; counts are corrected and reprocessed

- Daily data specifics
  - Daily VWC is the daily average of hourly corrected counts transformed to VWC
  - D86_75m (nearest CRNS-derived depth) is daily averaged
  - PE (potential evapotranspiration) calculated via Penman-Monteith using RN, G, TA, RH, WS, PA
  - SWE is estimated from CRNS-derived counts during snow events
  - Snow days identified using albedo thresholds (10:00–14:00 GMT); 50% threshold for snow onset, 35% for end
  - Date stamps in daily data refer to the start of the day (00:00) and cover the preceding 24-hour period

- Changes to data and methodology
  - Ongoing improvements and reprocessing of full time series when changes occur
  - Notable updates:
    - Jul 2020: VWC calibration values updated; CRNS counts infilled across primary/secondary tubes; NMDB data infilled; 30-min precipitation updated
    - Apr 2020: PE methodology revised; 30-min values calculated and aggregated to hourly/daily
    - Dec 2019: SWE added; daily albedo added
  - These changes aim to improve accuracy and consistency across the full dataset

- Completeness and site coverage
  - The document provides tabulated site-level completeness (Met, Soil, and VWC) for the October 2013–December 2018 window
  - Completeness reflects the proportion of valid observations across the defined variable groups

- Instrumentation details
  - COSMOS-UK uses a suite of instruments; details cover sensor types, models, and configuration
  - Not all instruments are present at every site; installation varies by site
  - Instrumentation is described comprehensively (CRNS, rain gauge, soil moisture sensors, heat flux plates, soil temperature sensors, radiometer, automatic weather station, pressure sensor, wind sensors, snow sensors, SWE, micrologger)

- Instrumentation at COSMOS-UK sites
  - A site-by-site table lists which instruments are installed at each site (e.g., presence/absence of 3D/2D sonic anemometers, automatic weather station, barometric sensor, etc.)
  - Notes indicate sites installed on pre-existing towers and any calibration caveats (e.g., rain gauge funnel corrections)

- Author contributions and references
  - Authors and data management teams are documented; data presentation, analysis, and interpretation responsibilities are listed
  - References include foundational works on cosmic-ray soil moisture methods, calibration approaches, and related methodology

- Access and purpose for analysts
  - Data are stored and made available via the NERC Environmental Information Data Centre
  - The dataset supports cross-site comparisons, trend analysis, and policy-relevant environmental health assessments by providing a consistent, quality-controlled time series of meteorological and soil moisture variables, including derived SWE and PE

- Practical notes for analysts
  - Be aware of site-specific completeness and QC flags when using the data for trend analyses
  - Consider the 2018 reprocessing and subsequent 2020 changes to VWC calibration and CRNS infilling when selecting data periods
  - Use the QC flag datasets to filter questionable observations and understand data provenance and processing history