AWS Weather Station Calibration and Maintenance Log

## Overview
- A chronological record of calibrations, maintenance, sensor adjustments, data quality checks, and system updates for an Automatic Weather Station (AWS).
- Focuses on ensuring data accuracy, proper metadata, and usable datasets, while documenting data gaps, corrections, and hardware/software changes.

## Key calibration and maintenance actions (highlights by date)
- 16/11/06 to 28/11/06
  - Net radiometer inspection; new logger installed; Pyronometer recalibration.
  - Anemometer and humidity/temperature probes reviewed; several wiring and channel alignment checks.
- 03/01/07 to 24/01/07
  - Anemometer alignment corrected (screw issue); soil probe reinserted at 5 cm depth; Pyronometer adjustments and logger interactions noted.
- 20/02/07
  - Updated program to separate Net radiation and Humidity channels; linked channels corrected.
- 20/05/08
  - Soil temperature probe removed for calibration; data gaps around 28/04/08–05/05/08.
- 28/05/09
  - No 10-minute data from new temperature/humidity probe; daily data present.
- 20/04/09 to 23/04/09
  - Vaisala HMP temperature/humidity probe introduced; channel wiring and signal alignment adjusted.
- 01/06/09
  - Pyronometer and AWS comparisons with calibrated probe showed consistency improvements; continued monitoring of offsets.
- 03/06/09 to 04/06/09
  - Installation of a new net radiometer with updated multiplication factor 113.77 (replacing 112.86); AWS reprogrammed to AWS_03_JUNE.

## Data quality adjustments and metadata
- Air temperature
  - Offsets recalibrated; average difference with calibrated probe around 0.23–0.24 °C; previous data flagged for potential adjustment.
  - Note indicating that earlier data may require correction by a substantial offset (approximately +4.0 °C) due to calibration changes.
- Net radiometer
  - Channel alignment issues identified (conflict between net radiation and humidity channels); fixed by reprogramming and later hardware update.
  - New net radiometer installed and data processing factor updated (113.77).
- Pyronometer and radiometric readings
  - Range adjustment from 2500 mV to 25 mV to improve accuracy; ongoing cross-checks against handheld probes.
- Soil temperature
  - Multiple calibrations; discussion of offsets with a suggested equation y = 0.9845x + 0.5942; historical data adjustments proposed (including an offset of +4.034 °C for older data per notes).
- Humidity and temperature (new vent)
  - Vaisala HMP probe installed; channel reconfiguration and signal calibration completed.
- Battery, solar power, and data transmission
  - Data gaps linked to solar charging issues and battery/solar panel recharging; occasional data loss noted (e.g., January 2009).

## Notable hardware and software changes
- Net radiometer
  - Replaced and re-calibrated; updated multiplication factor to 113.77; AWS reprogrammed with June 3 version.
- Logger and sensors
  - New logger installed (late 2006); ongoing sensor maintenance (anemometer, wind vane, net radiometer, soil probes).
- Vaisala HMP
  - Introduced to replace/augment existing temperature/humidity sensors; wiring adjustments completed to integrate with AWS.

## Data gaps, reliability, and maintenance notes
- Data gaps
  - 28/04/08–05/05/08: data removed during soil temp calibration period.
  - 06/01/2009–12/01/2009: data loss possibly due to solar charging issues.
  - 07/2007 onward: intermittent anomalies (e.g., wind data near zero due to animal-induced damage to wiring; repairs performed).
- Physical maintenance
  - Hallmarks include re-tensions of guy ropes, realignment of sensors, repair/re-soldering of cables, and addressing mechanical misalignment (e.g., net radiometer and anemometer angles).

## Sensor heights and layout (reference)
- Net Radiometer ~1575 mm
- Humidity/Temperature probe ~1475 mm
- Wind vane ~ 2395 mm
- Anemometer ~ 2500 mm
- Solarimeter ~ ~2867.5 mm (average)
- Note: Heights documented for maintenance and alignment purposes; adjustments observed when anomalies occurred.

## Data stewardship implications
- Provenance and metadata
  - Maintain detailed change logs for calibrations, sensor replacements, channel reassignments, and software/version updates to support retrospective data corrections.
- Data quality controls
  - Regular cross-checks with calibrated references; document offsets, calibration coefficients, and their temporal applicability.
- Data availability and gaps
  - Track and explain data gaps due to power/battery issues, weather events, or hardware failures; implement contingencies to minimize future losses.
- Interoperability and standardization
  - Resolve channel conflicts (e.g., net radiation vs. humidity) and ensure consistent metadata when integrating new sensor types (e.g., Vaisala HMP) into existing data streams.
- Communication and governance
  - Clearly communicate when recalibrations imply back-calibration of historical data; document rationale and methods for end-users.
- Data quality assurance workflow
  - Include calibration schedules, calibration kits used, comparisons with handheld/probe references, and decisions on data adjustments (with versioned records).