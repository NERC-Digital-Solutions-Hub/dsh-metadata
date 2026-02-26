# Tyn y Fron: Notes from field visits for tensiometers and OLF

## Overview
- A detailed, year-by-year field log (2005–2009) documenting management, maintenance, and data issues related to tensiometers, overland flow (OLF) traps, loggers (Delta-T), Tinytags, batteries, pumps, and related field equipment at Tyn y Fron.
- Captures how environmental conditions, equipment failures, and animal interference impacted data collection and data integrity.
- Serves as a record of data provenance, calibration, and corrective actions to support data governance and reuse.

## Data collection systems and data types
- Instruments and data streams involved:
  - Tensiometers at multiple depths (10 cm, 30 cm, 50 cm) per plot.
  - OLF (overland flow) tipping buckets with associated gauges and sensors.
  - Delta-T loggers and Tinytags for recording environmental/tipping events.
  - Pumps, gutters, and sump systems supporting OLF traps.
- Data characteristics and handling:
  - Regular data downloads and degassing/maintenance actions.
  - Frequent battery changes and equipment recalibration.
  - Observations of sensor status, wiring, and alignment (e.g., reed switches, tubing, vent checks).
- Data quality issues identified in the field:
  - Storm events causing non-sensible sensor readings across all sensors.
  - Periods where data needed to be marked as ignored due to equipment state or sampling activities.

## Data quality and integrity issues encountered
- Sensor and data anomalies:
  - July–August 2005: storm-induced electrical surge suspected to cause uniform nonsensical readings.
- Data gaps and incomplete records:
  - Multiple instances of missing or corrupted data due to pump battery depletion, logging interruptions, or data download problems (e.g., 27/11/05 gap; 9/2007–early 2008 data irregularities).
  - Delta-T and Tinytag data occasionally stood on default or corrupted programs after battery changes, requiring reinitialization.
- Maintenance-driven retuning:
  - Reinstallations and recalibrations after field events (plots 3.1–3.3; various depths).
  - Calibration attempts for tipping buckets and tensiometers to ensure data consistency.
- Data curation practices:
  - Explicit notes to ignore tips or data during specific windows (e.g., during sediment sampling, calibration, or known anomalies).
  - Documentation of calibration values and data quality flags in field notes.

## Data governance, maintenance, and lifecycle
- Maintenance cadence and actions:
  - Regular degassing of tensiometers, battery replacements, and recalibrations.
  - Reinstallation of tensiometers after misalignment or damage (e.g., cables, tubing, or cages moved by animals).
  - Repairs to OLF gutters, sump covers, and lawn edging to prevent data contamination from water inflow or cross-flow.
- Data provenance and traceability:
  - Detailed, timestamped records of each action (attachment/detachment, battery changes, calibration, data download, and issues observed).
  - Cross-referencing notes with plots, depths, and devices (e.g., Plot 3.1, 3.2, 3.3; 10 cm, 30 cm, 50 cm).
- Data quality interventions:
  - Recalibration and replacement of sensors when data anomalies were detected.
  - Re-downloads and data cleaning when Tinytag or Delta-T became unreliable or stopped logging properly.
- Governance implications:
  - The notes demonstrate the need for robust metadata, explicit data quality flags, and a clear policy on when to ignore data.
  - Importance of maintaining equipment integrity to minimize data gaps and ensure long-term usability for analysis.

## Metadata, provenance, and documentation
- Comprehensive field notes capture:
  - Dates, times, plot identifiers, sensor depths, and specific actions (degassing, calibration, battery changes, repairs).
  - Observations about environmental conditions (heavy rainfall, flooding, vegetation management) and animal activity (sheep, voles, birds, fox/badger interactions).
- Provenance tracked through sequential entries:
  - Each entry documents the context and rationale for subsequent data handling decisions (e.g., ignoring tips, recalibration events, or data corrections).

## Data availability, storage, and accessibility
- Data storage and access paths:
  - Data initially stored on loggers (Delta-T, Tinytags) and on field laptops; occasional recovery and re-access via Bangor (institutional reference).
- Data accessibility challenges:
  - Periodic data loss or corruption requiring recovery, re-downloads, or replacement of hardware components.
  - Laptop/program issues leading to periods of default configurations or missing data until corrected.
- Data integrity considerations for reuse:
  - Need for clear documentation of which data were ignored or flagged due to anomalies.
  - Reliance on meticulous metadata to enable future researchers to understand data gaps and corrective actions.

## Key challenges and mitigations (summary)
- Environmental and hardware risks:
  - Storm events, floods, and animal interference causing data disruption and physical damage to equipment.
- Data integrity risks:
  - Sensor miscalibration, battery failures, and software resets leading to unreliable or default-era data.
- Operational responses:
  - Frequent maintenance (degassing, recalibration, replacements), extensive logging of actions, and explicit data-flagging to guide data cleaning.
- Governance lessons:
  - The need for robust metadata standards, consistent calibration protocols, and clear guidance on when data should be ignored or treated with caution.

## Implications for data stewards
- Maintain thorough, timestamped provenance for all field data and maintenance actions.
- Establish and enforce metadata standards to capture device type, depth, plot, calibration status, and data quality flags.
- Implement clear data quality rules, including explicit ignore periods and documentation of anomalies.
- Plan for equipment redundancy and rapid recovery procedures to minimize data gaps.
- Ensure data storage solutions support long-term accessibility and traceability, with documented recovery paths from hardware or software failures.
- Use field notes to contextualize data and support reproducibility and auditability of data clues and corrections.