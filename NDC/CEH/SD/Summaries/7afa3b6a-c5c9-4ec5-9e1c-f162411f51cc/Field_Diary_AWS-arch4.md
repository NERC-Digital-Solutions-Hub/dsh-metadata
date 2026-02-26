# AWS Weather Station Calibration and Maintenance Log

## Overview
- Series of calibration, maintenance, and data quality notes from 2006–2009 for an Automatic Weather Station (AWS) and related sensors (soil temperature, air temperature, humidity, net radiometer, pyronometer, wind, solarimeter).
- Focus on data integrity, sensor alignment, offset corrections, and software/program updates to ensure accurate measurements and usable metadata.
- Highlights the ongoing challenges of data gaps, sensor failures, and the need for careful documentation and versioning of data processing.

## Data Quality Actions and Corrections
- Calibration and offset adjustments:
  - 21/09/06–10/11/06: Soil temperature required a +2.5°C calibration; air temperature +0.25°C offset; humidity +4% noted but not corrected at that time.
  - 16/11/06 onward: net radiometer and other sensors checked; calibration notes recorded.
  - 01/05/07 onward: various calibration and tightening actions; offsets updated to align with calibrated references.
  - 04/06/09: installation of a new net radiometer and reprogramming of AWS parameters (AWS_03_JUNE); six channels updated accordingly.
- Sensor and program fixes:
  - 03/01/07 and 19/03/07: mechanical fixes (anemometer screw, recalibration of temperature readings) and program updates to resolve temperature/recording discrepancies.
  - 20/02/07: updated and installed new program to fix channel conflicts between net radiation and humidity sensors.
  - 04/06/09: new net radiometer installed and AWS reprogrammed; consistency across six channels ensured.
- Data processing and correction notes:
  - 2006–2007: references to adjusting data using calibration offsets; specific note that prior data may require adjustment (e.g., “previous data needs to be adjusted by adding 4.034 oC” in a calibration context).
  - Soil temperature calibration discussions introduced a model (y = 0.9845x + 0.5942) for post-hoc adjustment; earlier offsets adjusted accordingly.
  - Pyronometer and air-temperature calibration checks against handheld/probe references; several adjustments to ensure agreement.
- Data quality verification:
  - Comparisons between AWS readings and calibrated probes conducted during calibration campaigns; documentation of differences and corrective factors (e.g., average differences and standard deviations).
  - Range and scaling corrections identified for pyronometer readings (range set to 2500 mV vs 25 mV for more accurate readings).

## Equipment Issues and Maintenance Timeline
- Mechanical and structural issues:
  - Anemometer: screws/damage caused by misalignment; later found to have fallen out, re-secured; wind data momentarily questionable due to structural faults.
  - Net radiometer: multiple incidents of misalignment (e.g., 45° angle) and eventual damage; multiple replacements and realignments; wires damaged by external factors (sheep) and subsequently repaired.
  - Logger upgrades/installations: 28/11/06 installed new logger; ongoing maintenance to ensure memory and data integrity.
-Environmental and power-related issues:
  - GPS-like memory and data loss events linked to power/battery or solar recharge (noted data loss in early 2009 and intermittent solar charging issues in January 2009).
  - Bird/animal interactions causing wire damage and subsequent repairs (sheep chews; re-soldering).
-Probe updates and replacements:
  - Introduction of Vaisala HMP temperature/humidity probe (installed 22/04/09; implementation issues resolved by 23/04/09).
  - Soil temperature probes moved/reinstalled (e.g., 10 cm depth adjustments in 2009).
- Routine maintenance:
  - Guy ropes tightened (01/05/07; 24/07/07 with subsequent re-tightening).
  - Calibration checks and cross-verifications with calibrated references conducted periodically.

## Data Gaps, Provenance, and Metadata Considerations
- Data gaps:
  - Notable data losses: 28/04/08–05/05/08; 06–12 January 2009; other periods with interrupted 10-minute vs daily data streams.
- Provenance and versioning:
  - Frequent reprogramming and sensor replacements necessitate clear metadata about software versions (e.g., AWS_03_JUNE), calibration offsets, and sensor models.
  - Explicit notes on data adjustments (e.g., “add 4.034 oC” to prior data; apply the soil temp equation) underscore the need for traceable data rewrites and versioned datasets.
- Data quality controls:
  - Cross-validation with handheld/calibrated probes documented; continuous checks to ensure sensor outputs align with physical references.
  - Documentation of thresholds, ranges, and offsets used to harmonize sensor outputs across years.

## Implications for Data Leaders
- Emphasize end-to-end data governance:
  - Maintain comprehensive, versioned calibration and maintenance logs that are linked to data streams.
  - Ensure metadata captures sensor changes, program versions, and applied corrections with precise timestamps.
- Prioritize data quality and usability:
  - Implement automated data quality checks to flag misalignments, offset drift, and potential data losses early.
  - Establish standardized procedures for recording and applying post-hoc adjustments (and clearly communicate when data has been retroactively corrected).
- Foster collaboration and transparency:
  - Coordinate with data communities and partners to harmonize calibration practices and metadata standards.
  - Encourage co-ownership of data products by policy colleagues and analysts to align data capabilities with user needs.
- Plan for resilience and continuity:
  - Mitigate data gaps by securing physical protections (e.g., wildlife-proofing sensors) and robust power management; document contingencies and recovery steps.
  - Maintain backup data streams where possible and document any reprocessing requirements for legacy data.