# Rhos2: Notes from field visits for tensiometers and OLF

## Overview
- A longitudinal field log (2004–2009) documenting tensiometer and OLF (likely open lysimeter/oil-laden facility) measurements, maintenance, calibration, and data issues across multiple plots.
- Recurring themes: data quality concerns, sensor maintenance, frequent hardware failures, and environmental disturbances affecting measurements (notably vole activity and weather events).

## Instruments, measurements and data handled
- Primary sensors: tensiometers at multiple depths (10 cm, 30 cm, 50 cm, and similar configurations), and OLF (open lysimeters) with pumps and gutters.
- Data loggers and ancillary instruments: Delta-T loggers, Tinytags/TinyTag data loggers, tipping buckets (TB) for OLF traps, reed switches, and associated batteries/desiccants.
- Key data types noted: soil water potential (tensiometer readings), water in traps, tipping bucket tips, pump status, sediment sampling notes, and occasional calibration/degassing logs.
- Depths and configurations repeatedly adjusted (e.g., 10 cm, 30 cm, 50 cm tensiometers); frequent degassing and reinstallation when readings were suspected to be erroneous.
- Data quality practices visible: periodic data downloads, calibration notes, and “ignore tips” periods flagged when data were suspected to be unreliable.

## Field maintenance and interventions
- Reinstallation and degassing of tensiometers at various depths (10 cm, 30 cm, 50 cm) to address apparent malfunctions or suspected misreadings.
- Rewiring, replacing and reseating equipment (e.g., wiring changes, sump repairs, and replacement of tensio probes after dodgy readings).
- Routine battery changes and desiccant replacements for loggers and pumps; occasional larger battery changes for OLF and Delta-T systems.
- Physical improvements to field infrastructure: trenching, enlarging pits, repairing sump pipes, replacing gutter covers, and repairing lawn edging around plots.
- Regular calibration and troubleshooting of OLF traps (trap 1–3) and TB rockers; addressing double tipping and reed switch misbehaviors.
- Documentation of vole-related damage prompting structural changes (diverting OLF water, replacing damaged wires, and planning protective measures).

## Data quality, anomalies and challenges
- Storm events causing electrical surges led to all sensors giving identical, nonsensical readings on multiple occasions; such data were flagged as non-sensible.
- Widespread equipment issues: trapped data gaps due to pump failures, blocked gutters, damaged wiring, chewed wires by voles, and reed switch failures.
- Data reliability concerns frequently addressed by recalibration, logger swapping, and recalibration of tipping buckets; some data periods explicitly marked as “ignore tips.”
- Vole activity identified as a major ongoing problem, causing extensive damage to OLF gutters, trenches, and wiring; at one point explicitly noted as a major upcoming problem requiring diversion strategies.
- Data inconsistencies such as double tipping, miscalibrated tiny tags, and sensors in ground at slightly different depths contributing to irregularities.
- Periodic and substantial maintenance required to keep data usable: recalibrations, component replacements (tensions, tensiometers, loggers), and parts swaps to restore function.

## Notable events and observations
- 2004–2005: Initial deployment and early troubleshooting; recurring degassing and wiring maintenance; early data irregularities suspected to be storm-related electrical surges.
- 2005–2006: Frequent data downloads and sensor maintenance; multiple instances of traps full of water due to pump battery issues; numerous degassing and reinstallation events.
- 2006–2007: Widespread field adjustments including trenching above OLF pits to divert surface water; increasing signs of equipment wear and environmental interference.
- 2007–2008: Escalation of vole-related damage; notes on diversions to manage OLF water flow; extensive repair activity across plots 1–3; multiple hardware replacements and recalibration efforts.
- 2008–2009: Emphasis on addressing vole damage with protective measures; reports of chewed wires, reed switch problems, and the need to re-check deltas and logs; culminating in consolidated sensor readings later in 2009 (e.g., detailed records of M2.1, M2.2, and M2.3 tensio readings). A clear warning about vole pressure and its impact on data integrity and field operations remains prominent.

## Summary of data integrity implications for analysis
- The dataset contains numerous periods of questionable reliability due to storm-induced anomalies, vole damage, and hardware failures.
- Effective analysis requires:
  - Rigorous data cleaning to remove or flag periods with non-sensible readings or known data corruption (e.g., storm surge artefacts, double tipping, chewed wiring).
  - Documentation of all sensor recalibrations, replacements, and desynchronizations to align timestamps and depths across equipment.
  - Consideration of environmental disturbances (vole activity, trench widening, gutter integrity) when modeling or imputing missing data.
  - Metadata tracking of data provenance (which logger/channel, depth, and plot) and data provenance for each measurement batch.
- Despite challenges, the log demonstrates extensive field maintenance and efforts to preserve and salvage data across years, with explicit attention to data quality, calibration, and equipment reliability—critical for deriving robust correlations and predictions from the Rhos2 field site.