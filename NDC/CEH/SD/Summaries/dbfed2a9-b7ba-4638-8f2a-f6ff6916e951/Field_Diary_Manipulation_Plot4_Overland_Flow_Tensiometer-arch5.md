# Penllywn: Notes from field visits for tensiometers and OLF

- An extended field log (2005–2009) documenting tensiometer and overland flow (OLF) monitoring across multiple plots, including equipment maintenance, data collection, calibration, and data quality issues.

## Overview

- Tracks day-by-day observations, equipment status, data downloads, and actions taken to keep monitoring systems operational.
- Highlights recurring data integrity challenges, such as storms causing erroneous readings and frequent hardware/connection problems.

## Data collection systems and workflow

- Systems involved:
  - Tensiometers, OLF traps, tipping buckets (TB), Delta-T loggers, tinytags.
- Data handling:
  - Regular data downloads, calibrations, and degassing procedures.
  - Battery management (changes, desiccants), pump maintenance, and occasional power configurations (external vs. internal).
  - Channel assignments, reed switches, and logger wiring frequently adjusted; cross-checks between plots and devices.
- Data governance in practice:
  - Some data are flagged for exclusion (ignore tips, ignore certain time windows) due to operational issues or calibration steps.

## Data quality assurance and cleaning

- Common data issues observed:
  - Non-sensible readings during storms or electrical events.
  - Pumps and gutters blocked or degraded, leading to incomplete or inaccurate measurements.
  - Float switches, reed switches, and wiring faults causing misrecorded tips or missing data.
  - Pits and gutters filling with water; variable drainage affecting TB readings.
  - Timing issues: clocks behind, data gaps, or data needing re-calibration after battery or wiring fixes.
  - Biological/environmental interference: vole damage, debris, algae in connectors.
- QA/maintenance actions performed:
  - Degassing tensiometers, recalibrations of TBs, and frequent sensor replacements.
  - Rewiring, replacing batteries and desiccants, and installing new components (e.g., pumps, reed switches).
  - Biweekly or regular data checks and confirmations to minimize data loss.
  - Data cleaning steps indicated by “ignore tips” windows and documented exceptions.

## Metadata, provenance, and documentation

- Rich, timestamped field notes accompany data points, detailing:
  - Plot numbers, device IDs, and specific sensor configurations.
  - Conditions observed (water presence in pits, pump status, gutting issues).
  - Calibration values and calibration times, as well as data corrections or exclusions.
  - References to diagrams and books for plotting layouts and instrumentation.
- This metadata supports traceability of data corrections, sensor replacements, and methodological changes across the monitoring period.

## Data governance considerations and recommendations

- Data availability and limitations:
  - Frequent need to flag unreliable periods and exclude certain data to preserve dataset quality.
  - Regular download cadence is beneficial; biweekly downloads are suggested to minimize data loss.
  - External power considerations and battery health are critical for continuous data capture.
- Data lifecycle and stewardship:
  - Ongoing hardware maintenance (pumps, gutters, TBs, tensiometers) is integral to data continuity.
  - Comprehensive documentation of equipment changes, calibrations, and data corrections enhances future reuse and auditability.
  - Maintaining channel mappings and logger configurations is essential for cross-plot data comparability.

## Endnotes and observed patterns

- Recurrent technical challenges span multiple plots (notably plots in the 1.x and 4.x series), including:
  - Battery depletion, pump failures, and clogging or blockage issues.
  - Sensor drift, miscalibration, or wiring faults leading to mislogged tipping events.
  - Data integrity issues triggered by environmental factors (vole damage, debris, weather events).
- Emphasis on data integrity through explicit data exclusion windows and careful record-keeping of fixes and recalibrations.

## Key takeaways for Data Stewards

- Maintain thorough, timestamped field logs detailing equipment status, maintenance actions, and data corrections.
- Ensure robust data quality checks by documenting when data should be excluded or treated with caution.
- Track metadata comprehensively (devices, plots, channels, calibrations) to support reproducibility and cross-device comparability.
- Establish reliable data ingestion and backup practices, including planned download cadences and redundancy for critical sensors.
- Prepare for and document common failure modes (batteries, wiring, pumps) to minimize data gaps and support transparent data governance.