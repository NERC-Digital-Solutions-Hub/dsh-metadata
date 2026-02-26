# Drain Flow Data Logging and Calibration Log

## Overview
- A longitudinal log of a drain-flow measurement system using tipping buckets (TB) and a weir box, including calibration, maintenance, and data quality notes from 2005 to 2009.
- Purpose: document intervals, calibrations, repairs, and data-quality decisions that affect data usability and provenance.

## Data Collection System & Characteristics
- Measurement setup:
  - Tipping buckets (TB) paired with a reed switch/magnet for flow tipping detection.
  - Weir box used for drain-flow measurement.
  - Data logger (TinyTag) and associated readings; occasional transducer issues noted.
- Recording interval:
  - Initial change from 10-minute to 5-minute intervals to align with overland flow trapping.
- Calibration and measurement units:
  - Early calibration: 30 L through TB resulting in 11 tips; initially interpreted as 2.91 L per tip.
  - Later calibration adjustments: 30.66 L = 11 tips → ~2.79 L per tip; a linear incremental change was applied to account for drift about six months after initial calibration.
- Timekeeping:
  - Occasional time-stamp issues due to GMT/BST changes; corrections documented in the data file.
- Data and data products:
  - Data include both raw readings and calibration-derived tip counts with associated volumes per tip.
  - Data flagged for disregard during calibration or maintenance windows (e.g., when calibration activities or hardware issues occurred).

## Key Maintenance, Calibrations, and Data Quality Events
- Data collection adjustments:
  - 22/02/05: Recording interval changed to 5 minutes.
- Hardware and sensor issues:
  - Water not fully flowing through the tipping bucket due to blockages or setup (e.g., icicle formation, magnet issues, reattaching reed switch, leaks).
  - TB components dislodging or malfunctioning (e.g., magnet off, tipping-bucket base issues, bucket replacement).
  - Weir box and TB connections problems; battery failures; transducer box water ingress; weather-related impacts.
- Calibration activities and data handling:
  - Periodic calibrations, reinstallation, and re-calibration when discrepancies observed.
  - Periods explicitly marked to ignore data during calibration activities or hardware repairs (e.g., 08:54–12:00 GMT during weir box calibration; other time blocks flagged as ignore due to calibration or data diversion).
  - 04/06/07 calibration check with precise poured volume to verify tips; re-checks followed by magnet replacement and resumption of logging.
  - 17/11/08: applied a linear incremental adjustment to tip volume to reconcile differences between 07/06/07 and 14/11/08 calibrations.
- Data quality notes:
  - Timstamp consistency issues corrected in subsequent analyses.
  - Data gaps and anomalies associated with calibration events, reconfigurations, and equipment maintenance.
  - Several instances of “ignore data” due to calibration or diversion (e.g., water diverted for calibration; sediment removal observed drop in readings).

## End State and Usability Implications for Data Leaders
- By mid-2009, the system was deemed suitable for use again after a series of repairs, calibrations, and data-quality adjustments.
- Practical implications:
  - Need for robust metadata around calibration events, hardware changes, and timekeeping adjustments to maintain data provenance.
  - Regular calibration and validation are essential to account for drift in TB tipping volumes and to correct for environmental effects (gunk buildup, leaks, battery changes).
  - Clear data governance around periods of ignore data or data diversion to prevent misinterpretation in analyses.
  - Documentation of calibration constants (tips per liter) and any applied adjustments is critical for cross-study comparability.
- Recommendations for Data Leaders:
  - Maintain a detailed, queryable log of calibration events, hardware changes, and timekeeping adjustments as part of data provenance.
  - Implement standardized metadata fields for tip volume per tip, calibration date, and any incremental adjustments.
  - Establish formal criteria for marking data as usable vs. ignored during maintenance windows and calibrations.
  - Plan for redundancy and monitoring to minimize data gaps from hardware failures (e.g., magnet, transducer housing, battery).
  - Align future data pipelines to automatically flag and compensate for known calibration periods, time-zone changes, and data diversions.