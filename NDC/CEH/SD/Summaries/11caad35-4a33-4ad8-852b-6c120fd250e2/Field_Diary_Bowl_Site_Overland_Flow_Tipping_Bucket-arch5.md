# Overland Flow and Tipping Bucket Monitoring Log

## Overview
- A longitudinal field log (2004–2009) of overland flow (OLF) measurements, tipping bucket (TB) data, weir box readings, and tinytag logger activity.
- Documents calibration, maintenance, data processing decisions, and incidents affecting data quality and usability.
- Aimed at ensuring data standards, traceability, and usability for analysis of flow events and related hydrological processes.

## Data collection and instrumentation
- Instruments involved: tipping buckets (TB), tinytag loggers, transducers, weir boxes, and associated plumbing (gutters, downpipes).
- Time intervals:
  - Initial 10-minute interval; later shortened to 5-minute intervals to avoid logger overflow.
  - 2005 adjustments reduced to 4-minute intervals at one point; 03/10/06 note mentions reset to 5-minute recording intervals.
- Measurements:
  - TB calibration established a per-tip volume (initially ~1 L; recalibrated to ~1.90933 L on 07/06/2007; later adjustments noted).
  - OLF measurements documented via weir box and TBs; occasional channeling around gutters due to animal activity.
- Data handling:
  - Regular downloads of TB, OLF, and drain data; notes on data integrity during downloads and calibration events.
  - Time zones adjusted (BST vs GMT) and timestamp issues acknowledged and resolved later.

## Data quality, processing, and metadata
- Data quality practices:
  - Raw data preserved; edits to reduce dataset size noted (and sometimes avoided for raw data).
  - Data flagged as unreliable or to be ignored during calibration, testing, or system adjustments (e.g., 10:24–13:00 GMT calibration periods; 13:30–14:30 ignores on 05/07/06).
  - Timestamp corrections and re-calibration events documented to maintain temporal accuracy.
- Calibration and interpretation:
  - 2007 calibration linked 30 L through TB to 16–17 tips, yielding ~1.9 L per tip; subsequent notes to adjust volume accounting (e.g., 02/12/08, 14/11/08) to align with measured TB performance.
  - 2008 note: apply linear incremental change in tip volume about six months after initial calibration to account for drift.
- Data quality issues and mitigation:
  - Recognized risks from vole/mole damage to OLF trap and nearby infrastructure; repairs and reinforcements performed (soil, stones, clay seals, grates proposed).
  - Physical blockages (sediment, leaf litter) in downpipes and filters (weir boxes, TBs) necessitated cleaning and maintenance.
  - Sensor and hardware reliability concerns: magnets detaching, reed switches failing, battery failures, transducer alignment issues, and need for re-seating or reinstallation.
  - Data gaps or questionable periods identified (e.g., passages labeled for “ignore data” during calibrations or maintenance events).

## Maintenance, incidents, and field actions
- Regular maintenance events:
  - Recalibration of tipping bucket volumes and checks of system accuracy.
  - Replacements and re-installations of TBs, magnets, reed switches, and batteries; addressing sensor malfunctions.
  - Weir box and gutter maintenance, including resealing, clearing blockages, and ensuring proper flow paths.
- Environmental challenges:
  - Animal damage to traps and infrastructure necessitating repairs and protective measures.
  - Sediment buildup and debris affecting OLF channeling and measurement integrity.
- Documentation of interventions:
  - Detailed notes on times, actions taken, and observed effects (e.g., calibration during downpipe work, weir box recalibration, sensor re-seating).

## Data governance implications for data stewards
- Emphasizes the importance of clear calibration metadata:
  - Calibration dates, per-tip volumes, and any subsequent adjustments to maintain accuracy.
- Necessitates transparent data curation:
  - Distinction between raw vs. edited data; rationale for ignoring data during calibration or maintenance.
- Requires robust maintenance logging:
  - Recording of equipment failures, repairs, and re-installations to support data provenance.
- Highlights interoperability considerations:
  - Handling of multiple sensors and data streams (TBs, tinytags, transducers, weir boxes) with synchronized timestamps.
- Suggests governance improvements:
  - Standardized metadata templates for calibration, instrument IDs, units, and data quality flags.
  - Regular reviews of data processing decisions to ensure reproducibility and traceability.

## End-state observations and recommendations
- Data quality relies on ongoing calibration, timely maintenance, and careful handling of timestampkeeping (BST vs GMT).
- Recommend maintaining:
  - A centralized calibration log with per-tip volumes and calibration dates.
  - An explicit data quality flag system to mark ignored periods and calibration windows.
  - Routine checks for animal-related damage and protective measures to reduce future disruptions.
- Consider enhancements:
  - Improved mounting and mounting stability for transducers and TBs to reduce data losses.
  - Clear procedures for re-seating and validating sensor alignment after maintenance.
  - Automated timestamp validation and drift checks to minimize manual correction needs.