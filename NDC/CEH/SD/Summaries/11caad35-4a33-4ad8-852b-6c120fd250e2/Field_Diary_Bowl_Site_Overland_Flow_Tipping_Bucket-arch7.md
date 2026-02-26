Field log of tipping bucket, overland flow, drain flow and calibration notes

## Overview
- Longitudinal field log (2004–2009) detailing tipping bucket (TB) measurements, overland flow (OLF) and drain flow, weir box instrumentation, transducers, and tinytags.
- Records calibrations, interval settings, maintenance, blockages, animal damage, and data quality actions relevant for GIS data products and map-based analyses.
- Highlights data integrity considerations needed for GIS use: interval changes, calibration revisions, time zone handling, and explicit data-cleaning windows.

## Data types and sensors
- Tipping bucket (TB) rainfall measurements with periodic calibrations and magnet/reed switch maintenance.
- Overland flow (OLF) measurements via TBs and OLF-specific channels.
- Drain flow measurements linked to weir boxes.
- Weir boxes and transducers subject to recalibration and positional issues.
- Tinytags for data logging and telemetry; several battery and download events recorded.
- Timekeeping devices and logs noting GMT/BST status and time-sync adjustments.

## Time intervals and data collection settings
- Interval changes to manage logger capacity:
  - 22/04/04: time interval reset from 10 min to 5 min.
  - 31/03/05: interval reduced to 4 min.
  - 03/10/06: reset back to 5-minute recording intervals.
  - 26/07/06: additional resets around data download.
- Calibration windows and their impact on data:
  - 19/05/05: TB recalibrated to 2 L per tip (previously 1 L per tip).
  - 07/06/07: calibration using 30 L to derive tip volume, yielding 15 tips and 1.36 L remainder (1.90933 L per tip).
  - 17/11/08: recalibration to account for TB crack and drift (1.81 L per tip for a period).
  - 02/12/08: note of a linear incremental change in tip volume (6 months after initial calibration) to be applied.
  - 11/06/09: final calibration noted as 30.54 L = 16 tips = 1.9 L/t.
- Time-zone handling:
  - Occasional notes to switch BST/GMT; 02/04/09 indicates a BST setting rather than GMT to be corrected later.

## Data quality, cleaning, and processing
- Data cleaning and editing practices:
  - 19/05/05: dataset being edited to reduce size; raw data to remain unedited.
  - Occasional note to ignore data during calibration, reinstallation, or when equipment was not operating correctly.
  - Examples: 29/06/06 (last 3 entries from drain data incorrect—no tips); 05/07/06 (ignore TB tips between 13:30–14:30); 24/10/08 and 31/10/08 (ignore periods during TB calibration and water diversion).
- Timestamp issues and corrections:
  - 31/10/08: time stamp issue resolved; some data periods marked to be ignored.
  - 24/03/09 and related entries indicate corrections and data integrity checks.
- Calibration/diversion events affecting data:
  - Water diverted from weir box during TB calibration periods; data flagged as affected.
  - Data flagged during weir box reinstallation and transport; data may be unreliable.
- Data volume management:
  - Multiple notes about downloading datasets and resetting logger times after downloads; some entries describe pruning to keep datasets manageable.
- Data reliability notes:
  - References to calibration checks and potential measurement drift (e.g., cracks in TB, magnet issues) requiring cautious interpretation of volumes and tips.

## Field maintenance and issues impacting data
- Animal damage and field hazards:
  - 25/07/05: overland flow trap damaged by moles/voles; accessibility issues with soil insertion.
  - 02/03/07–07/03/07: repeated TB magnet detachments; reinstallation and replacements.
  - 07/01/09: system freeze noted.
- Equipment and structural maintenance:
  - Weir box calibration and maintenance; downpipe blockages cleared; removal of sediment.
  - Gutter and downpipe issues addressed; holes near guttering filled; soil/stones used to repair vole damage.
  - TB and wiring issues: improvements to transducer fits, battery changes, desiccant, and seal replacements.
  - Sediment buildup and downpipe blockages occasionally caused data anomalies or flow diversion.
- Observational notes on flow behavior:
  - Situations where TBs and OLF channels behaved variably during rainfall, with flow circumventing expected paths (e.g., flow cracking through soil cracks).

## Implications for GIS data products
- Use caution with time-series alignment:
  - Apply the latest calibrated tip volume (≈1.9 L/t) and adjust historical data accordingly where calibration changes are documented.
  - Align datasets to a consistent time standard (GMT/BST) and flag periods with known time-zone adjustments or stamp issues.
- Data quality flags and cleaning windows:
  - Implement flags for calibration periods, data downloaded/reinstalled periods, and known diversions (e.g., TB calibration periods where data are diverted).
  - Exclude or separately label data blocks identified as affected by maintenance, calibration, or blockages (as noted in the log).
- Handling gaps and anomalies:
  - Document and map data gaps caused by vandalism, blockages, weir box recalibrations, and TB mechanical issues.
  - Include notes on periods explicitly marked “ignore data” for downstream analyses and map production.
- Rich context for interpretation:
  - The log contains essential metadata about equipment status (magnet, reed switch, battery), calibration results, and field conditions (vole damage, sedimentation, blockages) that are critical for interpreting spatially-referenced measurements.

## End summary
- The document is a comprehensive field log of TB, OLF, and drain-flow measurements with repeated interval changes, calibrations, and maintenance events over 2004–2009.
- Key data considerations for GIS use include calibrations of tip volume (notably around mid-2007 and late-2008), time-zone handling, data-cleaning windows around calibrations and diversions, and recurring maintenance issues (animal damage, sensor faults, and blockages) that introduce data gaps or quality flags.
- For reliable GIS-based analyses and map products, integrate calibration history, apply consistent time standards, and annotate data with flags describing calibration periods, data-diversion events, and known data-cleaning windows.