# Rhos2: Notes from field visits for tensiometers and OLF

- Overview
  - A longitudinal field log documenting tensiometer and OLF (open larval food? or open liquid flow) sensor deployments across plots, dates from 2004 to 2009.
  - Content covers sensor readings, hardware status, maintenance, calibration, data integrity concerns, and incidents affecting data collection (storms, vole damage, wiring issues, battery problems, and pump failures).
  - Multiple instruments per plot and depth (e.g., 10 cm, 30 cm, 50 cm tensiometers; OLF traps; tinytags; Delta-T loggers).

- Data quality and integrity themes
  - Data anomalies linked to external events: storm-induced electrical surge causing uniform nonsensical readings across sensors.
  - Recurrent data reliability issues: double tipping, tips recorded at wrong times, and periods flagged as “ignore tips” due to suspected faults.
  - Physical and environmental hazards affecting data: water in traps, blocked gutters, pump battery failures, chewed wiring (rodent/vole damage), trenching changes, and grounding/wiring faults.
  - Sensor and equipment failures necessitating replacements or recalibration: degassing, vent/connection problems, reed switch failures, desiccant changes, andตัวtinytag/logger issues.
  - Data management actions to preserve quality: regular data downloads, calibration checks, noting “All working correctly” after fixes, and explicit notes to disregard data during known faulty periods.

- Instrumentation, placement, and maintenance actions
  - Re-installation and adjustment: tensiometers moved/reinstalled at specific depths (e.g., 10 cm) and plots (e.g., 2.1, 2.2, 2.3; 3.1–3.3).
  - Routine upkeep: degassing, battery replacements, desiccant changes, vent inspections, and tube/tension upgrades.
  - Repairs and replacements: sump repairs, pump replacements, electrolyte/tubing corrections, wire repairs, and sensor/tensiometer replacements across multiple plots.
  - Data collection infrastructure improvements: protective covers, trenching above plots to divert water, enclosure boxes for pits, and prevention measures for vole damage (gutter covers, protective frames).
  - Documentation of calibration and data integrity checks: notes on recalibration needs, recalibration timing, and cross-referencing tip counts with loggers.

- Data provenance, metadata, and governance implications
  - Extensive instrument-level detail observed: instrument IDs, serial numbers, sensor depths, plot identifiers, and timing of data collection events.
  - Frequent "ignore tips" and “data not recorded” annotations indicating the need for explicit data quality flags and clear provenance for excluded data.
  - The logs reveal a rich history of changes to instrumentation and configurations that must be captured in metadata to interpret time-series data accurately.
  - Necessity for a robust data management plan to track:
    - Instrument inventory and changes (which device, where, when, and why).
    - Data quality flags and justification for excluding or flagging data.
    - Calibration events, sensor replacements, and connections (reed switches, delta-T channels, tensio probes).
    - Environmental and maintenance events that could influence data (vole damage, weather events, pump failures).

- Challenges highlighted for data stewards
  - Maintaining completeness amid hardware failures and environmental disturbances.
  - Ensuring consistent metadata standards across many instruments, plots, and years.
  - Handling data gaps and unreliable periods while preserving traceability for users.
  - Coordinating between field notes and digital datasets to reflect corrections, recalibrations, and sensor replacements.

- Practical recommendations for data governance
  - Establish a standardized instrument inventory with unique IDs, depths, plots, and installation dates; link to all data streams (tensiometers, OLF, tinytags, Delta-T loggers).
  - Implement a formal data quality framework with flags for:
    - Suspected storm-related anomalies
    - Double tipping or mis-timed tips
    - Data during known maintenance windows or “ignore tips” intervals
    - Sensor/connector/wiring faults and recalibration events
  - Require metadata templates capturing:
    - Sensor type, depth, plot, serial number
    - Dates of installation, maintenance, calibration, and replacement
    - Data quality notes and any data exclusions with justification
  - Maintain versioned data records and an audit trail tying data points to corresponding field notes and maintenance actions.
  - Document data cleaning and transformation rules, including when and why data were degassed, recalibrated, or replaced.
  - Plan for data sharing by communicating data reliability, known issues, and any periods unsuitable for analyses to end users.

- Notable events and their data impact
  - 2004–2005 storms caused electrical surges leading to non-sensible, identical readings across sensors.
  - 2005–2007 recurring issues with pump batteries, debris, and water management affecting trap data and Tinytag readings.
  - 2007–2008 significant vole damage affecting OLF gutters, wires, and sensors, with multiple repairs and protective measures.
  - 2008–2009 ongoing issues with chewed wires, reed switches, and intermittent data from Delta-T and Tinytag loggers, necessitating recalibrations and hardware replacements.
  - Throughout: frequent notes to ignore tips during problematic intervals and extensive records of fixes, recalibrations, and re-installations.

- Takeaway for data stewards
  - The dataset is a long-running, multi-instrument field deployment with substantial data quality challenges arising from environmental and hardware factors.
  - Strong data governance is essential to preserve data usability: detailed instrument-level metadata, explicit quality flags, a clear audit trail of maintenance actions, and standardized handling of data exclusions.
  - Proactive documentation and consistent linking of field notes to digital data will enhance discoverability, reliability, and reusability for downstream analyses.