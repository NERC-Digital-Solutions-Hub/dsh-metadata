# SUPPORTING DOCUMENTATION:

- Purpose: Describes data collection, structure, and methods for monitoring cricket behaviour to support environmental monitoring and policy-like scrutiny of ecological data over time.
- Collaboration and access: Encourages collaboration; provides contact (Tom Tregenza) before using the data and notes potential access to additional information and expertise.

## Data collection overview

- Study focus: Behaviour of male crickets around burrows, observed via video.
- Monitoring setup: 140 infrared day/night cameras recording 24/7 around burrows.
- Measured variable: Time spent performing target behaviours (in minutes) with mean ground-level temperature as a covariate.
- Data quality emphasis: Quality control to detect inconsistencies (e.g., same cricket recorded at two burrows simultaneously).

## Nature and units of recorded values

- Behaviours (five observed): Outside, Feeding, Calling, Fleeing, Inside.
- Additional fields: SunAvailable (sun patch around burrow), InSun (movement to sun/shade), Date, Duration (minutes), Temp (mean temperature during the observed duration).
- Covariate: Temperature (ºC).

## Data structure and files

- Three data files:
  - 2019_MaleBehaviour: Per-event records with fields such as Tag, Pop, Burrow, Behav, Date, Duration, Temp.
  - 2019_Populations: Population-level data including locality name, altitude, coordinates.
  - 2019_Specimens: Individual specimen data including Population, Tag, Sex, Mass, Released.

## Experimental design

- Population sampling: 132 male crickets from 10 locations (five under 160 m a.s.l., five above 1,200 m a.s.l.); 127 adult females from nearby meadows.
- Rearing and release: Crickets reared in separate boxes, labeled with two-character IDs, released into random burrows within the meadow, cages placed to limit movement initially.
- Monitoring setup: 140 high-resolution IR cameras installed over burrows; direct observations supplement video monitoring for non-videoed burrows.
- Timeframe: Monitoring from release through the breeding season with continuous video recording.

## Field work and instrumentation

- Cameras: Vivotek IP8330 connected to five computers with motion-triggered recording (i-Catcher software).
- Weather data: Davis Vantage Pro2 weather station at meadow center, logging every 10 minutes; six additional ground sensors (three surface, three in buried PVC pipes).

## Calibration and measurement specifics

- Calibration: Weather station factory-calibrated; no additional equipment beyond a computer; time is the primary measured variable.

## Analytical methods

- Data extraction workflow (two steps per day):
  - Step 1: Rough pass across 16 cameras simultaneously for the first ten minutes past each hour to identify active burrows.
  - Step 2: Detailed per-camera viewing starting from identified activity; playback backward to determine start times, then forward to record target behaviours.
- Data handling: Observations recorded in MS Excel, then imported into MS Access for processing.
- Observer setup: Nine groups of nine observers to minimize inter-observer differences across altitudes.

## Quality control

- Consistency checks using Access queries to detect errors (e.g., a cricket recorded as using two burrows at the same time).

## References

- Rodríguez-Muñoz, R., et al. (2010). "Natural and sexual selection in a wild insect population." Science 328: 1269-1272.

## Alignment with monitoring objectives

- Data standardization: Uses explicit, time-based behavioural units and a consistent covariate (temperature) to enable cross-time comparisons.
- Verification and cleaning: Built-in QC steps to ensure data integrity before analysis.
- Outputs and storage: Data are organized into clearly defined datasets and prepared for storage and portal upload; outputs can be translated into reports, maps, and charts for environmental monitoring.
- Data accessibility: Encourages collaboration and provides contact to access additional information, supporting broader use and integration with other environmental datasets.