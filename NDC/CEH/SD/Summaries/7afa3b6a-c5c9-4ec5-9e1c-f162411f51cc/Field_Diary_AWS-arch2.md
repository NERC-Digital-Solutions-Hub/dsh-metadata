# AWS Data Quality Assurance and Calibration Log (2006-2009)

## Purpose
- Document calibration, maintenance, and QA activities for the Automatic Weather Station (AWS) and associated sensors.
- Ensure data integrity, standardised processing, and readiness for storage/upload to data portals.

## Data QA and Calibration Activities
- Routine calibration checks and cross-validation with calibrated probes (air, soil, and pyronometer probes).
- Air temperature offset adjustment: offset set to +0.234°C after multiple checks; implication that older data require a +4.034°C correction.
- Soil temperature calibration: developed a correction relation (y = 0.9845x + 0.5942); discussion that previous data could be adjusted by +2.58°C (or +0.51 using the gradient), with the more precise approach requiring the equation.
- Pyronometer range correction: reading range corrected from 2500 mV to 25 mV for accurate radiation measurements.
- Net radiometer calibration: multiplication factor updated from 112.86 to 113.77; AWS reprogrammed on 04/06/09 with AWS_03_JUNE.
- Ongoing data verification: comparisons between AWS readings and handheld/calibrated probes; notes of potential discrepancies (e.g., range, channel mapping) until corrected.
- Data loss and gaps identified during calibration and verification periods (e.g., data loss 28/04/08–05/05/08; gaps around early January 2009).

## Maintenance and Equipment Updates
- Anemometer issues and fixes:
  - 03/01/07: Screw holding the anemometer fell out; repaired.
  - 15:40 onward in 2007: wind data affected by chewed wires; anemometer removed, re-wired, and reinstalled.
- Sensor and logger interventions:
  - 28/11/06: Installed new logger; recalibrated pyronometer.
  - 24/01/07: Pyronometer removed and soil probe repositioned; battery briefly disconnected.
  - 20/02/07: Software update to resolve channel conflicts between net radiation and humidity probe.
  - 07/03/07 and 08/03/07: AWS data download and pyronometer reinstallation; temperature issues addressed.
  - 19/07/07 and 24/07/07: Net radiometer alignment issues (angled readings); corrected by realigning and tightening guy ropes.
  - 25/07/08: AWS noted as being at an angle due to top guy peg issue.
  - 04/06/09: New net radiometer installed; AWS reprogrammed with updated configuration (AWS_03_JUNE).
- Sensor repositioning and heights:
  - Documented sensor heights above ground (net radiometer, humidity/temperature probe, wind vane, anemometer, solarimeter) for consistent mounting and data interpretation.
- Sensor substitutions and future-proofing:
  - 20/04–23/04/09: Attempts to install a Vaisala HMP temp/relative humidity probe; implementation not completed in this period.
- Other hardware notes:
  - Occasional data loss and glitches attributed to hardware events; ongoing monitoring recommended.

## Data Issues and Data Management
- Data quality issues identified:
  - 04/2009: Inconsistent data from the new temp/rh probe during initial deployment; later attempts to resolve.
  - 2009: RH drift and January data gaps flagged for review.
- Data integrity practices:
  - Emphasis on verification against calibrated probes, documentation of offsets and correction factors, and alignment of channel wiring to prevent misinterpretation (e.g., net radiation vs humidity channels).
- Data storage and sharing:
  - Routine to store created datasets and upload to appropriate data portals; aim to enable access to underlying data used to generate outputs.

## Key Observations and Decisions
- Recurrent calibration and channel configuration issues require careful documentation and standardized correction procedures to ensure long-term data comparability.
- Where data corrections are proposed (e.g., temperature offsets, soil temp equation), clear records are kept to support retrospective data adjustment if needed.
- Significant maintenance events (sensor realignments, wiring repairs, and net rad recalibrations) are essential to maintaining data quality and reducing spurious readings.

## Conclusions and Forward Look
- The AWS site has undergone extensive calibration, software updates, and mechanical maintenance to improve data accuracy and reliability.
- Ongoing QA, channel management, and data provenance (including access to raw underlying data) remain crucial challenges and focus areas for continued environmental monitoring and policy performance assessment.