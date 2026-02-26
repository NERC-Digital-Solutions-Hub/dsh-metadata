# Overland flow in the tree planted shelter belt

## Overview
- Two overland flow traps installed in a tree shelter belt (5 m x 5 m).
- Monitoring period example: 12/04 – 21/04; overland flow as % of rainfall at RG3: Trap 1 = 15.9%, Trap 2 = 4.2%; bowl area = 19.75% for the same period.
- The record includes maintenance and data quality notes from 2006 to 2009, indicating ongoing instrumentation, calibration, and data integrity issues.

## Dataset content and structure
- Measurements and variables:
  - Overland flow as a percentage of rainfall (per trap)
  - Rainfall measurement at RG3 (reference rainfall)
  - Tipping bucket (TB) loggers with calibrations (TB1, TB4, TB5; e.g., TB1 = 169.5 ml/tip; TB4 = 185.2 ml/tip)
  - Tiny tag loggers and related timing data
- Observational/maintenance events (examples):
  - Gutter guide plastic damage and repairs; reinsertions and patching
  - Cleaning gutters of leaves/soil; reinstalling edging
  - Covers placed on gutters to reduce direct rain input
  - Replacements and repairs of pipes, drains, and buckets; some components upgraded to stainless steel
  - Periodic blockages and subsequent unblocking; device recalibration
- Temporal coverage and notes:
  - Entries span 2006–2009, with multiple maintenance actions and calibration updates
  - 31/11/08 note (likely a date formatting error) and other timestamps requiring alignment
- Metadata cues:
  - Trap identifiers (Trap 1 left, Trap 2 right), location context, and notes on soil texture differences despite adjacency
  - Descriptions of installation conditions and environmental factors (ground unevenness, livestock interaction)

## Data provenance and metadata
- Data sources:
  - Rainfall data from RG3 used to compute % of rainfall for OLF
  - OLF readings from two traps, complemented by TB loggers and tiny tag loggers
- Provenance details:
  - Maintenance and device history (repairs, recalibrations, replacements) documented alongside readings
  - Calibration records for TB loggers documented prior to installation
- Data lineage:
  - Raw readings from loggers with subsequent cleaning/interpretation notes; time stamp adjustments made to account for BST/GMT changes

## Data quality and issues
- Timestamp and time alignment:
  - Reports of time stamp issues and BST/GMT transitions requiring adjustments
  - Last monitoring period flagged as potentially lower data quality due to time misalignment
- Sensor and hardware reliability:
  - Leaks in down pipes, disconnected barrels, and blockages in tipping buckets
  - Gutter and pipe integrity problems necessitating repairs and replacements
- Measurement reliability:
  - Blockages caused buildup and sudden large readings
  - Physical damage and wear affecting data capture (e.g., gutter guides, soil contact)
- Data gaps and continuity:
  - Series interruptions due to maintenance events and hardware failures
  - Need for careful annotation of gaps and anomalies in datasets

## Data governance and stewardship implications
- Metadata and standardization:
  - Require clear device identifiers, installation dates, calibration constants, and maintenance actions
  - Define units and references (e.g., % rainfall, ml/tip, rainfall at RG3)
- Data quality controls:
  - Regular checks for blockages, leaks, and sensor integrity
  - Robust handling of time stamps, BST/GMT transitions, and download overlaps
  - Explicit annotation of data gaps and anomalous periods
- Data storage, sharing, and cataloging:
  - Upload to appropriate data portals with a metadata-rich record
  - Catalogue fields should capture location, sensors, period, data quality notes, and maintenance history
  - Document data cleaning and processing steps to preserve provenance
- Recommendations for improve usability:
  - Adopt a standardized data schema for ecological monitoring datasets
  - Separate raw data from processed data with a clear provenance trail
  - Link maintenance logs to corresponding data quality notes and timestamps
  - Plan for routine post-rain data checks to ensure timely data availability

## Challenges and considerations for Data Stewards
- Understanding user needs for such niche, multi-sensor datasets
- Ensuring timely data delivery and integration across devices
- Ensuring data creators meet metadata and calibration standards
- Handling interoperability across multiple formats and large-time-series datasets
- Managing hardware evolution (loggers, sensors, and calibration methods) over long-term datasets