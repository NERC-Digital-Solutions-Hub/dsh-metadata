# Hyetographs and statistics of annual-maximum rainfall events in Great Britain, from historical rain gauge records

## Overview
- Describes the collection, processing, and presentation of rainfall data to generate a dataset of annual-maximum (AMAX) rainfall events in Great Britain.
- Core outputs include AMAX values across multiple durations, dimensionless hyetographs for ~70,000 AMAX events, and statistical properties for these events.
- Data originate from sub-hourly rain gauge records with extensive quality control and event separation to enable temporal climatology and engineering analyses.

## Data sources and scope
- Source agencies: Environment Agency (EA), Natural Resources Wales (NRW), Scottish Environment Protection Agency (SEPA) prior to summer 2018.
- Data resolutions: mix of 15-minute accumulations and tipping-bauge time-of-tip records; typical tip resolution 0.2 mm (some 0.5 mm).
- Coverage: ~27,600 station-years of data; most gauges have a median record length of ~20.5 years; no unified start/end date to preserve long-running records.
- Outputs: ~70,000 independent rainfall events containing ~200,000 AMAX values; time series stored as 5-minute (tip-time) or 15-minute cumulative profiles.

## Data processing and quality control
- QC framework uses two layers:
  - GSDR-QC: automated QC at hourly resolution; adapted for UK data (excluding GPCC due to access restrictions) with local parameter tweaks and UK-specific reference data.
  - SHQC: checks at sub-hourly resolution to flag and remove suspect data, including spike and streak tests; uses rolling-window totals and month-specific thresholds.
- QC references include ETCCDI/Climdex indices and HadEX2/GHCNDEX data; GPCC data not available for UK QC.
- Local UK adaptations include changes to:
  - UK-specific rainfall records (e.g., UK 1-hr and 24-hr records as references).
  - Modified tests for rainfall extremes (e.g., Rx1day replaced with UK 24-hour cap; rolling 24-hour comparisons).
  - Streak threshold adjustments to preserve large events (e.g., 20 mm hourly minimum).
- QC categorization covers format, completeness, temporal/spatial consistency, internal coherence, summarization checks, and threshold/spike/streak analyses.

## Independent rainstorm identification
- Events defined by AMAX values across multiple durations (5, 10, 15 min; 0.5–24 h).
- Independent events separated using per-gauge minimum inter-arrival times to ensure statistical independence between storms.
- Measures taken to avoid duplicating AMAX values within a single event; ~70,000 independent events identified per gauge dataset.
- Event time series archived as cumulative rainfall profiles at 5-minute or 15-minute resolution.

## Data formats and contents
- UK_AMAX.csv: 207,084 AMAX values with associated Burst_id and Event_id.
- UK_AMAX_Hyetographs.csv: 72,094 cumulative rainfall profiles corresponding to AMAX values.
- UK_AMAX_Hyetographs_Statistics.csv: metadata and summary statistics for hyetographs.
- Key identifiers:
  - Event_id: unique for each independent rainfall event; includes station, AMAX duration, end time, and an indicator for compound AMAX status.
  - Burst_id: unique identifier for each AMAX value (specific duration within an event).
- Variable concepts:
  - Station_id/Location, Datetime, Cum_rain, AMAX[mm], Event_duration, Event_magnitude, Longitude/Latitude, Timestep (5 or 15 min), etc.
- Compound AMAX events: final component of Event_id indicates if an event contains multiple storm components contributing to a longer AMAX total.

## Applications and relevance
- Enables detailed temporal characterization of rainfall (hyetographs) and statistical properties of AMAX events for climate research, flood estimation, and infrastructure design.
- Supports climate extremes studies and hydrological modelling that require high-temporal-resolution rainfall inputs.
- Provides a ready-to-use, self-serve dataset for researchers and practitioners analyzing UK rainfall extremes and their temporal profiles.

## Considerations, limitations, and caveats
- Data heterogeneity: mix of temporal resolutions and non-unified gauge periods; long records retained even if not continuous.
- Spatial independence: independence is defined per gauge; cross-gauge spatial independence of events not enforced.
- Data completeness varies; some gauges have limited record lengths and partial years.
- QC adaptations: GPCC data removed from UK QC; UK-specific thresholds and endorsements may affect comparability with global datasets.
- Documentation depth: extensive methodological details and references support replication and validation of QC and event identification.