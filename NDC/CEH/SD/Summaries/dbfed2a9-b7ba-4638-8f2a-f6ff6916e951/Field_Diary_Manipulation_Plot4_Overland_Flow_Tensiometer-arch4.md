# Penllywn: Notes from field visits for tensiometers and OLF

## Executive overview
- A long-running field log (2005–2009) documenting installation, maintenance, calibration, data collection, and issues for tensiometers and overland flow (OLF) monitoring across multiple plots.
- Data streams include tensiometer readings at various depths (e.g., 10 cm, 30 cm, 50 cm), Delta T loggers, OLF tipping buckets, tinytag data loggers, pump status, and associated metadata (batteries, wiring, blockages, calibration events).
- The record reveals frequent data quality problems (sensor/pump failures, power issues, data gaps, clock drift, wiring faults) and ad-hoc remediation steps. It also notes procedural suggestions (e.g., biweekly downloads) and times/conditions when data should be ignored or treated with caution.

## Data landscape
- System components
  - Tensiometers installed at various depths (notably 10 cm, 30 cm, 50 cm) across plots.
  - OLF (overland flow) traps with tipping buckets, gutters, and associated tubes.
  - Delta T loggers and Delta T batteries/desiccants.
  - Tinytag data loggers and control/logging hardware.
  - Pumps, batteries, desiccants, and degassing processes.
- Plots and setup
  - Multiple plots (e.g., plots 1–4 and subplots like 4.1, 4.2, 4.3) with associated gutter systems and OLF infrastructure.
  - Regular maintenance actions: degassing, calibration, cage cleaning, grass cutting, trenching, and system reconfiguration when needed.
- Data types and events
  - Continuous sensor readings (tensiometer values, Delta T data, tipping bucket counts).
  - Calibration events and troubleshooting notes (recalibration after tipping bucket issues; channel mapping changes; reed switches, and wiring adjustments).
  - Data download and synchronization events; clock adjustments and occasional clock drift corrections.
  - Ancillary observations: battery levels, pump functionality, pump replacements, blockages, water in pits, vole damage, algae, and debris in gutters.
- Data quality notes
  - Frequent data gaps or dubious readings during storms, electrical surges, and logging clock issues.
  - Occasional data corruption: “data downloaded … not correct,” “logger had stopped logging,” “double tipping,” and “tips not recording” during calibration or wiring events.
  - Inconsistent data due to hardware changes (channel reassignments, reed switch issues, external vs. internal power settings).

## Data quality, provenance, and governance considerations
- Provenance and traceability
  - Comprehensive field logs linking events to specific hardware actions, calibration events, and maintenance activities.
  - Detailed timestamps for installations, repairs, and data issues, enabling audit trails for data quality problems.
- Metadata and standards
  - Rich operational metadata (plots, sensor depths, device types, gutter configurations, OLF components) but no formalized data standards or schema described.
  - Occasional guidance on data treatment (e.g., ignore tips during certain times; time calibrations; calibration notes) indicating a need for consistent data curation rules.
- Data quality challenges to address
  - Power reliability: frequent battery changes and desiccant management; some loggers stop due to battery or connection problems.
  - Connectivity and wiring: recurrent reed switch, channel wiring, and external/internal power configuration issues.
  - Physical interference: vole damage, debris, and blockages in gutters/pipes; algae and green matter inside connectors.
  - Environmental factors: storms causing electrical surges or data anomalies; data drift due to clock misalignment.
  - Calibration integrity: need for ongoing calibration and validation of tipping bucket counts; occasional double tipping and miscalibration requiring re-calibration.
- Observed data management gaps
  - Recommendations to shift to biweekly downloads to mitigate data loss between checks.
  - Note to ignore certain tips tied to calibration runs or known test periods to avoid contaminating data.
  - Post-hoc data cleaning required to align channels and correct for known hardware issues.

## Data infrastructure, operations, and maintenance patterns
- Operations cadence
  - Regular field visits for maintenance, calibration, and troubleshooting.
  - Periodic data downloads with observations about data integrity (some downloads show inconsistencies that require investigation).
- Maintenance activities
  - Degassing and recalibration of tensiometers; replacement of batteries, desiccants, and pumps.
  - Physical repairs: re-wiring, reed-switch replacements, sump/tipping bucket adjustments, gutter repairs, and trench widening.
  - System reconfiguration in response to problems (e.g., relocating channels, swapping tensiometers, installing new loggers or decoupling external power).
- Data handling practices
  - On-site notes about data reliability and events that should be disregarded (e.g., certain tips as calibration artifacts or test runs).
  - Occasional explicit instructions to download data biweekly or to re-check data after hardware changes.

## Key takeaways for Data Leaders
- Data completeness and reliability are highly sensitive to hardware integrity and power management; ensure robust, redundant power and monitoring of battery health.
- Data quality needs formal governance
  - Implement standardized metadata schemas (device IDs, depths, plots, logger types, channel mappings).
  - Maintain a central data quality log capturing calibration events, channel reassignments, and known data issues with timestamps.
- Data provenance and traceability should be strengthened
  - Link every data segment to a specific maintenance action or hardware change to facilitate post-processing reconciliation.
- Data management practices should be standardized
  - Establish routine calibration protocols, validation checks, and automated flagging of anomalous data (e.g., clock drift, miscalibrated tipping buckets).
  - Define fixed data retrieval cadences (e.g., biweekly downloads) and documented rules for when to ignore or trust certain data segments.
- Risk and disruption planning
  - Prepare for environmental and animal-related interference (vole damage, debris, weather-induced data gaps) with protective enclosures and monitoring of connectors.
  - Create maintenance playbooks for rapid fault isolation (e.g., channel miswiring, reed switch faults, external vs. internal power issues).
- Data usage and integration
  - Align ongoing field practices with a wider data strategy to feed downstream analyses (soil moisture dynamics, infiltration experiments, and hydrological modeling).
  - Ensure calibration and data cleaning steps are reproducible and auditable for cross-team collaboration.

## Recommendations and next steps
- Establish a formal data governance plan covering metadata standards, data quality checks, and versioning.
- Implement a centralized log of maintenance actions mapped to data timestamps to improve traceability.
- Standardize calibration, degassing, and calibration validation procedures; lock in channel mappings to minimize post-hoc corrections.
- Introduce automated alerts for sensor/pump failures, battery health, and clock drift to reduce data gaps.
- Review and standardize data download cadence (e.g., biweekly) and validation procedures to ensure timely, clean data feeds.
- Develop a risk mitigation strategy for environmental interferences (vole damage, weather effects) with improved physical protections and backup components.