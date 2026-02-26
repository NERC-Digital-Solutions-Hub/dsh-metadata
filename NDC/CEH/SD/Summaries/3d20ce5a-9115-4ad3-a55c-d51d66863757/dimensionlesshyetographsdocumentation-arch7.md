# Hyetographs and statistics of annual-maximum rainfall events in Great Britain, from historical rain gauge records Supporting Documentation

- Overview
  - Describes the collection, processing, and formatting of rainfall data to create a dataset of annual-maximum (AMAX) rainfall events in Great Britain, based on sub-hourly rain gauge records.
  - Core outputs include hyetographs (dimensionless and cumulative), AMAX values across multiple durations, and statistical properties for ~70,000 events.
  - Dataset supports analysis of temporal rainfall characteristics and climatology relevant to GIS-based mapping and decision-support.

- Data scope and content
  - AMAX values across multiple durations (ranging from 5 minutes to 24 hours, with intermediate 10 and 15 minutes; includes half-hourly and hourly-resolution derivations as applicable).
  - Dimensionless hyetographs for approximately 70,000 AMAX events.
  - Statistical properties for each AMAX event.
  - Three main data files: AMAX values, hyetographs, and associated metadata/statistics.

- Data sources and collection
  - Original rainfall data from Environment Agency (EA), Natural Resources Wales (NRW), and Scottish Environment Protection Agency (SEPA) up to summer 2018.
  - Data available as mixed temporal resolutions (15-minute accumulations or tip records) and mixed measurement resolutions (0.2 mm per tip, some at 0.5 mm).
  - Records were unified by matching coordinates, IDs, and names; no unified start/end date due to value of long-running records.
  - Approximately 27,600 station-years of data compiled; most gauges have around 20.5 years of data.

- Methods and quality control
  - Quality Control (QC)
    - Two automated QC steps: original data aggregated to hourly and evaluated with GSDR-QC (global Sub-Daily Rainfall QC) adapted for the UK; then re-checked at original resolution with SHQC.
    - GSDR-QC tests include station metadata checks, 25 time-series tests, and a rule-base; ETCCDI indices used as reference datasets; GPCC data not used due to access restrictions.
    - UK-specific modifications to GSDR-QC: downscaled 1-hour world record values to UK records; replaced Rx1day with UK 24-hour rainfall record; adjusted thresholds and streak criteria to reflect UK rainfall.
    - SHQC provides sub-hourly-specific threshold checks, including tip-time data where available.
  - Independent rainstorm identification
    - Rainstorms identified using fixed-duration AMAX values (5, 10, 15 minutes; 0.5h to 24 hours); separation into independent events uses a gauge-specific minimum time between events, based on statistical independence (exponential inter-arrival times).
    - At the gauge level, multiple AMAX values may occur within a single rainstorm; care taken to remove duplicates across durations.
    - Final dataset: ~70,000 independent rainfall events containing ~200,000 AMAX values.

- Data format and file structure
  - UK_AMAX.csv
    - contains all 207,084 AMAX values.
    - Key fields: Event_id, Burst_id, AMAX[mm], Station_id, Datetime, Longitude, Latitude, etc.
  - UK_AMAX_Hyetographs.csv
    - contains 72,094 cumulative rainfall profiles aligned to AMAX values.
    - Key fields: Datetime, Cum_rain, Event_id, Burst_id, etc.
  - UK_AMAX_Hyetographs_Statistics.csv
    - contains metadata and simple profile statistics.
    - Key fields: Longitude, Latitude, Timestep (5 or 15 minutes), Event_duration (minutes), Event_magnitude (mm), Station_id, etc.
  - Key identifiers and structure
    - Event_id encodes station, AMAX duration, and end datetime; may include a part indicator for compound AMAX events.
    - Burst_id identifies a single AMAX value (duration-specific) within an event.
    - Event_id part value indicates compound AMAX when non-zero.

- Geographic and temporal characteristics
  - Spatial data: gauges with coordinates in WGS84 (Longitude, Latitude) suitable for GIS mapping.
  - Temporal data: sub-hourly to hourly accumulations; hyetographs use 5-minute or 15-minute timesteps depending on available tip-time data.

- How this supports GIS and map-based analysis
  - Enables mapping of where AMAX rainfall events occur and how their intensity distributes geographically.
  - Hyetographs provide temporally resolved profiles that can be visualized as time-series layers or animated rainfall events.
  - Data can inform flood risk assessment, drainage design, climate-extremes studies, and policy/decision support for infrastructure planning.

- Limitations and considerations for use
  - Data coverage is non-uniform in time per gauge; median record length is ~20 years with many gauges under 30 years.
  - Spatial independence of events is defined per gauge; cross-gauge spatial independence not enforced.
  - GPCC reference data were not available for QC in this UK-focused dataset.
  - Compound AMAX handling is explicit via event parts; users should interpret Event_id components accordingly.

- References and methodology context
  - QC methodologies and climate-extremes references underpinning the QC and database construction (e.g., GSDR-QC, SHQC; ETCCDI/Climdex datasets; UK-specific adjustments).
  - Foundational studies on independent rainstorms and storm identification inform the event separation approach.