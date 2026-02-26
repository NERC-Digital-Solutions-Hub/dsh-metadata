# AWS Calibration and Maintenance Log (2006-2009)

## Overview
- A detailed log of calibration, maintenance, data quality checks, and equipment changes for an Automatic Weather Station (AWS) and associated sensors (soil temperature, air temperature, humidity, net radiometer, pyronometer, weather sensors, wind, solarimeter, etc.).
- Frequent recalibrations, offset adjustments, software reprogramming, and hardware replacements.
- Documentation of data gaps, sensor issues, and steps taken to resolve them.

## Calibration and adjustments timeline
- 21/09/06: Soil temperature check at AWS; initial readings recorded.
- 27/09/06: Soil temp readings noted; ongoing monitoring of sensor behavior.
- 10/11/06: Net radiometer too high by ~2.5°C; adjusted. Air temp ~0.25°C too low; adjusted. Humidity ~4% too low; not corrected at this time.
- 16/11/06–28/11/06: Net radiometer inspected and a new logger installed; pyro recalibrated.
- 03/01/07–20/02/07: Anemometer screw issue fixed; wiring/program conflicts between net radiation and humidity channels identified and corrected; new program installed.
- 08/03/07–19/03/07: Pyronometer reinstalled; temperature issue resolved with updated program; further confirmations of sensor alignment and calibration.
- 24/01/07: Logger replaced; pyro reinstalled.
- 20/05/08–20/04/09: Soil temperature probe calibration and multiple offset checks; field offset adjustments (discussion of model-based correction) and data adjustments (see data corrections).
- 02/04/09–23/04/09: New Vaisala humidity/temperature probe introduced; channel reallocation and testing; data gaps noted with the new probe.
- 28/05/09: AWS data download indicated missing 10-minute data from the new temperature/humidity probe.
- 04/06/09: Installation of a new net radiometer and reprogramming of AWS using AWS_03_JUNE with six channels updated.

## Data quality issues and fixes
- Recurrent data gaps and potential data loss due to:
  - Power/recharging issues and solar panel limitations.
  - Memory faults and data logging interruptions.
  - Physical damage or misalignment (e.g., net radiometer angled, sheep damage to wiring).
- Calibration checks against calibrated probes and handheld references:
  - Regular offset adjustments for air temperature, soil temperature, and humidity.
  - Pyronometer range and signal scaling corrected (e.g., range corrected from 2500 mV to 25 mV).
  - Net radiometer channel conflicts resolved; new multiplication factors applied (e.g., 113.77 vs 112.86).
- Notable data correction notes:
  - Temperature corrections included subtracting/adding fixed offsets and applying linear adjustments (example: add 4.034°C to past data after offset fixes; adjust using y = 0.9845x + 0.5942).
  - Some earlier lines indicate adjusting AWS temperature readings by a specific offset after calibration checks; implications were to align AWS readings with calibrated references.

## Equipment maintenance and replacements
- Mechanical and hardware fixes:
  - Anemometer screw securing and subsequent tightening of guy ropes; later reports of net radiometer damage requiring removal and reinstallation.
  - Replacement of logger hardware and subsequent reprogramming.
  - Reinstalled pyronometer and reconnected to logger after battery disconnections.
- Sensor upgrades:
  - Introduction of Vaisala HMP temperature/humidity probe in 2009; partial success with data gaps noted post-installation.
  - New net radiometer installed in June 2009 with updated calibration factor and reprogrammed AWS configuration.

## Data corrections and formulas
- Offsets and calibration corrections documented:
  - Air temperature offset updated to bring AWS readings in line with calibrated probes (e.g., offset ~+0.234°C after checks).
  - Soil temperature calibrations involved multiple offsets; final recommended adjustment expressed as applying a linear equation (e.g., y = 0.9845x + 0.5942) and adding an overall offset (e.g., +4.034°C) for older data.
- Net radiometer calibration:
  - New multiplication factor introduced (113.77) to replace the old factor (112.86) with the 04/06/09 update.
- Data alignment:
  - Occasional guidance to subtract or add fixed values to reconcile AWS data with calibrated references and handheld measurements.

## Current status and actions (as of 04/06/09)
- A new net radiometer installed; AWS reprogrammed with AWS_03_JUNE.
- Six data channels updated; ongoing verification of data quality with new hardware and software configuration.
- Continued monitoring of data completeness (noting past and present gaps) and calibration integrity with the new Vaisala probe and updated net radiometer.