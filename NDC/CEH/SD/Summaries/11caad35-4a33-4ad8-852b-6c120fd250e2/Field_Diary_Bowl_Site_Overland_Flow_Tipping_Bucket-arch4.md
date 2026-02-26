# Log of tipping bucket, overland flow and related field instrumentation

## Overview
- Describes a long-running field data collection effort monitoring tipping buckets (TB), overland flow (OLF), drain flow, and a weir box, including calibrations, maintenance, and data quality notes from 2004–2009.
- Aims to document how data collection, instrument status, and calibration decisions impact data reliability and usability for analysis and interpretation.

## Instrumentation and data flow
- Key components:
  - Tipping buckets (TB) with magnets and reed switches; magnet failures/replacements documented.
  - Tiny tags / Tinytags for data logging; time stamps and recording intervals adjusted over time.
  - Overland flow (OLF) trap and associated guttering, pipes, and downpipes; occasional blockages and sediment issues.
  - Weir box measuring drain flow; calibration events and channel issues noted.
- Time interval management:
  - Recording interval reduced from 10 to 5 minutes, then to 4 minutes to prevent logger overload.
  - 5-minute interval re-established later; ongoing adjustments around calibration events.
- Calibration and measurement units:
  - Initial calibration: 30 L through TB yielded 15 tips (1.0 L per tip).
  - Later recalibration: tip volume adjusted to ~1.909 L (15 tips from 30 L → 1.909 L/t).
  - Final calibration reference: 30.54 L ≈ 16 tips → 1.9 L/t.
- Data handling:
  - Raw data sets retained unedited; some entries removed to reduce size or exclude non-recorded tips.
  - Data downloads for drain, OLF, and TB with attention to incorrect entries during certain periods.

## Calibration, data quality, and metadata practices
- Calibration discipline:
  - Regular calibration checks (e.g., pouring known volumes) to validate tip volumes.
  - Documentation of changes to tip volume over time and the rationale (e.g., instrument wear or measurement drift).
- Data quality controls:
  - Specific time windows ignored during calibration or maintenance (e.g., between 13:30–14:30 or other calibration periods).
  - Indications of data to ignore due to transducer handling, calibration, or equipment being moved.
  - Noted discrepancies between datasets (e.g., last entries from drain data incorrect) requiring exclusion from analysis.
- Metadata and traceability:
  - Detailed notes on instrument positioning, sensor seating, and mounting challenges.
  - Logging of issues that affect data (vole damage, sediment, blockages, weather-related disturbances).
  - Observations on timestamp alignment, time zone changes (GMT/BST), and reinstallation dates.

## Maintenance and operational incidents
- Physical issues:
  - Vole/vole damage to OLF trap; structural repairs and re-sealing with soil and clay.
  - Cracks and misalignment in tipping buckets; magnets falling off; reed switch replacements.
  - Weir box adjustments, pipe blockages, and sediment buildup requiring cleaning or rerouting.
- Repairs and replacements:
  - TB reinstalled and recalibrated multiple times; battery swaps, seal and desiccant changes.
  - Weir box and transducer adjustments to improve measurement stability.
  - Downpipes and gutters cleared; sediment and debris management implemented.
- Operational notes:
  - Periods of “system frozen” and other anomalies requiring reinitialization or re-downloads.
  - Calibration-driven adjustments to ensure consistency across data collection sessions.

## Data governance, implications for data leaders
- Data system overview:
  - The dataset demonstrates the importance of maintaining calibration continuity, metadata-rich logs, and transparent data cleaning practices.
- Data quality and usability:
  - Regular calibration, explicit ignore windows, and clear notes about data exclusion are essential for credible analysis.
  - Documentation of equipment problems and maintenance improves reproducibility and trust in downstream analyses.
- Coordination and standards:
  - The log highlights scattered data sources (TB, OLF, drain, weir box) and the need for cohesive metadata standards, consistent units, and cross-device synchronization.
  - Potential for shared best practices: calibration protocols, timestamp handling, and maintenance cadences.
- Recommendations for data leaders:
  - Maintain a centralized calibration and maintenance log linked to data records.
  - Define and enforce clear data exclusion rules with justification (calibration periods, sensor faults).
  - Preserve raw data alongside edited datasets and capture all transformation steps in metadata.
  - Establish standardized units and conversion schemes (e.g., fixed tip volumes) with versioned records.
  - Document time zone handling and any timestamp adjustments to ensure temporal alignment across devices.