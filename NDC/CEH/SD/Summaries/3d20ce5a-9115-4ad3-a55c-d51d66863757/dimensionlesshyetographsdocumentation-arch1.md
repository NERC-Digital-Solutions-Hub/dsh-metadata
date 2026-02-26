# Hyetographs and statistics of annual-maximum rainfall events in Great Britain, from historical rain gauge records Supporting Documentation

## Overview
- Describes the collection, QC, processing, and formatting of rainfall data used to create a dataset of the unique temporal profiles (hyetographs) of annual-maximum AMAX rainfall events in Great Britain.
- Original data come from Environment Agency (EA), Natural Resources Wales (NRW), and Scottish Environment Protection Agency (SEPA) at sub-hourly resolution; subjected to quality control and event segmentation to produce AMAX-based records and hyetographs.
- Core outputs: AMAX values at multiple durations, dimensionless hyetographs for ~70,000 events, and statistical properties for these events.

## Data scope and content
- Data period: all available sub-hourly records from EA, NRW, SEPA prior to summer 2018; no unified start/end date across gauges.
- Coverage: approximately 27,600 station-years of data; median pre-QC record length ~20.5 years.
- Event statistics:
  - About 70,000 independent rainfall events identified.
  - Approximately 200,000 AMAX values (across durations).
  - ~72,094 cumulative rainfall profiles (hyetographs) produced.
- Temporal resolutions:
  - 5-minute or 15-minute cumulative profiles (depending on tip-time data availability).
  - AMAX durations considered: 10 minutes to 24 hours, with independent-event segmentation implemented at gauge level.
- Data organization:
  - Three CSV files: UK_AMAX.csv (AMAX values), UK_AMAX_Hyetographs.csv (hyetographs), UK_AMAX_Hyetographs_Statistics.csv (metadata/statistics).
- Event structure:
  - Event_id encodes station, AMAX duration, end time, and an event-part indicator.
  - Burst_id corresponds to an individual AMAX value (a “burst”).
  - Event part in Event_id indicates compound AMAX events (non-zero value signals a compound event).

## Methods: quality control and data processing
- Quality control (QC) workflow:
  - Automated QC in two stages: GSDR-QC (hourly) and SHQC (sub-hourly).
  - GSDR-QC uses station metadata tests, 25 time-series tests, and a rule-based flagging system; ETCCDI indices (Climdex) and GPCC daily data used as reference datasets where available.
  - Local UK adaptations exclude GPCC due to access restrictions; ETCCDI references retained.
  - Modifications tailored to UK rainfall characteristics, including adjustments to UK-specific records (UKMO 1-hour and 24-hour thresholds) and a revised 24-hour rolling window comparison.
  - SHQC focuses on sub-hourly resolution data, with threshold-based trimming of implausibly intense episodes; thresholds vary by month and data resolution (hourly, 15-minute, 1-minute).
  - Tip-time data (where available) enables detailed spike and streak checks; rolling-window sums are used for totals.
- Independent rainstorm identification:
  - Rainstorms identified using fixed-duration AMAX values across 5, 10, 15 minutes and 0.5, 1, 2, 3, 6, 12, 24 hours.
  - An algorithm estimates the minimum time between independent events (exponential arrival distribution) to separate storms statistically.
  - Excluded years with more than 15% incomplete/suspicious data per gauge.
  - Careful de-duplication to avoid counting multiple AMAXs within the same storm as separate events.
- Outputs:
  - Independent rainfall events and their AMAX values are stored as cumulative rainfall profiles, enabling temporal and climatological analyses.

## Data structure and formats
- UK_AMAX.csv: 207,084 AMAX values; key fields include Event_id, Burst_id, AMAX_mm, Station_id, End datetime, etc.
- UK_AMAX_Hyetographs.csv: 72,094 cumulative rainfall profiles; fields include Datetime, Cum_rain, Location coordinates, Timestep (5 or 15 minutes).
- UK_AMAX_Hyetographs_Statistics.csv: metadata for hyetographs; includes Longitude, Latitude, Timestep, Event_duration (minutes), Event_magnitude (total depth in mm).
- Key identifiers:
  - Event_id: unique event with location, AMAX duration, end time, and optional event part.
  - Burst_id: identifier for each AMAX value within an event.
  - Event_duration: duration of the AMAX event (minutes).
  - Event_magnitude: total event depth (mm).
- Agencies: EA (Environment Agency), NRW (Natural Resources Wales), SEPA (Scottish Environment Protection Agency).

## Considerations for analysts
- Suitable for analyses of rainfall temporal structure, AMAX climatology, and hyetograph-informed flood/engineering risk assessments.
- Independence caveat: events are defined independently at the gauge level; spatial independence across gauges is not guaranteed.
- Temporal scope caveat: no single, uniform time period across all gauges; dataset compiles all available data pre-2018.
- Data quality caveat: GPCC data not used in QC; UK-specific QC adaptations applied; some external reference datasets are not accessible in full.
- Rich, multi-resolution data enabling correlation studies, model validation, and exposure of temporal rainfall patterns contributing to extreme-event analyses.

## References
- Includes WMO quality assurance guidelines, ETCCDI/Climdex datasets, GPCC products, UK extreme rainfall records (UKMO), and methodological papers on independent rainstorms and sub-hourly QC.