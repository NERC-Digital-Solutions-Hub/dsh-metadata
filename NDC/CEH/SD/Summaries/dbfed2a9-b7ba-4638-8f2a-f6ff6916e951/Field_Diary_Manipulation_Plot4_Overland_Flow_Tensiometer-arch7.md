# Penllywn: Notes from field visits for tensiometers and OLF

## Overview
- Long-running field log (2005–2009) of tensiometer and overland flow (OLF) monitoring at Penllywn.
- Captures start-up tips, routine testing, sensor and equipment status, data downloads, maintenance, and issues encountered.
- Useful for GIS work as it links spatially referenced plots and equipment to time-stamped sensor data and events.

## Instruments, setup and spatial context
- Sensors and equipment:
  - Tensiometers at multiple depths (e.g., 10 cm, 30 cm, 50 cm).
  - OLF traps with tipping buckets (TB) and associated gutters.
  - Delta-T data loggers and Tinytag loggers; various pumps and batteries; desiccants; calibration references.
- Spatial layout cues:
  - Mentions of plots (1, 2, 3) and plots 4.1, 4.2, 4.3; control vs treatment plots; trenches and pits coordinated around the plots.
  - References to diagrams in a separate book for plotting and flow paths.

## Data collection, processing and QA
- Data collection activities:
  - Regular data downloads, degassing, battery/desiccant changes, and pole/gear calibration.
  - Calibration activities for tipping buckets; periodic degassing of tensiometers.
- Data quality and reliability issues:
  - Storm events causing electrical surges and nonsensical readings.
  - Frequent power and logging problems: depleted batteries, desiccant exhaustion, clock drift, and loggers stopping.
  - Sensor/connection faults: reed switches, wiring problems, bad channels, loose connections, kinked tubes, and pumps failing or blocking.
  - Data integrity problems: water in pits, sediment/vole damage, algae in ports, gutter blockages, double tipping, and data anomalies requiring ignoring certain periods or recalibration.
  - Periods flagged as tests or non-representative; some data explicitly marked to be disregarded.

## Maintenance, troubleshooting and calibration practices
- Routine tasks:
  - Degassing tensiometers; cleaning and cutting grass; vent inspections; recalibration of TBs; battery and desiccant replacement.
  - Pump maintenance, wiring repairs, reed switch replacements, and channel reconfigurations on Delta-T loggers.
  - Data integrity checks following hardware changes; occasional re-downloading and re-checking data.
- Documentation and guidance:
  - Frequent notes indicate which data windows to ignore and reference to diagrams or logs for proper interpretation.
  - Emphasis on verifying data after hardware changes before use in analyses.

## Data management implications for GIS
- Metadata and data provenance:
  - Need to capture sensor type, depth, plot location, and exact timestamps; maintain notes about calibration events and hardware changes.
- Data quality flags:
  - Record instances to ignore (test runs, known issues), battery/power downtimes, and periods of suspected data corruption.
- Spatial integration:
  - Align sensor data with plot-level GIS layers (plots, trenches, TB locations, gutters, OLF traps) to enable meaningful maps and time-series visualizations.
- QA/QC workflows:
  - Implement consistent QC steps to filter out erroneous periods, annotate calibration events, and document data cleaning decisions for GIS consumption.
- Recommendations for GIS-ready outputs:
  - Keep biweekly or regular data exports with accompanying metadata and flags.
  - Preserve a log of equipment replacements and sensor relocations to support spatial accuracy over time.

## Endnotes
- The notes span 2005–2009, reflecting persistent operational and data-quality challenges across multiple devices and plots.
- The detailed field diary underscores the importance of robust metadata, QA/QC, and clear documentation to produce reliable GIS-based data products from complex, multi-sensor time-series field data.