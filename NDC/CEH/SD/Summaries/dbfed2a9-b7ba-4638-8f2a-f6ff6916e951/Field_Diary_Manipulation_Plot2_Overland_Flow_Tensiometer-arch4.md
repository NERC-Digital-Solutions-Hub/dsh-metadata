# Rhos2: Notes from field visits for tensiometers and OLF

## Scope and purpose
- Field log documenting tensiometer and OLF (observational fluxes) field activities, sensor maintenance, data issues, and operational challenges across multiple plots from 2004 to 2009.
- Tracks data quality concerns, calibration, repairs, and decisions to include or exclude data.

## Data collection components and workflow
- Devices involved:
  - Tensiometers at multiple depths (10 cm, 30 cm, 50 cm)
  - OLF (open lateral flow) traps with tipping buckets and associated sensors
  - Delta-T loggers, Tinytags, and tiny-tag related instrumentation
  - Battery packs, desiccants, wiring and connectors
- Regular tasks:
  - Degassing tensiometers, replacing wiring, recalibrations
  - Data downloads and time synchronization
  - Sediment/trap sampling, trenching, and maintenance of gutters and covers
  - Periodic replacement of tensiometers and big batteries; calibration checks

## Data quality events and data gaps
- Storm-related data corruption:
  - 15/06/04 and 19/07/05: all sensors produced identical nonsensical readings attributed to electrical surges from storms.
- Water ingress and data loss:
  - 31/10/05 and 10/11/05: traps filled with water due to pump battery issues; noted as data to be ignored for affected periods.
  - 16/11/06: traps 2 blocked; evidence of subsurface flow; data flagged accordingly.
- Ongoing data integrity issues:
  - Recurrent “tips” anomalies (double tipping, timing misalignments) prompting recalibration and data exclusion windows.
  - 2007–2009: vole damage causing wiring and tube issues; necessitated shielding, covers, trench work, and reassessment of data validity.
- Data cleaning and flagging:
  - Frequent instructions to “ignore tips” during specific windows and to treat certain data as unreliable or invalid until rechecked.

## Maintenance, calibration, and data hygiene
- Frequent hardware interventions:
  - Re-installation of tensiometers, 50 cm and shallower probes, and replacement when readings were dubious
  - Wiring changes, degassing, sediment trap access, and sump/tipping bucket repairs
- Calibration and timing:
  - Calibration of tiny tags and loggers; resetting sampling intervals (e.g., tinytags and tiny-tag timing adjustments)
  - Replacing sensors (tensiometers, TBs, read switches) and recalibrating to restore data integrity
- Physical/structural upkeep:
  - Enlarging pits, installing trenching above plots to manage water, replacing gutter covers, and repairing lawn edging
  - Regular battery replacement and desiccant changes to maintain logger performance

## Environmental and operational challenges
- Wildlife interference:
  - Voles causing repeated damage to wires and tubes; necessitated protective measures and data interpretation adjustments
- Weather and environmental conditions:
  - Grass cutting, weed management, thistles, and leaf litter affecting sensor cages
  - Water management issues requiring drainage modifications and sump/pump maintenance

## Data governance and implications for Data Leaders
- Provenance and metadata needs:
  - Detailed logging of maintenance, calibrations, and events that affect data quality
  - Explicit flags or annotations for data to be ignored or flagged as suspect
- Data quality assurance:
  - Importance of automated and manual checks to identify storms, instrument faults, and wildlife damage
  - Cross-device verification (e.g., delta-T vs Tinytag) to diagnose data integrity problems
- Standardization and transparency:
  - Consistent documentation of when data is excluded and the rationale behind those decisions
  - Clear metadata around sensor depths, calibration status, battery level, desiccant status, and hardware replacements

## Recommendations and takeaways for data-powered leadership
- Harden field instrumentation against wildlife and environmental wear (vole-proof housings, strengthened wiring protections, protective covers).
- Implement automated data quality flags and centralized incident logs to track data integrity issues and remediation steps.
- Standardize metadata schemas across devices (sensor type, depth, calibration date, battery status, desiccant status, data exclusion windows).
- Establish explicit data exclusion policies and communicate data availability after incident periods to stakeholders.
- Build redundancy and rapid repair workflows to minimize data loss during storms or equipment failures.