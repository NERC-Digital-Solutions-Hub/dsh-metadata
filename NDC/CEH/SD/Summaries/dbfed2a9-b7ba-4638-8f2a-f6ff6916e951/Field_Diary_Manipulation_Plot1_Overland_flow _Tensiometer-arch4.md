# Rhos1: Notes from field visits for tensiometers and OLF

## Overview
- Field log documenting tensiometers and overland flow (OLF) traps at Rhos1 from 2005 to 2009.
- Records include setup, maintenance, sensor issues, data edits (tips/comments added to raw data), calibrations, and data quality decisions.
- Emphasis on data reliability, with frequent notes to ignore or flag data during certain periods (e.g., around storms, calibration, or sensor faults).

## Instrumentation and site context
- Components involved: tensiometers (at multiple depths: 10 cm, 30 cm, 50 cm), OLF traps with tipping buckets, pumps, reed switches, sensors, tinytags, delta T loggers.
- Plots referenced: multiple subplots (e.g., plot 1.1, 1.2, 1.3; plot 2; plot 3; control plots) with associated pits, gutters, and trench work.
- Data collection devices include long-running loggers, batteries/desiccants replaced, and occasional external power/additional logging equipment.

## Data quality and processing notes
- Raw data often edited post-collection (e.g., tips edited from raw data files; some tips flagged as ignore).
- Recurrent data integrity events:
  - Storms and electrical disturbances causing nonsensical or spuriously recorded readings across sensors.
  - Moisture ingress affecting loggers (desiccant changes required).
  - Desynchronization or miscalibration of tipping buckets and reed switches (faults corrected with recalibration or component replacement).
  - Battery failures and pump/float switch issues leading to incomplete or unreliable data (replacements and recalibrations documented).
  - Blockages in gutters, traps, or pipes causing full or partial data loss; several notes indicate data should be disregarded during affected periods.
  - Animal/vole interference and vandalism (e.g., damage to tubing, mesh, and covers) prompting repairs.
- Calibration and verification activities include:
  - Recalibrations of tipping buckets (documented values in multiple entries).
  - Regular degassing and "logged" checks to confirm sensor functionality.
  - Specific notes on when tipped data may be unreliable (e.g., “ignore tips” windows, double-tipping events, reed switch misalignment).
- Metadata practices observed:
  - Entries typically link to sensor IDs, plot numbers, depths, and timestamps.
  - Occasional cross-referencing with additional sheets (e.g., calibration sheets) for validation.

## Key data governance implications for Data Leaders
- Provenance and edit tracking: Data edits (tips removal, ignore periods) must be clearly documented with justification and time stamps.
- Data quality flags: Systematic use of flags for storm-related anomalies, sensor faults, or calibration issues to distinguish usable data from questionable segments.
- Metadata standardization: Consistent recording of sensor IDs, depths, plot locations, and equipment status (batteries, desiccants, reed switches) to support discoverability and reproducibility.
- Data continuity risk: Recurrent hardware failures (batteries, pumps, reed switches) and environmental damage (vole interference) create intermittent data gaps requiring explicit gap handling strategies.
- Governance of “ignore” decisions: Establish criteria for when data should be excluded or flagged versus retained with caveats, and ensure those decisions are auditable.

## Lessons learned and recommended actions for data management
- Implement a formal data quality framework:
  - Define when to ignore data and how to flag corresponding records.
  - Maintain an auditable log linking each data edit to its rationale and the underlying equipment status.
- Standardize instrumentation metadata:
  - Create a registry of sensors with IDs, depths, plots, and component health (battery level, desiccant status, reed switch condition).
- Strengthen calibration and maintenance protocols:
  - Schedule and document routine calibrations, with stored calibration sheets referenced in the data model.
  - Track cause of recurring faults (e.g., reed switch misalignment, pump sticking) to inform supplier/vendor actions and design improvements.
- Improve data discoverability and traceability:
  - Attach field notes to data records or associated metadata files to provide context for quality flags.
  - Use consistent timestamp formats and synchronize logs across devices to minimize temporal misalignment.
- Proactively manage data gaps:
  - Identify high-risk periods (storms, maintenance windows) and implement planned redundancy or backup logging where feasible.

## Notable data lineage and examples from the notes
- Entries repeatedly record “degassed,” “calibrated,” and “ignore tips” actions tied to specific dates, sensors, and plots.
- Frequent references to equipment recalibration (tipping buckets), battery/desiccant changes, and pump or float switch repairs.
- Several instances of “data to be disregarded” or “ignore tips” during defined time windows around maintenance or sensor anomalies.
- Depth-specific and plot-specific notes (e.g., 10 cm tensio in various plots, pit 1.3 pump issues, reed switch corrections) illustrating granular traceability of data quality decisions.