# Hyetographs and statistics of annual-maximum rainfall events in Great Britain, from historical rain gauge records

## Overview
- Presents a dataset of annual-maximum (AMAX) rainfall events in Great Britain derived from historical sub-hourly rain gauge records.
- Core products: 70,000 dimensionless hyetographs and 200,000 AMAX values, plus statistical properties for each event.
- Data enable analysis of temporal rainfall characteristics and AMAX climatology across GB.
- Data were originally collected by Environment Agency (EA), Natural Resources Wales (NRW), and Scottish Environment Protection Agency (SEPA) and quality-controlled at multiple timescales.

## Data scope and sources
- Timeframe: sub-hourly rainfall records available up to summer 2018.
- Gauges monitoring: EA, NRW, SEPA; data include 15-minute accumulations or time-of-tip records, with tip resolutions often 0.2 mm (some 0.5 mm).
- Records include temporal discontinuities; unified records created by matching gauge coordinates, IDs, and names.
- Approximately 27,600 station-years of data, with a median record length of about 20.5 years prior to QC.
- Final dataset comprises ~70,000 independent rainstorms containing ~200,000 AMAX values.

## Data processing and event identification
- Data processing steps: quality control, identification of temporally independent storms, calculation of rainfall profiles for each storm.
- AMAX values used across durations from 5, 10, 15 minutes up to 0.5–24 hours.
- Rainstorms are defined as independent rainfall events separated by statistically significant dry periods; minimum inter-event times calculated per gauge to ensure statistical independence.
- Each independent event may contain multiple AMAX values for different durations.
- Hyetographs stored as cumulative rainfall profiles at 5-minute (tip-time records) or 15-minute resolution.
- Careful filtering to remove duplicate independent events within the same year.

## Quality control (QC)
- Two automated QC schemes:
  - GSDR-QC: hourly data QC, using station metadata tests, 25 time-series tests, and a rule-base; modified for UK context (local thresholds and reference datasets; GPCC data excluded due to access restrictions).
  - SHQC: sub-hourly QC for high-resolution data, including frequency checks and threshold tests; uses rolling-window sums for 1-min, 5-min, 15-min, and hourly data as available.
- UK-focused adaptations include:
  - Replacing world-record references with UK-specific records (UKMO 1-hr and 24-hr rainfall limits).
  - Adjusting Rx1day to UK 24-hour totals; setting a fixed minimum 20 mm threshold for streaks to preserve large events (e.g., Storm Desmond).
  - Removing GPCC-based spatial consistency tests not available outside DWD.
- Thresholds vary by month to reflect seasonal extremes; tests include spike/streak, completeness, temporal, and spatial checks, plus summarization consistency.

## Independent rainstorm identification details
- Storms identified using fixed-duration AMAX values for multiple time scales (5, 10, 15 minutes; 0.5, 1, 2, 3, 6, 12, 24 hours).
- Post-filtering excludes years with >15% incompleteness or suspicious data.
- Event and AMAX relationships:
  - Burst_id identifies AMAX instances for a given duration at a gauge.
  - Event_id identifies an independent rainfall event; an Event may contain multiple AMAX values.
  - Compound AMAX events occur when a long-duration AMAX is composed of multiple independent rainstorm components.
- Result: ~70,000 independent rainfall events across GB.

## Data format and contents
- Three data files:
  - UK_AMAX.csv: 207,084 AMAX values (per burst).
  - UK_AMAX_Hyetographs.csv: 72,094 cumulative rainfall profiles (hyetographs) containing AMAX values.
  - UK_AMAX_Hyetographs_Statistics.csv: metadata and simple summary statistics for hyetograph profiles.
- Key variables:
  - Event_id and Burst_id: unique identifiers; Event_id differentiates independent events; Burst_id differentiates AMAX instances.
  - AMAX[mm]: depth of AMAX for a given duration.
  - Datetime: timestamp for hyetograph accumulation (5-min or 15-min resolution).
  - Cum_rain: cumulative rainfall depth (hyetograph profile).
  - Location coordinates (Longitude, Latitude), Station_id.
  - Timestep: 5 or 15 minutes (depending on data resolution).
  - Event_duration: duration of the event in minutes.
  - Event_magnitude: total event depth (mm).
  - Agency: original data provider (EA, NRW, SEPA).

## Outputs and potential uses
- Hyetographs and AMAX statistics support:
  - Temporal profiling of rainfall events for infrastructure design, flood estimation, and climate extremes analysis.
  - Climatological studies of AMAX event characteristics in GB.
- Data are suitable for integration with other datasets to enhance environmental monitoring and assessment.

## Access, limitations, and provenance
- Data originate from official UK agencies and undergo rigorous quality control with UK-specific adaptations.
- QC relies on external reference datasets (ETCCDI, HadEX2) where accessible; GPCC data were not used due to access restrictions.
- Temporal coverage is heterogeneous across gauges; most gauges have less than 30 years of data, with a substantial portion around 20 years pre-QC.
- Spatial independence of events is not guaranteed (events are defined per gauge independently).

## References (selected)
- WMO Guidelines on Surface Station Data Quality Assurance for Climate Applications.
- ETCCDI and Climdex-based rainfall indices (HadEX2) for QC references.
- UK-specific rainfall records and thresholds (UK Met Office data).
- Foundational methodology for independent storm identification and rainfall event analysis.