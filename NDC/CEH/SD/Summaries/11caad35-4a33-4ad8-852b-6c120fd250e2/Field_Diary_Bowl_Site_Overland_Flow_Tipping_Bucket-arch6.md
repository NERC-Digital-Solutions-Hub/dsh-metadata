# Overland Flow and Tipping Bucket System Maintenance and Calibration Log

## Purpose and data products
- Document the operation, maintenance, calibration, and data handling of the overland flow (OLF) monitoring system, including tipping buckets (TB), weir boxes, tinytags, and transducers.
- Aims to enable data-driven understanding of flood/runoff events and support data quality through calibration, cleaning, and self-serve outputs (dashboards/plots) when possible.
- Notes ongoing efforts to keep raw data unedited while creating cleaned, usable datasets for analysis.

## Instrumentation and data collection
- Key components:
  - Tipping buckets (TB) with magnet/reed switch sensors
  - TinyTags for OLF and drain measurements
  - Weir boxes and associated downpipes for flow measurement
  - Transducer/logger housing and related cabling
- Time interval management:
  - 22/04/04: Time interval reset from 10 to 5 minutes to avoid overflow in TB logger (255)
  - 31/03/05: Interval reduced to 4 minutes
- Calibration and data formats:
  - TB calibration and calibration checks used to convert tips to volume (initially 1 tip ≈ 1 L; later revised)
  - Raw data edited to reduce file size; raw datasets remain unedited

## Calibration results and data processing rules
- 19/05/05: TB recalibrated to 2 L per tip; some data removed when no tip recorded in a given interval; raw data preserved
- 07/06/07: Calibration check: 30 L through TB produced 15 tips + 1.36 L remaining => 1.90933 L per tip
- 21/08/07–23/01/08: TBs reinstalled/repaired after magnet issues; multiple re-installations and recalibrations
- 14/11/08: Calibration event with TB crack found; data adjusted
- 02/12/08: TB reinstalled; time baseline corrected (BST vs GMT)
- 11/06/09: TB calibration result: 30.54 L ≈ 16 tips ≈ 1.9 L/t

- Volume adjustment over time:
  - 07/06/07 TB volume ~1.909 L/t (from calibration)
  - 14/11/08 calibration indicated changes; then 30.76 L = 17 tips => ~1.81 L/t
  - 02/12/08 reinstalled TB and applied updated calibration
  - 17/11/08 and subsequent entries note applying a linear incremental change to tip volume to reconcile differences from earlier calibration

## Data quality, gaps, and corrections
- Timestamp and interval issues:
  - Occasional time stamp issues (e.g., 30/10/08) and deliberate ignores during calibrations or data-diversion events (e.g., 10:24–13:00 GMT in Oct 2008)
- Data integrity checks:
  - 29/06/06: Last 3 drain entries incorrect (no tips)
  - 21/04/06: Transducer mounting issues; noted need for improvement
  - 21/08/06 and 28/09/06: Battery failures and cleaning/dislodgement of components
- Data cleaning practices:
  - Ignore data during TB recalibration, weir box calibrations, or when known disturbances occurred (e.g., 09/05/08–12/05/08; 24/10/08–31/10/08)
  - Some periods identified as noisy or unreliable due to hardware issues (vole damage, gully blockages)
- Disturbances affecting measurements:
  - Vole/mole damage to OLF trap; damaged gutters; bark/clay repairs; holes above guttering corrected (early 2007)
  - Blocked drains and downpipes causing overflow or reduced readings (e.g., 19/01/08)
  - Weir box calibrations and sediment buildup affecting measurements (late 2006–2008)
- Hardware maintenance:
  - Replacements and reattachments of TB magnets, reed switches, batteries, seals, and desiccants
  - Weir box repairs, drain pipe cleaning, and occasional cover improvements to reduce seepage

## Maintenance events and responses
- Structural and device repairs:
  - OLF trap damaged by voles (25/07/05); repairs followed by recalibration
  - Mole burrow impacts addressed (11/04/06); clay and soil fixes to prevent leakage
  - Weir box issues and sediment management (2006–2008)
- Sensor reliability improvements:
  - Regular TB reinstallation and magnet fixes (2006–2009)
  - Transducer alignment and waterproofing improvements (21/04/06)
  - Battery replacements and periodic system reboots (2006–2009)
- Ancillary system enhancements:
  - Consideration of a drain cleaner and potential grate to prevent blockage at the TB inlet (09/09/06 notes)
  - Gatekeeping and covers added to reduce unintended TB activation during rainfall

## Outputs, usage, and recommendations
- Data products:
  - Cleaned TB-derived discharge estimates (volume per tip), TB counts, and calibrated TB volume used to estimate flow
  - Weir box and tinytag datasets for cross-validation of OLF and drain data
- Usage considerations:
  - Maintain documentation of calibration campaigns and data exclusion windows
  - Continue to log hardware issues and their impact on data quality for transparent datasets
- Recommendations implied by the log:
  - Implement more robust physical protections (e.g., grate at inlets, reinforced guttering) to reduce vole-related damage
  - Improve transducer mounting stability and environmental sealing
  - Regular calibration checks with explicit update of tip-volume parameters and propagation into datasets
  - Maintain clear notes on data exclusion periods to support reproducible analyses
  - Consider automation or tooling to flag irregular intervals, calibration events, and potential timestamp anomalies for faster data QA