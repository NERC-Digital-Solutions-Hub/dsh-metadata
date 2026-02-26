# Hyetographs and statistics of annual-maximum rainfall events in Great Britain, from historical rain gauge records Supporting Documentation

- Purpose and scope
  - Describes the collection and processing of rainfall data to generate a dataset of the unique temporal profiles (hyetographs) of annual-maximum (AMAX) rainfall events in Great Britain.
  - Core data are AMAX hyetographs from sub-hourly rain gauges, with ~70,000 independent rainfall events and ~200,000 AMAX values.
  - Hyetographs enable analysis of the temporal characteristics and climatology of AMAX-causing events across GB.
  - Data originate from three government bodies (Environment Agency, Natural Resources Wales, Scottish Environment Protection Agency) and were quality controlled at hourly and sub-hourly scales.

- Data provenance and governance
  - Data providers: EA, NRW, SEPA; data compiled and QC’d for research use.
  - External reference datasets used for QC: ETCCDI indices (Climdex datasets) and GPCC daily data (GPCC access restricted to DWD; not accessible for UK QC, therefore omitted in local QC).
  - Local adaptations to QC: GPCC-based tests removed; UK-specific adjustments to reflect British rainfall characteristics (e.g., UKMO 1-hr and 24-hr records).
  - Documentation includes data lineage, processing steps, and metadata to support reuse and reproducibility.
  - Data licensing and sharing considerations noted through reference data access restrictions and local QC adaptations; not all external reference data are accessible for independent verification.

- Data collection
  - Source records: sub-hourly rain gauge data available up to summer 2018, with 15-minute accumulations or time-of-tip data, and tip resolutions typically 0.2 mm (some 0.5 mm).
  - Data heterogeneity: varying temporal resolutions and station metadata; temporal discontinuities reconciled by matching coordinates, IDs, and names.
  - Temporal coverage: no unified period across gauges; many gauges closed before 2018; aiming to preserve all available long-running records.
  - Coverage: approximately 27,600 station-years of data compiled; most gauges have median ~20.5 years of data prior to QC.

- Methods overview
  - QC (quality control): two-tier approach
    - GSDR-QC: automated QC on hourly data (and some tests on sub-hourly data) using station metadata, 25 time-series tests, and a rule-based flagging system; local UK adaptations applied (no GPCC tests; modified thresholds and references).
    - SHQC: sub-hourly QC on original resolution data, focusing on frequency checks and threshold-based filtering to remove implausible high-intensity events; uses rolling-window sums and month-specific thresholds.
  - Independent rainstorm identification: storms identified using fixed-duration AMAX values across multiple rolling-window durations (5, 10, 15 minutes; 0.5, 1, 2, 3, 6, 12, 24 hours); gauge-level separation of independent events based on statistically independent arrival times; care taken to avoid duplicate AMAXs within a single event.
  - Data processing: creation of cumulative rainfall profiles for each independent event; handling of records with incomplete years or gaps; emphasis on preserving long records where possible.
  - Outputs planned to support climatological and hydrological analyses with robust metadata.

- Independent rainstorm identification details
  - Definition: independent rainstorms are separated when rainfall ceases at a gauge for a minimum time inferred to yield independent arrivals (per gauge, not spatially cross-checked).
  - Durations used: AMAX values extracted for 5-, 10-, 15-minute and 0.5-, 1-, 2-, 3-, 6-, 12-, 24-hour windows.
  - Outcome: final dataset comprises about 70,000 independent events with ~200,000 AMAX values; each event may contain multiple AMAX values.
  - Data structure note: events can be compound (long-duration AMAX composed of multiple sub-events); indicated in event identifiers.

- Data format and contents
  - Three main files:
    - UK_AMAX.csv: contains all 207,084 AMAX values; fields include AMAX depth, Burst_id, Event_id, duration, and location metadata.
    - UK_AMAX_Hyetographs.csv: contains 72,094 cumulative rainfall profiles corresponding to the AMAX values.
    - UK_AMAX_Hyetographs_Statistics.csv: contains metadata and summary statistics for the hyetographs (including location, timestamping, resolution, event duration, and total event depth).
  - Key data relationships
    - Burst_id identifies individual AMAX events (specific duration and end time).
    - Event_id identifies independent rainfall events; an Event_id may encompass multiple Burst_ids.
    - Compound AMAX events: indicated by a non-zero event-part component in the Event_id.
  - Spatial and temporal details
    - Hyetographs include timestamps aligned to 5-minute (tip-time records) or 15-minute resolutions.
    - Geographic coordinates provided for gauges ( longitude, latitude in UK_AMAX_Hyetographs_Statistics.csv ).

- Data quality and limitations
  - QC outcomes reduce but do not eliminate all issues; emphasis on sub-hourly fidelity and plausibility across resolutions.
  - Limitations stem from data heterogeneity, gauge- and period-specific gaps, and reliance on external reference datasets with access restrictions.
  - The dataset is not spatially aggregated or fully spatially independent (independence is defined per gauge at the storm level).
  - Some long-running historical data may be excluded from uniform periods to preserve data length, which affects temporal consistency across gauges.

- Practical considerations for data stewardship
  - Clear provenance and metadata facilitate discoverability and reuse; alignment with established QC practices (GSDR-QC and SHQC) supports data integrity.
  - Documentation of modifications to QC procedures and reference datasets helps maintain transparency and auditability.
  - File structure and identifier conventions (Event_id, Burst_id) support traceability between individual AMAX values, hyetographs, and independent events.
  - Data availability constraints (e.g., GPCC access restrictions) and UK-specific adaptations should be recorded in data governance notes and user guides.

- References and context
  - Foundational works on QC methodologies, extreme rainfall indices, and independent rainstorm identification cited to support methodological choices and reproducibility (e.g., WMO guidelines, ETCCDI/Climdex datasets, GPCC, Met Office UK climate extremes).
  - Related studies by Villalobos-Herrera and colleagues detailing storm creation, climatology, and sub-hourly QC enhancements underpin the processing workflow.