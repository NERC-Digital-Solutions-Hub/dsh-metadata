# This file is for the weir boxes that are measuring drain and overland flow in the bowl.

## Overview
- Purpose: Notebook/log documenting the weir boxes measuring drain flow (DRAIN) and overland flow (OLF) in the bowl.
- Time span: Install date 11/04/06 with ongoing notes through 13/11/09 (and references up to 2009).
- Data elements: Pressure transducers (PTs) in both weir boxes, logger readings, water height above the V-notch, and subsequent analysis in spreadsheets.
- Measurements: Heights above V-notch used to estimate flow; V-notch crest references and box dimensions recorded (drain ~0.4074 m^2, OLF ~0.404022 m^2; two measurement methods for depth above V-notch).
- Additional sensors: Turbidity sensors installed on outflows (29/11/06).

## Data collection methods and metrics
- Instruments: Pressure transducers in each weir box; loggers with data downloads; tipping buckets for flow estimation.
- Measurements and methods:
  - Water height above V-notch used to derive flow; measurements taken at or near standard GMT times (e.g., 1010–1015 GMT).
  - Two methods to measure depth above V-notch; occasional recalibration when V-notch not straight (noted differences in measurement values).
  - TB (tipping bucket) data used to estimate flow when certain conditions hinder direct measurement.
- Calibration and verification:
  - Regular calibration notes, including zero-offset adjustments, especially in 2009 after periods of data gaps or suspected drift.
  - Battery and logger calibration issues noted (e.g., jumps in PT values, offset corrections applied in analysis spreadsheets).
- Data quality flags and corrections:
  - Jumps in PT values acknowledged and corrected in the analysis file.
  - Periods with no data or doubtful data due to battery, logger issues, or freezing conditions flagged as needing caution or re-checks.
  - Adjustments documented when data could be corrected post-download (e.g., after 03/01/07, 18/01/07, 03/03/08).

## Key events, maintenance, and changes
- 2006
  - Initial installation and early tests; batteries changed; occasional dry runs and tests of loggers.
  - 27/04/06: pressure transducers and logger removed for testing.
  - 14/07/06: OLF and DRAIN measured; logger restart procedures documented.
- 2007
  - Weather-related challenges: snow ingress into stilling wells; wooden lids added 11/03/07 to prevent disturbance.
  - 03/01/07 onward: bowl drain disconnected temporarily; remeasurement of V-notch depth later.
  - 24/07/07: OLF weir box noted presence of dead rodents; minor blockages observed.
  - 07/06/07: weir box dimensions measured for area calculations.
  - 21/11/07 onward: data jumps and calibration notes; some data flagged as unreliable due to logger issues.
- 2008
  - Recurrent data quality issues: data jumps after downloads; freezing conditions affecting both OLF and DRAIN measurements.
  - 12/06/08: weir box calibration measurements; reinstallation of PTs; notes on data anomalies post-cleaning.
  - 18/02/08 onward: freezing suspected to shift PT position; multiple periods with suspected erroneous values.
  - 25/11–05/12/08: data loss due to dodgy logger.
  - 28/11/06: turbidity sensors installed on bowl outflows (Alex H).
  - 20/05/08: issues with black organic/inorganic gunk affecting measurement; adjustments documented.
- 2009
  - 04/06/09: new zero offset calibration for both boxes; notes that drain inflow pipe was not properly reinstalled during a period, making some data unsuitable.
  - 20/02/09–22/04/09: drain flow out of action; estimation of flow based on pre/post periods and low rainfall.
  - 13/11/09: logger disconnected from battery and reconnected; ongoing concerns about data integrity.

## Data quality, challenges, and adjustments
- Technical and environmental challenges:
  - Frequent data gaps and questionable readings due to logger/battery issues, freezing, snow, and debris blockage.
  - Sudden jumps in PT values requiring adjustments in the spreadsheets and/or recalibration.
  - Sensor misalignment or relocation concerns after freezing could shift base readings; recalibration required.
- Calibration and correction practices:
  - Zero-offset recalibrations performed (notably 04/06/09) with new baselines for 0 flow defined.
  - Data corrections applied post-download when PT jumps occurred, with explicit notes to recheck during next download.
  - Some data deemed not suitable for use due to poor installation or reinstallation issues (e.g., drain pipe reinstallation problems).
- Data integrity and continuity:
  - Data loss periods due to dodgy loggers, battery issues, or disconnected loggers.
  - Instances where data was not fully collected from the logger due to low battery voltage.
  - Missing or uncertain periods require re-verification, re-downloads, and possibly re-calibration.

## Data management implications for Data Leaders
- Data availability and reliability:
  - Extended, multi-year field data with frequent interruptions; need robust hardware redundancy and battery management.
  - Clear gaps and data suitability notes essential for downstream analyses and policy-informed decisions.
- Data quality governance:
  - Frequent calibrations, offset corrections, and data flags indicate need for standardized data quality rules and metadata schema.
  - Documentation of measurement method changes, calibration events, and hardware issues is critical for traceability.
- Data standards and metadata:
  - Variation in measurement methods (two depth-measurement methods; changes in PT positioning) highlights need for consistent metadata around measurement procedures.
  - Recording of box dimensions, V-notch geometry, and crest heights is essential for reproducibility.
- Operational considerations:
  - Weather implications (snow, freezing) significantly affect data; contingency planning and protective measures (e.g., lids) are necessary.
  - Maintenance events (cleaning, sediment removal, instrument recalibration) should be integrated into data quality timelines.
- Opportunities for improved data strategy:
  - Introduce data quality flags, automated anomaly detection, and standardized calibration pipelines.
  - Centralize metadata for long-term traceability and to support cross-referencing with other data streams (e.g., turbidity sensors).
  - Plan for redundancy (backup loggers, power supplies) and documented recovery procedures after data gaps.

## End status and takeaways
- Final notes indicate ongoing monitoring with periodic recalibration and ongoing concerns about data integrity due to environmental and hardware factors.
- The dataset demonstrates the importance of rigorous data governance, calibration discipline, and clear documentation to support reliable interpretation of drain and overland flow measurements.