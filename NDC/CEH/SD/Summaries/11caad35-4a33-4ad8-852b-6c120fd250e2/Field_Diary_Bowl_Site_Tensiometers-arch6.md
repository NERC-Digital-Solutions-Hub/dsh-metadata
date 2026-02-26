# Delta-t logger data in the bowl study area

## What this dataset is and how it was collected
- Data downloaded from a Delta-t logging system in the bowl study area.
- Contains tensiometer readings at multiple depths (10 cm, 30 cm, 50 cm) across various transects, cages, and bowls.
- Time span covered by the log entries ranges from 2004 to 2009, with ongoing maintenance and data management events throughout.
- Entries document operational events (degassing, vent exposure, recalibration, reinstallation), field maintenance (grass cutting, cage adjustments), and experimental notes (plant and animal interactions).

## Key measurements and components
- Tensiometers at depths of 10 cm, 30 cm, and 50 cm.
- Multiple locations: bowl-based and cage-based setups (e.g., T2.1, T2.3, T1.2, 2.2, etc.; various transect points).
- Delta-t data logging hardware (DL6 loggers) and associated wiring, batteries, and program settings.
- Recording notes include data points, calibration references, and any observed data integrity issues.

## Data quality issues and maintenance highlights
- Data gaps and integrity issues:
  - Initial data missing due to logger auto-wrap; need to ensure overwrite mode is enabled for continuous data capture.
  - 03/11/08: Data download from the top cage corrupted; not available.
  - Periodic data gaps from logger timing, battery issues, and communication problems.
- Equipment and environmental challenges:
  - Repeated incidents of sheep damage to cages, tubing, and wiring; some tensiometers removed or chewed.
  - Vents exposed or buried; frequent vent checks and exposure cleanup.
  - Earthworms and moles affecting vent positions and data quality.
  - Grass growth and mowing affecting cage access and data collection.
- Calibration and offset adjustments:
  - Installation changes: tensiometers installed at approximately 15° angle relative to ground; introduced a depth offset of -4.8 cm applied to measurements to account for cup depth and angle.
  - 25/11/08: Offset adjustments reverted from -4.8 cm to 0 cm in both loggers after re-evaluation.
  - 16/10/08 to 03/11/08: data offset and installation geometry documented; subsequent offsets embedded in logger program to reduce post-download processing.
- Data logging and processing settings:
  - Delta-t logger programming changes (warm-up period adjustments, overwriting behavior).
  - Rewiring the Delta-t logger to ensure negative mV readings correspond to negative pore water pressure values (revised wiring polarity in 2007).
  - Periodic recalibration and reinstallation of tensiometers after maintenance events.

## Data handling, processing, and interpretation notes
- Cleaning and preparation actions:
  - Regular degassing of tensiometers and vent checks.
  - Replacement and repair of damaged tubing, cups, and wiring; reinstallation of tensiometers after incidents.
  - Calibration checks and lab verification of removed tensiometers where needed.
- Documentation of data modifications:
  - Offsets and installation geometry details recorded to align measurements with actual depths.
  - Observed data irregularities (e.g., “data funny” in Delta T readings) noted and addressed with hardware changes (new set of tensiometers, different installation angle).
- Data continuity and future reliability considerations:
  - 30/07/09: Bottom tensiometers not responding to the logger despite battery changes; may indicate hardware or logger communication failure needing investigation.
  - Ongoing need to ensure overwrite mode is active to minimize start-period data gaps and to embed depth-angle offsets in the logger for streamlined downstream analysis.

## Notable events affecting data continuity
- Repeated animal interference (sheep, moles) prompting cage reinforcements and sealant/tube replacements.
- Mechanical issues with Delta-t logger and batteries leading to data interruptions or corrupted downloads.
- Orientation and depth-specific adjustments to tensiometer installation requiring recalibration and offset updates.
- Periodic data quality reviews resulting in reinstallation and re-calibration of tensiometers to preserve data integrity.

## Current status and actions required
- As of 30/07/09, bottom tensiometers show no response from the logger despite battery changes; requires diagnostics of logger-tensiometer communication or hardware integrity.
- Prior offsets (-4.8 cm) were removed or re-applied based on reinstall geometry; confirm final offset strategy for downstream analysis and embed in data processing pipeline if possible.
- Ongoing maintenance and verification recommended to maintain data continuity, including:
  - Ensuring overwrite mode is consistently enabled.
  - Continuation of vent checks, degassing, and protective measures against animal interference.
  - Regular data quality checks for missing segments and anomalous Delta T readings.