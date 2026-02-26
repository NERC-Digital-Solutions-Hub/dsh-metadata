# AWS Data Calibration, Maintenance, and Quality Notes (2006-2009)

- Overview
  - A detailed log of calibrations, hardware maintenance, sensor issues, data corrections, and data gaps for the Automatic Weather Station (AWS) from 2006 to 2009.
  - Highlights the iterative process of validating sensor readings against calibrated probes, fixing physical components, and updating data interpretation rules.

## Calibration and maintenance timeline

- 21/09/06 – 27/09/06
  - Soil temperature checks performed at AWS; initial readings around 15°C.

- 10/11/06
  - Soil temperature calibration: readings ~2.5°C too high.
  - Air temperature offset: ~0.25°C too low.
  - Humidity ~4% too low (not corrected in this log).
  - Net radiation and Pyronometer appear sensible but require calibration kit verification.
  - Caution advised when downloading data to avoid disturbing the unit.

- 16/11/06
  - Net Radiometer inspected; condition deemed good.

- 28/11/06
  - New data logger installed; Pyronometer recalibrated.

- 03/01/07
  - Anemometer mounting screw had fallen out; repaired.

- 24/01/07
  - Pyronometer temporarily removed; soil probe repositioned (5 cm depth, moved downhill and left of AWS).

- 15/02/07 – 20/02/07
  - Identified a programming conflict: net radiation channel assignment conflicted with humidity channel.
  - New program uploaded (20/02/07) to resolve issue.

- 07/03/07 – 08/03/07 – 19/03/07 – 20/03/07
  - AWS data download; Pyronometer installation pending; net radiation functioning but temperature showed issues.
  - Temperature problem resolved after new program (20/02/07) and program updates; a recalibration/isolation step noted.

- 01/05/07 – 19/07/07 – 24/07/07
  - Routine maintenance (guy ropes tightened).
  - 19/07/07: Net Radiometer orientation corrected (from ~45° to horizontal). Additional rope tightening noted.
  - 24/07/07: Net Radiometer damaged again (angle issue) and subsequently removed; ropes re-tightened.

- Sensor heights (installs around 2007)
  - Net Radiometer: ~1575 mm
  - Humidity/Temperature probe: ~1475 mm
  - Wind vane: ~2395 mm
  - Anemometer: ~2500 mm
  - Solarimeter: ~2867.5 mm (average of 2860–2870 mm)

- 15:40 (mid-late 2007)
  - Wind data largely 0; cause attributed to sheep chewing through wire leading to anemometer damage; repaired with re-soldered wiring.

- 16/11/07 – 14/11/07
  - Recurrent checks on net radiation and sheltering; ongoing maintenance.

- 20/04/09 – 22/04/09 – 23/04/09
  - Plan to install Vaisala HMP temperature/relative humidity probe; data channels reworked to accommodate new sensor.
  - 22/04/09: RH/Temp probe installed; working channels adjusted on 23/04/09.

- 01/06/09 – 04/06/09
  - Vaisala-related sensor integration in progress; calibration notes documented.
  - 03/06/09 – 04/06/09: New net radiometer to be installed; AWS reprogrammed with AWS_03_JUNE; six channels updated; six entries documenting the reprogramming.

- 04/06/09
  - New net radiometer installed; AWS reprogrammed accordingly (AWS_03_JUNE) across all channels.

## Hardware issues and fixes

- Anemometer
  - Loose screw (03/01/07) caused misalignment; repaired.
  - Repeated wind data anomalies due to wiring (sheep damage on 15:40 in 2007); repaired with soldering and reinstallation of anemometer.

- Net Radiometer
  - Repeated detachment/angle issues (07/07/07 and 24/07/07); eventually redirected to correct orientation.
  - 27/06/07 height and mounting adjustments recorded.

- Power and data logging
  - New logger installed (28/11/06); ongoing calibration of Pyronometer (Pyronometer adjustments and range issues later identified).
  - Data gaps and occasional data loss linked to battery recharging and memory faults; several notes cautioning about data integrity during maintenance.

- Hydrometeorological probes
  - Humidity/Temperature probes moved and recalibrated; later upgrades to Vaisala HMP system planned (and initial installation attempted in 2009).

- Miscellaneous
  - “Flying saucer” (instrument housing) reviewed (02/04/09) to check for data glitches.
  - AWS occasionally found angled or misaligned; corrective actions documented.

## Sensor setup, calibrations, and corrections

- Temperature calibrations
  - Soil temperature calibration indicated a need to adjust offsets; recommended using a linear equation y = 0.9845x + 0.5942 for field data post-calibration.
  - Initial offset for soil temperature around -2.58°C; later recommendation to apply +0.51 or more complex correction.

- Air temperature
  - Offset adjustments were performed after calibration checks; a notable conclusion was that a calibration adjustment of +0.234°C was necessary to align AWS readings with calibrated probes.
  - This implied a broader historical data correction (noted as potentially +4.034°C for past data in the log).

- Net radiation
  - A change in multiplication factor from 112.86 to 113.77 planned/implemented on 04/06/09 as part of a net rad calibration update.

- Pyronometer
  - Range/scale adjustment identified: set range at 2500 mV was incorrect and corrected to 25 mV for more accurate readings.
  - Recalibrations conducted to ensure consistency with handheld references.

- Humidity/temperature sensors
  - Initial attempts with humidity/temperature probes encountered channel conflicts and data integrity issues.
  - 2009 efforts to install Vaisala HMP RH/Temp probe; installation and channel adjustment occurred, with partial success (not fully functional until mid-April 2009).

## Data gaps, quality issues, and data integrity

- Data gaps
  - 28/04/08 – 05/05/08: data loss associated with calibration activity and probe removal.
  - 06/01/2009 – 12/01/2009: data loss period; suspected solar recharging or battery issues affecting data capture.
  - 28/05/09: no 10-minute data from new RH/Temp probe; only daily data available.

- Data quality concerns
  - Persistent data corrections required for temperature and radiation components due to calibration offsets and sensor reconfiguration.
  - Channel conflicts and sensor miswiring historically caused misinterpretation of radiation and humidity signals until resolved with program updates.

- Calibration validation
  - Regular cross-checks between AWS sensors and calibrated handheld/probe instruments were used to derive offsets and corrections.
  - Corrections documented to improve data comparability, with explicit notes on how to adjust historical data.

## Future plans and installations

- Vaisala HMP humidity/temperature probe
  - Installation attempted in 2009; partial success with channel reconfiguration.
  - Planned to enhance humidity/temperature measurement reliability and reduce cross-channel interference.

- Ongoing net radiation and sensor recalibration
  - Continued updates to net radiation calibration factors and reprogramming of AWS channels (June 2009 update).

## Key takeaways for analysts

- Expect substantial historical data adjustments due to calibration offsets (air, soil temperatures) and net radiation scaling changes.
  - Air temperature offset corrections (~+0.234°C identified; earlier data potentially requiring larger corrections).
  - Soil temperature corrections may involve a linear transformation; original offsets and proposed equations should be applied consistently to historical data.
  - Net radiation factor updates (112.86 → 113.77) in June 2009 to improveradiation measurements.
  - Pyronometer scaling correction (10 mV vs 25 mV range) to improve shortwave radiation readings.
- Hardware reliability is a recurring issue (anemometer wiring, sheep damage, AWS tilt, and logger reliability) that can introduce data gaps and quality concerns.
- Sensor upgrades (Vaisala HMP) were planned to improve humidity/temperature measurements; consider metadata documenting sensor changes and their impact on long-term time series.
- When using this dataset, consult calibration logs for period-specific adjustments and apply documented corrections; maintain detailed metadata to track sensor changes and calibration decisions.