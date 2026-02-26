# Hyetographs and statistics of annual-maximum rainfall events in Great Britain, from historical rain gauge records Supporting Documentation

- Purpose: Describe collection and processing of sub-hourly rainfall data to build a dataset of annual-maximum (AMAX) rainfall events in Great Britain, including hyetographs and statistical properties.
- Core outputs:
  - AMAX values across multiple durations
  - Dimensionless hyetographs for ~70,000 AMAX events
  - Statistical properties for these events

## Data scope and sources
- Original data from three government agencies: Environment Agency (EA), Natural Resources Wales (NRW), Scottish Environment Protection Agency (SEPA)
- Data characteristics:
  - Sub-hourly resolution with 15-minute accumulations or time-of-tip records
  - Tip resolutions commonly 0.2 mm per tip (some at 0.5 mm)
- Time span: Records up to summer 2018; no unified start/end date; most gauges have median ~20.5 years of data; total ~27,600 station-years
- Data challenges addressed:
  - Temporal discontinuities due to file splits or operator changes, reconciled by matching coordinates, IDs, and names
  - Data gathered from multiple gauges across GB, not strictly spatially aligned

## Quality control and data processing
- QC framework:
  - GSDR-QC: automated quality control at hourly resolution (adapted for UK); includes station metadata checks, 25 time-series tests, and a rule-based flagging system
  - SHQC: sub-hourly QC applied to the original data (pre-aggregation) to catch suspect data
- Reference datasets used for QC (UK-adapted):
  - ETCCDI indices from Climdex (HadEX2 data)
  - GPCC daily data (not accessible for local UK QC; excluded from this study)
- Local adaptations and key changes:
  - GPCC-based spatial consistency tests disabled due to access restrictions
  - UK-specific parameter adjustments:
    - UKMO 1-hour and 24-hour rainfall records used for thresholding
    - Rx1day test replaced with UKMO 24-hour rolling-window comparison
    - Streak threshold adjusted to 20 mm for large events (e.g., Storm Desmond 2015)
- Thresholds and tests:
  - Thresholds vary by month and resolution (hourly, 15-minute, 1-minute)
  - Includes spike and streak tests, drizzle tests, and rolling-window checks
- Output of QC:
  - Cleaned, quality-assured sub-hourly rainfall series used for AMAX identification

## Independent rainstorm identification
- Independence criteria:
  - Rainfall events identified using fixed-duration AMAX values across rolling windows: 5, 10, 15 minutes; ½, 1, 2, 3, 6, 12, 24 hours
  - Durations chosen to align with climatological and engineering needs
- Event separation:
  - Minimum inter-event dry period determined per gauge to ensure statistical independence (exponential arrival-time distribution)
  - Separation performed at the gauge level; spatial independence across gauges not enforced
- Handling of multiple AMAX within a single event:
  - Some events contain multiple AMAX values of different durations
  - Careful filtering to remove duplicates of independent rainstorms
- Dataset scale:
  - Approximately 70,000 independent rainfall events
  - Approximately 200,000 AMAX values
  - Per-event time series stored as cumulative rainfall profiles at 5-minute (tip-time records) or 15-minute resolution

## Data format and contents
- Three primary files:
  - UK_AMAX.csv: All 207,084 AMAX values
  - UK_AMAX_Hyetographs.csv: 72,094 cumulative rainfall profiles containing AMAX values
  - UK_AMAX_Hyetographs_Statistics.csv: Metadata and summary statistics for hyetographs
- Key variables and structure:
  - Event_id and Burst_id differentiate independent events and AMAX occurrences
  - Event_id encodes station, AMAX duration, end time, and an event-part indicator (to mark compound AMAXs)
  - Burst_id identifies individual AMAX occurrences within events
  - Geographic coordinates (Longitude, Latitude) and timing (Datetime) included
  - Timestep indicates 5 or 15-minute resolution
  - Event_duration and Event_magnitude summarize event-level results
  - Agency field records data provenance (EA, NRW, SEPA)
- Relationships:
  - Multiple rows may share the same Event_id (same independent event)
  - Burst_id ties to a specific AMAX value within an event

## Data quality, limitations, and governance
- Coverage and continuity:
  - Not all gauges span the same time period; clipping to create a unified period would lose long-running records, so all available data were retained
  - Most gauges have less than 30 years of data; median ~20.5 years pre-QC
- Limitations:
  - Spatial independence of events is not enforced across gauges
  - GPCC data inaccessible for local QC, reducing some external validation options
  - Some records lack complete spatial coverage; not a fully spatially harmonized dataset
- Reproducibility and transparency:
  - Detailed methodology and adaptations to GSDR-QC published and described, enabling replication
  - Clear documentation of data sources, QC modifications, storm separation logic, and data formats

## References and sources
- Includes WMO guidelines, ETCCDI/Climdex references, GPCC methodology, and supporting methodological papers detailing QC and storm identification approaches
- Key cited works cover quality control, independent rainstorm identification, and UK-specific adaptations to global QC frameworks