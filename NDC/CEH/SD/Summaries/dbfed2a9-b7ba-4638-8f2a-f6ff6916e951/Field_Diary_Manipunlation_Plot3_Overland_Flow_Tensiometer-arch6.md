# Tyn y Fron: Notes from field visits for tensiometers and OLF

- A detailed field log (2005–2009) of maintenance, data collection, and troubleshooting for tensiometers and overland flow (OLF) traps, including Delta-T loggers, Tinytags, and associated pumps, batteries, and sensors across plots (1, 2, 3).

## Overview

- Documents daily/periodic actions to attach, degas, calibrate, repair, and download data from tensiometers (at 10 cm, 30 cm, 50 cm depths) and OLF tipping buckets.
- Records data streams (tensiometer readings, tipping-bucket tips, Delta-T logger data, Tinytag logs) and situational notes that affect data quality (storms, floods, equipment faults, wildlife interference).
- Highlights the ongoing need to interpret data quality, separate reliable signals from field issues, and maintain self-serve data outputs and dashboards.

## Data collection and instruments

- Instruments and data streams:
  - Tensiometers in plots (depths: 10 cm, 30 cm, 50 cm); devices degassed and recalibrated as needed.
  - OLF traps with tipping buckets; reed switches and associated wiring; regular degassing and maintenance.
  - Delta-T loggers and Tinytags (TinyTag) for pump and water event measurements.
  - Pumps, battery systems (big batteries), and desiccants; gutters and trenches for drainage.
- Data products and access:
  - Logged readings used to derive soil water status and overland flow events; data downloaded during visits; occasional notes to ignore certain tipping events or periods (e.g., after sampling, during storms, or when components were disturbed).
  - Field notes cross-validate logger outputs with on-site observations and manual measurements.

## Data quality issues encountered

- Sensor and data reliability challenges:
  - Storm events causing electrical surges leading to nonsensical, identical readings across sensors.
  - Data gaps due to pump outages, battery failures, and data download interruptions (e.g., gaps around 27/11/05; 5–7/12/05; 28/02/06).
  - Frequent maintenance must-dos: degassing tensiometers, re-installing sensors after movement, and recalibration (notably 2006).
- Hardware and access problems:
  - Cages damaged or displaced; cables cut or chewed; tensiometer tubes dislodged; reed switches failing; tipping buckets misaligned after field work.
  - Wildlife and weather impacts: vole/bird damage to gutters and covers; overland flow from heavy rainfall flooding pits; gutter covers and trench integrity degraded.
- Data interpretation pitfalls:
  - Times and periods required to be ignored (e.g., during sampling, after 09:00–11:00 BST events; tips between certain hours; periods of known calibration or maintenance).
  - Occasional “default” program reinstatements on Delta-T leading to non-useful data until corrected.
- Calibration and recalibration:
  - Recalibration needed for tipping buckets (May 2006; later adjustments after faults), and multiple replacements of tensiometers and sensors over the years.
  - Issues with Tinytags and tiny tags requiring replacement or reattachment; calibration notes recorded for plots 1 and 2 in early 2008.

## Data management practices

- Documentation and cross-validation:
  - Continuous field notebooks accompany instrument data to explain anomalies, maintenance actions, and any data to be ignored.
  - Regular data downloads with notes on sensor status, battery levels, and calibration needs.
- Data quality safeguards:
  - Explicit notes to ignore certain tips or data windows during troubleshooting, sampling, or post-maintenance periods.
  Alternative data streams (Tinytag, Delta-T) used to corroborate or identify inconsistencies.
- Inventory and maintenance workflow:
  - Track battery replacement and pump status; reinstallation of tensiometers after transport or disturbance; replacement of damaged cables and tubes.
  - Periodic trench enlargement and gutter repair to prevent water overtopping and data corruption.

## Timeline of key events (highlights)

- 2005: Storm events cause data anomalies; initial attention to degassing and reinstallation; early data gaps noted (e.g., 27/11/05; 5–7/12/05).
- 2006: Ongoing maintenance (batteries replaced, wiring changes, degassing), frequent data gaps and pump issues documented; recalibration efforts begin.
- 2007: Regular sensor checks; Tinytag/delta-T calibration and data integrity checks; several episodes of full pits and pump adjustments.
- 2008: Major field disturbances (flooding, heavy rainfall) prompt pit enlargement, gutter repairs, and repeated recalibrations; several episodes of Delta-T program resets requiring reupload.
- 2009 (through 18/08/09): Continued validation and recalibration; updated sensor statuses and depths recorded for plots M3.1 and M3.2; M3.3 status less complete at this point.
- Notable data points near 18/08/09:
  - M3.1: 10 cm = 222; 30 cm = 242; 50 cm = data not specified.
  - M3.2: 10 cm = 171; 30 cm = 201; 50 cm = 258.
  - M3.3: data status not fully recorded in this entry.

## Current status and data readiness

- As of 18/08/2009:
  - Plots M3.1 and M3.2 have recorded tensiometer measurements at multiple depths with corresponding tipping-bucket or logger data; some depths (e.g., M3.1 at 50 cm) lack complete data in this log.
  - Pits and trenches have required ongoing maintenance (drains, gutters, sump covers, and vent clearing) to sustain data collection.
  - Data quality is contingent on ongoing calibration, battery health, and mechanical integrity; some events require data exclusion or careful interpretation.

## Implications for data support

- Ensure robust data validation and flagging:
  - Implement automated flags for storms, pump outages, battery failures, and calibration events to separate reliable data from field-induced artifacts.
- Strengthen maintenance and data pipeline:
  - Establish a standardized battery replacement schedule and spare parts inventory; document sensor replacements and calibration in a centralized schema.
- Improve data integration:
  - Align timestamps and event logs across Delta-T, Tinytag, and tipping-bucket data to reduce reconciliation effort.
- Promote data usability:
  - Create self-serve dashboards summarizing plot-level soil water status and overland flow events, with annotations for known data gaps and maintenance windows.